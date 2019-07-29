## redux-saga

### 介绍：
  在 redux-saga 的世界里，所有的任务都通用 yield Effects 来完成（Effect 可以看作是 redux-saga 的任务单元）

----
### 名词释义：
#### Effect：
一个 effect 就是一个 Plain Object JavaScript 对象，包含一些将被 saga middleware 执行的指令。使用 redux-saga 提供的工厂函数来创建 effect。一个 Saga 所做的实际上是组合那些所有的 Effect，共同实现所需的控制流。 最简单的例子是直接把 yield 一个接一个地放置来对序列化 yield Effect。你也可以使用熟悉的控制流操作符（if, while, for） 来实现更复杂的控制流。

----
### 核心API:
- Saga 辅助函数:
  - takeEvery
    - 允许多个实例同时启动
  - takeLatest
    - 在任何时刻 takeLatest 只允许执行一个任务，并且这个任务是最后被启动的那个，如果之前已经有一个任务在执行，那之前的这个任务会自动被取消
- Effect Creators
  - take(pattern)
    - take函数可以理解为监听未来的action，它创建了一个命令对象，告诉middleware等待一个特定的action， Generator会暂停，直到一个与pattern匹配的action被发起，才会继续执行下面的语句，也就是说，take是一个阻塞的 effect。take 让我们通过全面控制 action 观察进程来构建复杂的控制流成为可能。
  - put(action)
    - put函数是用来发送action的 effect，你可以简单的把它理解成为redux框架中的dispatch函数，当put一个action后，reducer中就会计算新的state并返回，注意： put 也是阻塞 effect
  - call(fn, …args)
    - call函数你可以把它简单的理解为就是可以调用其他函数的函数，它命令 middleware 来调用fn 函数， args为函数的参数，注意： fn 函数可以是一个 Generator 函数，也可以是一个返回 Promise 的普通函数，call 函数也是阻塞 effect
  - select(selector, …args)
    - select 函数是用来指示 middleware调用提供的选择器获取Store上的state数据，你也可以简单的把它理解为redux框架中获取store上的 state数据一样的功能 ：store.getState()
  - fork(fn, …args)
    - fork 函数和 call 函数很像，都是用来调用其他函数的，但是fork函数是非阻塞函数，也就是说，程序执行完 yield fork(fn， args) 这一行代码后，会立即接着执行下一行代码语句，而不会等待fn函数返回结果后，在执行下面的语句
  - cancel(task)
    - 一旦任务被 fork，可以使用 yield cancel(task) 来中止任务执行，使用 yield cancelled() 来检查 Generator 是否已经被取消。取消正在运行的任务。取消接口请求（race也可以实现类似取消功能）
- createSagaMiddleware()
  - createSagaMiddleware 函数是用来创建一个 Redux 中间件，将 Sagas 与 Redux Store 链接起来。sagas 中的每个函数都必须返回一个 Generator 对象，middleware 会迭代这个 Generator 并执行所有 yield 后的 Effect（Effect 可以看作是 redux-saga 的任务单元）
- middleware.run(sagas, …args)
  - 动态执行sagas，用于applyMiddleware阶段之后执行sagas

----
### 错误处理：
我们可以使用熟悉的 try/catch 语法在 Saga 中捕获错误。

----
### 示例项目:
* 💯[tiger-react-cli](https://github.com/TigerHee/tiger-react-cli)