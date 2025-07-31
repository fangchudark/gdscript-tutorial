# 行为型模式

> 怎么在对象之间通信，优雅地完成任务

关注的是如何让多个对象之间**优雅地协作完成某个任务**，而不是一锅炖地互相调用得乱七八糟

举个例子：

* 你是一个“角色状态机”，不同状态之间怎么切换？

* 你是个“UI按钮”，点击后要通知谁？谁来响应？

* 你在做日志系统，怎么统一调度每条日志？

这些，都属于“**行为如何组织**”的问题，而不是“结构怎么搭”、“对象如何创建”。



# 11个行为型模式

* [责任链（Chain of Responsibility）](10.7.3.1.chain-of-responsibility.md)：多个处理者排成一列，按顺序处理请求

* [命令（Command）](10.7.3.2.command-pattern.md)：将请求封装为命令对象，支持撤销、记录、延迟等操作

* [解释器（Interpreter）](10.7.3.3.interpreter-pattern.md)：用于构建简单的解释器（如逻辑表达式、公式）（较少使用）。

* [迭代器（Iterator）](10.7.3.4.iterator-pattern.md)：统一集合遍历方式，封装内部结构

* [中介者（Mediator）](10.7.3.5.mediator-pattern.md)：用中心化对象管理多个对象之间的交互

* [备忘录（Memento）](10.7.3.6.memento-pattern.md)：保存对象状态以支持撤销、恢复等操作

* [观察者（Observer）](10.7.3.7.observer-pattern.md)：一改多联动，变化时通知所有订阅者

* [状态（State）](10.7.3.9.state-pattern.md)：对象状态不同行为也不同，用状态类封装变化

* [策略（Strategy）](10.7.3.8.strategy-pattern.md)：封装不同算法，按需动态选择

* [模板方法（Template Method）](10.7.3.10.template-method-pattern.md)：定义流程骨架，子类决定某些步骤

* [访问者（Visitor）](10.7.3.11.visitor-pattern.md)：把“对数据的操作”封装在访问者里
