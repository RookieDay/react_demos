View： 视图层
Action（动作）：视图层发出的消息（比如mouseClick）
Dispatcher（派发器）：用来接收Actions、执行回调函数
Store（数据层）：用来存放应用的状态，一旦发生变动，就提醒Views要更新页面

- Flux 的最大特点，就是数据的"单向流动"。
    1.用户访问 View
    2.View 发出用户的 Action
    3.Dispatcher 收到 Action，要求 Store 进行相应的更新
    4.Store 更新后，发出一个"change"事件
    5.View 收到"change"事件后，更新页面
上面过程中，数据总是"单向流动"，任何相邻的部分都不会发生数据的"双向流动"。这保证了流程的清晰。