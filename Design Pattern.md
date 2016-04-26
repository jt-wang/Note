# Design Pattern

* [Design Pattern](#design-pattern)
  * [OO 基础](#oo-%E5%9F%BA%E7%A1%80)
  * [OO 原则](#oo-%E5%8E%9F%E5%88%99)
  * [OO 模式](#oo-%E6%A8%A1%E5%BC%8F)
	* [策略模式（The Strategy Pattern）](#%E7%AD%96%E7%95%A5%E6%A8%A1%E5%BC%8Fthe-strategy-pattern)
	* [观察者模式（The Observer Pattern）](#%E8%A7%82%E5%AF%9F%E8%80%85%E6%A8%A1%E5%BC%8Fthe-observer-pattern)
	  * [Java 中的观察者模式](#java-%E4%B8%AD%E7%9A%84%E8%A7%82%E5%AF%9F%E8%80%85%E6%A8%A1%E5%BC%8F)
	* [装饰者模式（The Decorator Pattern）](#%E8%A3%85%E9%A5%B0%E8%80%85%E6%A8%A1%E5%BC%8Fthe-decorator-pattern)
	  * [Java I/O](#java-io)
	* [工厂模式（The Factory Pattern）](#%E5%B7%A5%E5%8E%82%E6%A8%A1%E5%BC%8Fthe-factory-pattern)
	  * [简单工厂（Simple Factory）](#%E7%AE%80%E5%8D%95%E5%B7%A5%E5%8E%82simple-factory)
	  * [工厂方法模式（The Factory Method Pattern）](#%E5%B7%A5%E5%8E%82%E6%96%B9%E6%B3%95%E6%A8%A1%E5%BC%8Fthe-factory-method-pattern)
	  * [抽象工厂模式（The Abstract Factory Pattern）](#%E6%8A%BD%E8%B1%A1%E5%B7%A5%E5%8E%82%E6%A8%A1%E5%BC%8Fthe-abstract-factory-pattern)
	* [单例模式（The Singleton Pattern）](#%E5%8D%95%E4%BE%8B%E6%A8%A1%E5%BC%8Fthe-singleton-pattern)
	  * [简单但低效的多线程版本](#%E7%AE%80%E5%8D%95%E4%BD%86%E4%BD%8E%E6%95%88%E7%9A%84%E5%A4%9A%E7%BA%BF%E7%A8%8B%E7%89%88%E6%9C%AC)
	  * [不用延迟实例化（lazy instantiaze）的版本](#%E4%B8%8D%E7%94%A8%E5%BB%B6%E8%BF%9F%E5%AE%9E%E4%BE%8B%E5%8C%96lazy-instantiaze%E7%9A%84%E7%89%88%E6%9C%AC)
	  * [“双重检查加锁”版本](#%E5%8F%8C%E9%87%8D%E6%A3%80%E6%9F%A5%E5%8A%A0%E9%94%81%E7%89%88%E6%9C%AC)
	* [命令模式（The Command Pattern）](#%E5%91%BD%E4%BB%A4%E6%A8%A1%E5%BC%8Fthe-command-pattern)
	  * [命令模式的其他用途](#%E5%91%BD%E4%BB%A4%E6%A8%A1%E5%BC%8F%E7%9A%84%E5%85%B6%E4%BB%96%E7%94%A8%E9%80%94)
		* [队列请求（queuing requests）](#%E9%98%9F%E5%88%97%E8%AF%B7%E6%B1%82queuing-requests)
		* [日志请求（logging requests）](#%E6%97%A5%E5%BF%97%E8%AF%B7%E6%B1%82logging-requests)
	* [适配器模式与外观模式](#%E9%80%82%E9%85%8D%E5%99%A8%E6%A8%A1%E5%BC%8F%E4%B8%8E%E5%A4%96%E8%A7%82%E6%A8%A1%E5%BC%8F)


笔记基于 [Head First Design Patterns](http://www.headfirstlabs.com/books/hfdp/)

## OO 基础
- 抽象
- 封装
- 多态
- 继承

## OO 原则
- 封装变化
- 多用组合，少用继承
- 针对接口编程，不针对实现编程
- 尽量在交互对象之间使用松耦合设计
- 对扩展开放，对修改关闭
- 依赖倒置原则（Dependency Inversion Principle）：要依赖抽象，不要依赖具体类

## OO 模式
### 策略模式（The Strategy Pattern）
定义算法族，分别封装起来，让它们之间可以相互替换，此模式让算法的变化独立于使用算法的客户。

### 观察者模式（The Observer Pattern）
定义了对象之间的一对多依赖，这样一来，当一个对象改变状态时，它的所有依赖者都会收到通知并自动更新。<br>
![Observer Pattern](/Design Pattern/Observer Pattern.png)
#### Java 中的观察者模式
- java.util package 中包含 Observer 接口和 Observable 类
- `notifyObservers(Object arg)` 可以设置使用 push 或 pull（无参数）的方式传送数据
- 在调用`notifyObservers()`之前，要先调用`setChanged()`来指示状态已经改变
- Swing 大量使用观察者模式

### 装饰者模式（The Decorator Pattern）
动态地将责任附加到对象上。若要扩展功能，装饰者提供了比继承更有弹性的替代方案。<br>
缺点：利用装饰者模式，常常造成设计中有大量的小类。<br>
![Decorator Pattern](/Design Pattern/Decorator Pattern.png)
#### Java I/O
![Java I/O](/Design Pattern/Java I_O.png)

### 工厂模式（The Factory Pattern）
所有的工厂都是用来封装对象的创建；所有工厂模式都通过减少应用程序和具体类之间的依赖促进松耦合。
#### 简单工厂（Simple Factory）
![Simple Factory](/Design Pattern/Simple Factory.png)
#### 工厂方法模式（The Factory Method Pattern）
定义了一个创建对象的接口，但由子类决定要实例化的类是哪一个。工厂方法让类把实例化推迟到子类。<br>
![Factory Method Pattern](/Design Pattern/Factory Method Pattern.png)
#### 抽象工厂模式（The Abstract Factory Pattern）
提供一个接口，用于创建相关或依赖对象的家族，而不需要明确指定具体类。<br>
![Abstract Factory Pattern](/Design Pattern/Abstract Factory Pattern.png)

### 单例模式（The Singleton Pattern）
确保一个类只有一个实例，并提供一个全局访问点。<br>
在Java中实现单例模式需要私有的构造器、一个静态方法和一个静态变量。
#### 简单但低效的多线程版本
``` java
public class Singleton {
	private static Singleton uniqueInstance;

	private Singleton() {}

	public static synchronized Singleton getInstance() {
		if (uniqueInstance == null) {
			uniqueInstance = new Singleton();
		}
		return uniqueInstance;
	}
}
```
#### 不用延迟实例化（lazy instantiaze）的版本
``` java
public class Singleton {
	private static Singleton uniqueInstance = new Singleton();

	private Singleton() {}

	public static Singleton getInstance() {
		return uniqueInstance;
	}
}
```
#### “双重检查加锁”版本
``` java
public class Singleton {
	private volatile static Singleton uniqueInstance;

	private Singleton() {}

	public static Singleton getInstance() {
		if (uniqueInstance == null) {
			synchronized (Singleton.class) {
				if (uniqueInstance == null) {
					uniqueInstance = new Singleton();
				}
			}
		}
		return uniqueInstance;
	}
}
```

### 命令模式（The Command Pattern）
将“请求”封装成对象，以便使用不同的请求、队列或者日志来参数化其他对象。命令模式也支持可撤销的操作。<br>
命令模式将发出请求的对象和执行请求的对象解耦。在被解耦的两者之间是通过命令对象进行沟通的，命令对象封装了接收者和一个或一组动作。调用者通过调用命令对象的execute()发出请求，这会使得接收者的动作被调用。调用者可以接受命令当作参数，甚至在运行时动态地进行。<br>
![The Command Pattern](/Design Pattern/The Command Pattern.png) <br>
**其他**
- NoCommand对象是一个空对象（null object）的例子
- 命令撤销：实现undo()方法来回到execute()被执行前的状态。（多层次的撤销：使用堆栈记录所有状态）
- 宏命令：允许调用多个命令

#### 命令模式的其他用途
##### 队列请求（queuing requests）
工作队列类和进行计算的对象之间完全是解耦的。<br>
命令 --> 实现命令接口的对象被放进队列 --> 这样能有效地把运算限制在固定数目的线程中进行 --> 线程从队列中一个个地删除命令对象，然后调用命令对象的execute()方法。一旦完成，就会再去处理下一个新的命令对象。
##### 日志请求（logging requests）
通过使用记录日志，我们可以将上次检查点（checkpoint）之后的所有操作记录下来，如果系统出状况，从检查点开始应用这些操作。（store()和load()方法）
比方说，对于电子表格应用，我们可能想要实现的错误恢复方式是将电子表格的操作记录在日志中，而不是每次电子表格一有变化就纪录整个电子表格。

### 适配器模式与外观模式
