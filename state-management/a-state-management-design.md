
## 设计一个状态管理方案
### 要求
1. 独立于视图框架
2. 统一的接口，具有鲁棒性
3. 完备的能力，能够自行运行、管理副作用
4. 可观测、易调试

### 基本功能

1. 状态存储

状态需要有初始值，通常是一个默认值对象集合。
```js
const ins = new State({
    a: 1,
    b: 'hello'
})
```

1. 状态的获取
直接获取
```js
ins.state.a
ins.state.b
```

1. 状态的更新

```js
ins.setState({
    a: ins.state.a + 1
});
```

4. 状态的订阅

通常会提供类似 rxjs 的 subscribe 方法，可以订阅状态的变化。
```js
ins.subscribe(state => {
    console.log(state);
});
```

这看起来够用，但是，实际使用过程中的场景是希望更加细粒度并可读的。
```js
// 状态字段的独立订阅，同步与异步
ins.states.a.subscribe
ins.asyncStates.a.subscribe

// 状态整体的订阅，同步与异步
ins.fullState.subscribe
ins.asyncFullState.subscribe

// 状态更新的订阅（跳过初始状态）
ins.updates.a.subscribe
ins.fullUpdate.subscribe
```

5. 状态模型销毁

销毁模型，会自动取消订阅，阻止后续 setState 修改状态。
```js
ins.destroy();
```

### 安全性设计
1. 防止直接通过 `.state` 修改状态
```js
ins.state  // -> 返回一个 readonly proxy
```

### 高级能力
1. action、reducer。

经过长期的实践，直接使用 setState 修改状态不是一个好的习惯。将对模型的操作以 action 的形式进行封装，并在类内部实现类似 redux 的 reducer 是一个好的主意，这也是为什么创建状态用的是 `new State(...)`，因为你需要扩展它来实现你的业务逻辑。

```js
class MyState extends State {
    constructor(...args){
        super(...args);

        this.setReducer(this.reducer)
    }

    private reducer(state, action){
        switch(action.type){
            case 'add':
                return {
                    ...state,
                    a: state.a + action.payload.value
                }
            default:
                return state;
        }
    }
}

const ins = new MyState({
    a: 1,
    b: 'hello'
})

ins.dispatch({
    type: 'add',
    payload: {
        value: 1
    }
});

// 或者基于 Proxy dispatch 实现 
ins.dispatch.add({ value: 1 })
```

以 rxjs 的流来处理输入在实践中也是一个不错的选择，在类内可以访问到 actions 流，可以通过 subscribe 来订阅输入事件。

```js
class{
    constructor(...args){
        super(...args);
        this.init();
    }
    init(){
        this.actions.add.subscribe(({value}) => {
            this.setState({
                a: this.state.a + value
            })
        })
    }
}

```

2. event 输出事件

就像 actions 用于输入事件流，也需要输出事件用于告知外部调用方这个状态模型发生了什么，区别于状态，事件是瞬时的、不保持的。

```js
class MyState extends State {
    constructor(...args){
        super(...args);
    }
    doSomething(){
        this.emit('someEventName', { info: 'some message'})
    }
}

const ins = new MyState({
    a: 1,
    b: 'hello'
})

ins.events.someEventName.subscribe(({ info }) => console.log({ info }))

ins.doSomething(); // log: { info: 'some message' }

```

3. 副作用管理

状态实例通常代表了你的一个业务实体，在业务实体内部，可能会有一些副作用，比如请求、异步操作、订阅事件、定时器等，这些副作用需要在状态实例内部进行管理，而不是在业务实体外部进行管理。

```js
class ...{

    init(){
        this.runEffect( ()=>{
            const t = setInterval(()=>{
                this.setState({
                    a: this.state.a + 1
                })
            }, 1000);
            return () => {
                clearInterval(t);
            }
        })
    }
}

// 调用状态实例的 destroy 方法会销毁副作用
// ins.destroy() 
```




### 观测、调试能力

### 工程设计
TypeScript