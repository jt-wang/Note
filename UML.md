# UML

笔记基于 UML用户指南（第2版）（The Unified Modeling Language User Guide 2nd Edition）

## 基础
- 模型是对现实的简化
- 建模是为了能够更好地理解正在开发的系统
- UML是一种对软件密集型系统的制品进行下述工作的语言：可视化、详述、构造、文档化

## UML的构造块（Building Blocks of the UML）
### 事物（Things）
#### 结构事物（Structural things）
##### 类（class）
![class](./UML/class.png)
##### 接口（interface）
![interface](./UML/interface.png)
##### 协作（collaboration）
![collaboration](./UML/collaboration.png)
##### 用况（use case）
![use case](./UML/use case.png)
##### 主动类（active class）
![active class](./UML/active class.png)
##### 构件（component）
![component](./UML/component.png)
##### 制品（artifact）
![artifact](./UML/artifact.png)
##### 结点（node）
![node](./UML/node.png)

#### 行为事物（Behavioral things）
交互注重一系列相互作用的对象；状态机注重一定时间内一个对象的生命周期；活动注重步骤之间的流
##### 交互（interaction）
![interaction](./UML/interaction.png)
##### 状态机（state machine）
![state machine](./UML/state machine.png)
##### 活动（activity）
![activity](./UML/activity.png)

#### 分组事物（Grouping things）
##### 包（package）
![package](./UML/package.png)

#### 注释事物（Annotational things）
##### 注解（note）
![note](./UML/note.png)

### 关系（Relationships）
#### 依赖（dependency）
![dependency](./UML/dependency.png)
#### 关联（association）
![association](./UML/association.png)
#### 泛化（generalization）
特殊／一般关系</br>
![generalization](./UML/generalization.png)
#### 实现（realization）
接口和实现它们的类或构件之间；用况和实现它们的协作之间</br>
![realization](./UML/realization.png)

### 图（Diagrams）
#### 类图（class diagram）
#### 对象图（object diagram）
#### 构件图（component diagram）
#### 组合结构图（composite structure diagram）
#### 用狂图（use case diagram）
#### 顺序图（sequence diagram）
#### 通信图（communication diagram）
#### 状态图（state diagram）
#### 活动图（activity diagram）
#### 部署图（deployment diagram）
#### 包图（package diagram）
#### 定时图（timing diagram）
#### 交互概览图（interaction overview diagram）

## UML中的公共机制（Common Mechanisms in the UML）
### 详述（Specifications）
### 修饰（Adornments）
抽象；可见性：公共、受保护、私有</br>
![adornments](./UML/adornments.png)
### 通用划分（Common divisions）
类和对象；接口和实现；类型和角色
### 扩展机制（Extensibility mechanisms）
![extensibility mechanisms](./UML/extensibility mechanisms.png)
#### 衍型（stereotype）
如：`class Overflow`
#### 标记值（tagged value）
如：`class EventQueue`
#### 约束（constraint）
如：`{ordered}`

## 体系结构（Architecture）
![architecture](./UML/architecture.png)
### 用况视图（use case view）
静态：用况图；动态：交互图、状态图和活动图
### 设计视图（design view）
静态：类图和对象图；动态：交互图、状态图和活动图
### 交互视图（interaction view）
静态：类图和对象图；动态：交互图、状态图和活动图
### 实现视图（implementation view）
静态：构件图；动态：交互图、状态图和活动图
### 部署视图（deployment view）
静态：部署图；动态：交互图、状态图和活动图
