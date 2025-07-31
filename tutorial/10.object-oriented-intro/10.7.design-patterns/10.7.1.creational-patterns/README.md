# 创建型模式

> 「我想要一个对象，但我不想每次都`new`得那么死板，我想**优雅地、可控地、有弹性地**创造它！」

创建型设计模式的目标是

* 把对象的**创建过程“封装”起来**

* 提供**更灵活、可扩展**的创建方式

* 避免代码到处`new`，提升可维护性



# 五个创建型模式

* [单例（Singleton）](10.7.1.1.singleton-pattern.md)：确保一个类只有一个实例，提供全局访问点。

* [工厂方法（Factory Method）](10.7.1.2.factory-method.md)：由子类决定创建哪个对象。

* [抽象工厂（Abstract Factory）](10.7.1.3.abstract-factory.md)：创建相关对象的家族。

* [建造者（Builder）](10.7.1.4.builder-pattern.md)：分步骤构建复杂对象。

* [原型（Prototype）](10.7.1.5.prototype-pattern.md)：通过克隆现有对象创建新对象。
