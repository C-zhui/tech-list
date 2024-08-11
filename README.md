# tech-list
> 包含我的技术栈, 我喜欢使用的工具, 保持更新

## 语言基础
- JavaScript
  - https://zh.javascript.info/
- CSS
  - 文档索引：https://css-tricks.com/ ,  https://cssreference.io/
  - [张鑫旭博客](https://www.zhangxinxu.com/wordpress/category/css/), 大概是全国最懂 css 的人了, 内容很不错
- HTML：https://htmlreference.io/
- 综合文档： https://developer.mozilla.org
- TypeScript, 工程化必备 
  - 官网 https://www.typescriptlang.org/
  - 类型挑战 https://github.com/type-challenges/type-challenges
  - [ttypescript](https://www.npmjs.com/package/ttypescript)
- [AssemblyScript](https://www.assemblyscript.org/), ts 子集, 可以编译成 wasm  

## 工具库
- [lodash](https://lodash.com/), 数据操作
- [dayjs](https://day.js.org/), [date-fns](https://date-fns.org/), 日期操作
- [promise-funs](https://github.com/sindresorhus/promise-fun), 提供了独立的 promise 工具
- [rxjs](https://rxjs.dev/guide/overview), 异步数据流操作, 响应式编程的通用方案, 🚀 强烈推荐学习, 
- [async](https://caolan.github.io/async/v3/), 异步流程控制, 比较老, 不推荐, rxjs 更好用 
- [localforage](https://localforage.github.io/localForage/), [idb](https://github.com/jakearchibald/idb), [daixie](https://dexie.org/) indexedDB 存储
- [jsonata](https://jsonata.org/), 数据处理
- [axios](https://axios-http.com/docs/intro), [ky](https://github.com/sindresorhus/ky), [alova](https://alova.js.org/) 请求库
- tapable-ts 插件化

## React
- React 官网 https://react.dev/
- Dan 的博客 https://overreacted.io/
- 常用工具 hook, [react-use](https://github.com/streamich/react-use), [ahook](https://ahooks.js.org)

- 状态管理
  - [react-router](https://reactrouter.com)，路由状态管理
  - [redux-toolkit](https://redux-toolkit.js.org/introduction/getting-started), redux 的最佳实践
  - [mobx](https://mobx.js.org/README.html), 可变对象响应式 
  - 基于 context
    -  [unstated-next](https://github.com/jamiebuilds/unstated-next)
    -  [use-context-selector](https://github.com/dai-shi/use-context-selector)
    -  [react-tracked](https://github.com/dai-shi/react-tracked)
  - [zustand](https://zustand-demo.pmnd.rs/), [valtio](https://valtio.pmnd.rs/), [jotai](https://jotai.org/), 同一个作者, 小巧精致
  - [swr](https://swr.vercel.app/), [react-query](https://tanstack.com/query/latest/docs/framework/react/overview), 异步状态管理
  - [observable-hook](https://observable-hooks.js.org/), 接入 rxjs 的最佳姿势
  - 可选方案很多, 各有优劣, 实际项目中通常需要组合各种技术, [状态管理](./state-management/state-management.md)、[设计一个状态管理工具](./state-management/a-state-management-design.md)

- CSS方案
  - [BEM](https://getbem.com/), 朴素的 css 命名方案
  - [css modules](https://github.com/css-modules/css-modules), 将自动 hash 的类名与 js 对象绑定，再也不用担心类名冲突了
  - [tailwindcss](https://tailwindcss.com/), [unocss](https://unocss.dev/), 原子类，用起来很方便，但是 dom 结构很冗长
  - [emotion](https://emotion.sh/docs/@emotion/react), css in js, 运行时动态生成样式类，缓存复用
  - [mui system](https://mui.com/system/getting-started/), css in js, 同 emotion, 样式简写、定制主题
  - [cva](https://cva.style/docs/getting-started/variants), 根据状态组合类名，可以结合 tailwindcss 组合出样式

- 组件库
  - [MUI](https://mui.com/core/), 世界级的UI组件库
  - [antd](https://ant.design/components/overview-cn/), 阿里旗下 
  - [semi](https://semi.design/), 抖音旗下 
  - [shadcn](https://ui.shadcn.com/docs), CV大法好, 可以自己定制是亮点

- 框架
  - [nextjs](https://nextjs.org/)
  - [remix](https://remix.run/)

- 可视化库：
  - [echarts](https://www.echartsjs.com/zh/index.html), [chartjs](https://www.chartjs.org/), [recharts](http://recharts.org/en-US/), [antv](https://antv.antgroup.com/), [visx](https://airbnb.io/visx/), [gojs](https://gojs.net/latest/index.html), [d3](https://d3js.org/)

- 交互, 动画
  - [anime.js](https://animejs.com/), 动画工具函数
  - [framer-motion](framer-motion) , 声明式的动画组件库
  - [react-spring](https://www.react-spring.dev/) 弹簧动画 hook
  - [use-gesture](https://use-gesture.netlify.app/) 手势库, 可组合多种事件做交互, 通常结合 react-spring 使用
  - [react-dnd](https://react-dnd.github.io/react-dnd/), [react-beautiful-dnd](https://github.com/atlassian/react-beautiful-dnd), [react-grid-layout](https://github.com/react-grid-layout/react-grid-layout) 拖拽交互, 布局
  - [React-Splitters](https://github.com/martinnov92/React-Splitters), [golden-layout](https://golden-layout.com/) 分割面板
  - [lottie](https://github.com/airbnb/lottie-web) 动画
  - [canvas-confetti](https://www.npmjs.com/package/canvas-confetti), 礼炮效果

- 实用组件（没啥好的分类, 就单独列举了）
  - [react-activation](https://github.com/CJY0208/react-activation), 实现了类似 vue 的 \<keep-alive\> 组件，但是与 react 18 并发模式不兼容
  - [react-select](https://react-select.com/home), 很精致, 丰富, 可定制的 select 组件
  - 表单方案, react-hook-form, formik, formily
  - 更多 https://github.com/brillout/awesome-react-components
  
- 优化
  - TODO
  - react 18, batch update
  - react 19 compiler

- 模式、技巧
  - https://www.patterns.dev/react
  

- 文档
  - [Gatsby](https://www.gatsbyjs.org/docs/)
  - [Docusaurus](https://docusaurus.io/)
  - [Storybook](https://storybook.js.org/)
- code playground
  - [codesandbox](https://codesandbox.io/)
  - [stackblitz](https://stackblitz.com/)
  - [replit](https://replit.com)

## 模式
- 设计模式
  - https://www.patterns.dev/
  - https://refactoringguru.cn/design-patterns
  - https://www.tutorialspoint.com/design_pattern/index.htm
  - [MVC](https://developer.mozilla.org/en-US/docs/Glossary/MVC)
- 架构模式
  - [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- Design system
  - [什么是设计系统](https://pixso.cn/designskills/what-is-a-design-system/)

## 微前端
- [module federation](https://module-federation.io/), 模块联邦首选方案
- [micro-app](https://micro-zoe.github.io/micro-app/)
- [qiankun](https://qiankun.umijs.org/zh/guide)
- [wujie](https://github.com/Tencent/wujie)

## 构建工具
- [webpack](https://webpack.js.org/)
- [rspack](https://rspack.dev/), [rsbuild](https://rsbuild.dev/)
- [parcel](https://parceljs.org/)
- [vite](https://vitejs.dev/)
- [esbuild](https://esbuild.github.io/), [tsup](https://tsup.egoist.dev/)
- [swc](https://swc.rs/)
- [rollup](https://rollupjs.org/), [tsdx](https://tsdx.io/)
- [rolldown](https://rolldown.rs/)

## 测试
- [jest](https://jestjs.io/)
- [react-testing-library](https://testing-library.com/docs/react-testing-library/intro/)
- [vitest](https://vitest.dev/)
- [playwright](https://playwright.dev/)
- [cypress](https://www.cypress.io/)

## 监控
- TODO

## 性能优化
- [web.dev](https://web.dev/explore), 这个网站上有系列的文章讲性能优化
- Script
- CSS
- WASM
- WebGPU

## Git
- https://git-scm.com/book/en/v2

## 算法

## 常用链接
- Awesomes
  - https://github.com/sorrycc/awesome-javascript
  - https://github.com/enaqx/awesome-react
  - https://github.com/sindresorhus/awesome-nodejs
  - https://github.com/tayllan/awesome-algorithms
  - https://github.com/sindresorhus/awesome