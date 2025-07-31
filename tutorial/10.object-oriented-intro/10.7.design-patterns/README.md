# 设计模式

面向对象设计模式（Object-Oriented Design Patterns）是解决软件设计中常见问题的可重用方案，它们基于面向对象编程（OOP）的核心思想（如封装、继承、多态），提供了一套经过验证的最佳实践。设计模式不是具体的代码，而是描述如何组织代码结构的模板，帮助开发者构建灵活、可维护和可扩展的软件系统。



> 本章节的后续内容讲解的是传统OOP的设计模式，提供了设计模式在两种语言中的示例代码模板，若要参考在Godot游戏编程中运用这些模式的方式，请直接参见 游戏编程模式 章节

***

### 核心概念

1. 模式的目标：

   * 提高代码复用性，避免重复造轮子。

   * 解耦系统组件，增强灵活性和可维护性。

   * 提供清晰的代码结构，便于团队协作。

2. 四大要素：

   * 模式名称（如工厂模式、观察者模式）便于交流。

   * 问题描述模式的适用场景。

   * 解决方案描述模式的设计与实现。

   * 效果分析模式的优缺点（如性能、复杂度）。

***

### 经典分类（GoF 23种设计模式）

《设计模式：可复用面向对象软件的基础》（GoF, 1994）将模式分为三类：

#### 1. [创建型模式（怎么造对象）](10.7.1.creational-patterns/README.md)

处理对象创建机制，解耦对象的实例化过程。

* [单例模式（Singleton）](10.7.1.creational-patterns/10.7.1.1.singleton-pattern.md)：确保一个类只有一个实例。

* [工厂方法（Factory Method）](10.7.1.creational-patterns/10.7.1.2.factory-method.md)：由子类决定创建哪个对象。

* [抽象工厂（Abstract Factory）](10.7.1.creational-patterns/10.7.1.3.abstract-factory.md)：创建相关对象的家族。

* [建造者（Builder）](10.7.1.creational-patterns/10.7.1.4.builder-pattern.md)：分步骤构建复杂对象。

* [原型（Prototype）](10.7.1.creational-patterns/10.7.1.5.prototype-pattern.md)：通过克隆现有对象创建新对象。

#### 2. [结构型模式（对象之间怎么组合）](10.7.2.structural-patterns/README.md)

关注类和对象的组合方式，形成更大的结构。

* [适配器（Adapter）](10.7.2.structural-patterns/10.7.2.1.adapter-pattern.md)：转换接口以兼容现有系统。

* [装饰器（Decorator）](10.7.2.structural-patterns/10.7.2.3.decorator-pattern.md)：动态添加职责。

* [代理（Proxy）](10.7.2.structural-patterns/10.7.2.4.proxy-pattern.md)：控制对对象的访问（如缓存、权限）。

* [组合（Composite）](10.7.2.structural-patterns/10.7.2.7.composite-pattern.md)：以树形结构处理部分-整体关系。

* [外观（Facade）](10.7.2.structural-patterns/10.7.2.5.facade-pattern.md)：简化复杂子系统的接口。

* [桥接（Bridge）](10.7.2.structural-patterns/10.7.2.2.bridge-pattern.md)：分离抽象与实现，避免继承爆炸。

* [享元（Flyweight）](10.7.2.structural-patterns/10.7.2.6.flyweight-pattern.md)：共享细粒度对象以减少内存占用。

#### 3. [行为型模式（对象之间怎么说话）](10.7.3.behavioral-patterns/README.md)

定义对象间的交互和职责分配。

* [观察者（Observer）](10.7.3.behavioral-patterns/10.7.3.9.observer-pattern.md)：一对多的依赖通知机制。

* [策略（Strategy）](10.7.3.behavioral-patterns/10.7.3.8.strategy-pattern.md)：封装可互换的算法族。

* [命令（Command）](10.7.3.behavioral-patterns/10.7.3.2.command-pattern.md)：将请求封装为对象。

* [模板方法（Template Method）](10.7.3.behavioral-patterns/10.7.3.10.template-method-pattern.md)：定义算法骨架，子类实现步骤。

* [责任链（Chain of Responsibility）](10.7.3.behavioral-patterns/10.7.3.1.chain-of-responsibility.md)：请求沿处理链传递。

* [状态（State）](10.7.3.behavioral-patterns/10.7.3.7.state-pattern.md)：通过对象状态改变行为。

* [迭代器（Iterator）](10.7.3.behavioral-patterns/10.7.3.4.iterator-pattern.md)：提供遍历集合的统一方式。

* [中介者（Mediator）](10.7.3.behavioral-patterns/10.7.3.5.mediator-pattern.md)：集中管理对象间通信。

* [备忘录（Memento）](10.7.3.behavioral-patterns/10.7.3.6.memento-pattern.md)：保存和恢复对象状态。

* [访问者（Visitor）](10.7.3.behavioral-patterns/10.7.3.11.visitor-pattern.md)：在不修改类的情况下添加操作。

* [解释器（Interpreter）](10.7.3.behavioral-patterns/10.7.3.3.interpreter-pattern.md)：为语言语法定义解释器（较少使用）。
