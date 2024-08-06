# tech-list
> 包含我的技术栈，我喜欢使用的工具，保持更新

## 语言基础
- JavaScript
  - https://zh.javascript.info/
- CSS
  - 文档索引：https://css-tricks.com/ ,  https://cssreference.io/
  - [张鑫旭博客](https://www.zhangxinxu.com/wordpress/category/css/)，大概是全国最懂 css 的人了，内容很不错
- HTML：https://htmlreference.io/
- 综合文档： https://developer.mozilla.org
- TypeScript，工程化必备。
  - 官网 https://www.typescriptlang.org/
  - 类型挑战 https://github.com/type-challenges/type-challenges
  - [ttypescript](https://www.npmjs.com/package/ttypescript)
- AssemblyScript，ts 子集，可以编译成 wasm。 https://www.assemblyscript.org/

## 工具库
- [lodash](https://lodash.com/)，数据操作
- [dayjs](https://day.js.org/), [date-fns](https://date-fns.org/)，日期操作
- [promise-funs](https://github.com/sindresorhus/promise-fun)，提供了独立的 promise 工具
- [rxjs](https://rxjs.dev/guide/overview)，异步数据流操作，🚀 强烈推荐学习，totally change your life.
- [localforage](https://localforage.github.io/localForage/), [idb](https://github.com/jakearchibald/idb), [daixie](https://dexie.org/) indexedDB 存储

## React
- React 官网 https://react.dev/
- Dan 的博客 https://overreacted.io/
- Hook
  - 常用工具 hook，[react-use](https://github.com/streamich/react-use), [ahook](https://ahooks.js.org)
  - 专业的请求hook，[swr](https://swr.vercel.app/), [react-query](https://tanstack.com/query/latest/docs/framework/react/overview)
  - 其他
    - [observable-hook](https://observable-hooks.js.org/)，接入 rxjs 的最佳姿势
- 模式
  - [react pattern](./pattern.md)
- 优化
  - TODO
- 状态管理
  - [redux-toolkit](https://redux-toolkit.js.org/introduction/getting-started)，redux 的最佳实践。 
  - [mobx](https://mobx.js.org/README.html)，可变对象响应式。
  - context: [unstated-next](https://github.com/jamiebuilds/unstated-next), [use-context-selector](https://github.com/dai-shi/use-context-selector), [react-tracked](https://github.com/dai-shi/react-tracked)。
  - [zustand](https://zustand-demo.pmnd.rs/), [valtio](https://valtio.pmnd.rs/), [jotai](https://jotai.org/)，同一个作者，小巧精致。
  - 可选方案很多，各有优劣，实际项目中我用的是我自己造的。
- 组件库
  - [MUI](https://mui.com/core/)，YYDS。
  - [antd](https://ant.design/components/overview-cn/)，阿里出品的中后台组件库。
  - [shadcn](https://ui.shadcn.com/docs)，可以自己定制，很nice。
- 框架
  - [nextjs](https://nextjs.org/)
  - [remix](https://remix.run/)
- 可视化组件库：
  - echarts, chartjs, recharts, antv, visx, gojs, d3
- 交互, 动画
  - [anime.js](https://animejs.com/)，动画工具函数
  - [framer-motion](framer-motion) ，声明式的动画组件库
  - [react-spring](https://www.react-spring.dev/) 弹簧动画 hook
  - [use-gesture](https://use-gesture.netlify.app/) 手势库，可组合多种事件做交互，通常结合 react-spring 使用
  - [react-dnd](https://react-dnd.github.io/react-dnd/)，[react-beautiful-dnd](https://github.com/atlassian/react-beautiful-dnd)，[react-grid-layout](https://github.com/react-grid-layout/react-grid-layout) 拖拽交互, 布局
  - [React-Splitters](https://github.com/martinnov92/React-Splitters)，[golden-layout](https://golden-layout.com/) 分割面板
  - lottie动画，https://github.com/airbnb/lottie-web
- 实用组件（没啥好的分类，就单独列举了）
  - [react-activation](https://github.com/CJY0208/react-activation)，实现了类似 vue 的 <keep-alive>
  - [react-select](https://react-select.com/home)，很精致, 丰富, 可定制的 select 组件
- 文档建设
  - [Gatsby](https://www.gatsbyjs.org/docs/)
  - [Docusaurus](https://docusaurus.io/)
  - [Storybook](https://storybook.js.org/)

## 模式
- 设计模式
- 架构

## 微前端
- module federation，模块联邦首选方案
- micro-app
- qiankun
- wujie

## 构建工具
- webpack
- rspack
- parcel
- vite
- esbuild、tsup
- swc
- rollup、tsdx

## 测试
- jest
- react-testing-library
- vitest
- playwright
- cypress

## 监控
- TODO
  
## 性能优化
- Script
- CSS
- WASM
- WebGPU
- SSR

## Git
- TODO