# 发展历史

React 发展至今，从 16.8 发布 Hook 新增特性，依据渐进策略，保持 React 原有 API、功能不变的基础上，不断逐步发展至如今的 v18.2.0。

接下来，我们将从 React 设计原理的方向，依次分析从 v16 ~ v18 的过程中，React 究竟做了哪些迭代更新

## React 的本质

在我的理解中，不管是什么框架，本质上都是为开发者提供了便捷，高效的工作方式，从统一开发理念，代码设计模式的角度，设计出一款能够满足团队协同开发，代码风格统一管理，渲染性能出色优秀的前端框架。

就拿 Vue 和 React 来说，本质上可以将他们的工作方式分为两个维度 视图 + 响应。

UI 视图的部分，负责对接 dom，去做实际发生到页面上的渲染。

响应系统的部分，负责实现前端 UI 中的数据联动。

在 UI 视图上，vue 基于模板语法，react 基于 JSX

在响应系统上，vue 基于 proxy 封装拦截数据进行响应，react 通过维护静态状态，维护不同场景下触发状态更新的 Update 对象进行相应。

那我们本身也可以引入状态管理方案，不管是 Mobx 还是 Redux，Rxjs，就比如，在 React 中可以使用 Mobx 管理页面数据，利用 makeAutoObservable 来模仿 Vue 中的 reactive Api 生成 proxy 数据，亦或者使用 Mobx 提供的 useLocalObservable 来替换 useState 的 hook。

当然不同的框架其实不仅仅是这些，他们在实际的工作中，会对我们开发的产品提供更好的性能（虚拟 DOM 优化，DIFF 算法等），提供更好的解决方案（编程思想，技术生态），本人也是在不断地学习过程中，以上总结纯属自我理解，欢迎大家的交流分享。