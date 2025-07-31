# GDScript 中文教程

GDScript 是 Godot 引擎专用的脚本语言。  
本仓库将带你从基础代码框架入门，逐步掌握 GDScript 的语法，学习面向对象编程，并提供丰富的实战示例。

目录
---

- ## 基础概念
  - [预测试](tutorial/1.pre-test.md)
  - [初识代码结构](tutorial/2.introduction-to-code-structure.md)

- ## [变量与基本数据类型](tutorial/3.variables-and-basic-data-types/README.md)
  - [变量](tutorial/3.variables-and-basic-data-types/3.1.variables.md)
  - [基本数据类型](tutorial/3.variables-and-basic-data-types/3.2.basic-data-types.md)
  - [类型转换](tutorial/3.variables-and-basic-data-types/3.3.type-conversion.md)
  - [算术和位运算符](tutorial/3.variables-and-basic-data-types/3.4.arithmetic-and-bitwise-operators.md)

- ## [分支语句和常量](tutorial/4.branch-statements-and-constants/README.md)
  - [条件表达式](tutorial/4.branch-statements-and-constants/4.1.conditional-expressions.md)
  - [if-else-elif语句](tutorial/4.branch-statements-and-constants/4.2.if-else-elif.md)
  - [常量和枚举](tutorial/4.branch-statements-and-constants/4.3.constants-and-enums.md)
  - [match语句](tutorial/4.branch-statements-and-constants/4.4.match-statement.md)

- ## [循环语句](tutorial/5.loop-statements/README.md)
  - [while循环](tutorial/5.loop-statements/5.1.while-loop.md)
  - [for循环](tutorial/5.loop-statements/5.2.for-loop.md)
  - [跳转语句](tutorial/5.loop-statements/5.3.jump-statements.md)

- ## [函数](tutorial/6.functions.md)

- ## [集合](tutorial/7.collections/README.md)
  - [数组](tutorial/7.collections/7.1.array.md)
    - [API文档摘要](tutorial/7.collections/api-docs-summary/array.md)
  - [紧缩数组](tutorial/7.collections/7.2.packed-array.md)
    - [API文档摘要](tutorial/7.collections/api-docs-summary/packed-array.md)
  - [字典](tutorial/7.collections/7.3.dictionary.md)
    - [API文档摘要](tutorial/7.collections/api-docs-summary/dictionary.md)

- ## [可调用体](tutorial/8.callable.md)

- ## [信号](tutorial/9.signals.md)

- ## [面向对象入门](tutorial/10.object-oriented-intro/README.md)
  - [类](tutorial/10.object-oriented-intro/10.1.class.md)
  - [对象](tutorial/10.object-oriented-intro/10.2.object.md)
  - [静态成员](tutorial/10.object-oriented-intro/10.3.static-members.md)
  - [继承](tutorial/10.object-oriented-intro/10.4.inheritance.md)
  - [多态](tutorial/10.object-oriented-intro/10.5.polymorphism.md)
  - ## [设计原则](tutorial/10.object-oriented-intro/10.6.design-principles/README.md)
    - [单一职责原则](tutorial/10.object-oriented-intro/10.6.design-principles/10.6.1.single-responsibility-principle.md)
    - [开闭原则](tutorial/10.object-oriented-intro/10.6.design-principles/10.6.2.open-closed-principle.md)
    - [里氏替换原则](tutorial/10.object-oriented-intro/10.6.design-principles/10.6.3.liskov-substitution-principle.md)
    - [接口隔离原则](tutorial/10.object-oriented-intro/10.6.design-principles/10.6.4.interface-segregation-principle.md)
    - [依赖倒置原则](tutorial/10.object-oriented-intro/10.6.design-principles/10.6.5.dependency-inversion-principle.md)
    - [迪米特法则](tutorial/10.object-oriented-intro/10.6.design-principles/10.6.6.law-of-demeter.md)
    - [组合优于继承](tutorial/10.object-oriented-intro/10.6.design-principles/10.6.7.composition-over-inheritance.md)

  - ### [设计模式](tutorial/10.object-oriented-intro/10.7.design-patterns/README.md)
  
    - #### [创建型模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.1.creational-patterns/README.md)
      - [单例模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.1.creational-patterns/10.7.1.1.singleton-pattern.md)
      - [工厂方法](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.1.creational-patterns/10.7.1.2.factory-method.md)
      - [抽象工厂](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.1.creational-patterns/10.7.1.3.abstract-factory.md)
      - [建造者模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.1.creational-patterns/10.7.1.4.builder-pattern.md)
      - [原型模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.1.creational-patterns/10.7.1.5.prototype-pattern.md)

    - #### [结构型模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/README.md)
      - [适配器模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/10.7.2.1.adapter-pattern.md)
      - [桥接模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/10.7.2.2.bridge-pattern.md)
      - [装饰器模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/10.7.2.3.decorator-pattern.md)
      - [代理模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/10.7.2.4.proxy-pattern.md)
      - [外观模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/10.7.2.5.facade-pattern.md)
      - [享元模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/10.7.2.6.flyweight-pattern.md)
      - [组合模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.2.structural-patterns/10.7.2.7.composite-pattern.md)

    - #### [行为型模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/README.md)
      - [责任链模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.1.chain-of-responsibility.md)
      - [命令模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.2.command-pattern.md)
      - [解释器模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.3.interpreter-pattern.md)
      - [迭代器模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.4.iterator-pattern.md)
      - [中介者模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.5.mediator-pattern.md)
      - [备忘录模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.6.memento-pattern.md)
      - [状态模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.7.state-pattern.md)
      - [策略模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.8.strategy-pattern.md)
      - [观察者模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.9.observer-pattern.md)
      - [模板方法模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.10.template-method-pattern.md)
      - [访问者模式](tutorial/10.object-oriented-intro/10.7.design-patterns/10.7.3.behavioral-patterns/10.7.3.11.visitor-pattern.md)

- ## [注解](tutorial/11.annotation.md)

- ## [文档注释](tutorial/12.doc-comments.md) 

# 分享知识

欢迎你参与知识分享或修正内容，如有建议或发现错误，欢迎提交 PR！