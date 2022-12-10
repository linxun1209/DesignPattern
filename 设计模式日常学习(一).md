# 设计模式
## 软件设计模式的概念
软件设计模式（Software Design Pattern），又称设计模式，是一套被反复使用、多数人知晓的、经过分类编目的、代码设计经验的总结。它描述了在软件设计过程中的一些不断重复发生的问题，以及该问题的解决方案。也就是说，它是解决特定问题的一系列套路，是前辈们的代码设计经验的总结，具有一定的普遍性，可以反复使用。
## 学习设计模式的必要性
设计模式的本质是面向对象设计原则的实际运用，是对类的封装性、继承性和多态性以及类的关联关系和组合关系的充分理解。
### 正确使用设计模式具有以下优点。

- 可以提高程序员的思维能力、编程能力和设计能力。
- 使程序设计更加标准化、代码编制更加工程化，使软件开发效率大大提高，从而缩短软件的开发周期。
- 使设计的代码可重用性高、可读性强、可靠性高、灵活性好、可维护性强。

## 设计模式分类

- **创建型模式**用于描述“怎样创建对象”，它的主要特点是“将对象的创建与使用分离”。GoF（四人组）书中提供了单例、原型、工厂方法、抽象工厂、建造者等 5 种创建型模式。
- **结构型模式**用于描述如何将类或对象按某种布局组成更大的结构，GoF（四人组）书中提供了代理、适配器、桥接、装饰、外观、享元、组合等 7 种结构型模式。
- **行为型模式**用于描述类或对象之间怎样相互协作共同完成单个对象无法单独完成的任务，以及怎样分配职责。GoF（四人组）书中提供了模板方法、策略、命令、职责链、状态、观察者、中介者、迭代器、访问者、备忘录、解释器等 11 种行为型模式。
# UML图
统一建模语言（Unified Modeling Language，UML）是用来设计软件的可视化建模语言。它的特点是简单、统一、图形化、能表达软件设计中的动态与静态信息。
UML 从目标系统的不同角度出发，定义了用例图、类图、对象图、状态图、活动图、时序图、协作图、构件图、部署图等 9 种图。
## 类图的概述
类图(Class diagram)是显示了模型的静态结构，特别是模型中存在的类、类的内部结构以及它们与其他类的关系等。类图不显示暂时性的信息。类图是面向对象建模的主要组成部分。
## 类图的作用

- 在软件工程中，类图是一种静态的结构图，描述了系统的类的集合，类的属性和类之间的关系，可以简化了人们对系统的理解；
- 类图是系统分析和设计阶段的重要产物，是系统编码和测试的重要模型。
## 类图表示法
### 类的表示方式
在UML类图中，类使用包含类名、属性(field) 和方法(method) 且带有分割线的矩形来表示.
属性/方法名称前加的加号和减号表示了这个属性/方法的可见性，UML类图中表示可见性的符号有三种：

- +：表示public
- -：表示private
- #：表示protected

属性的完整表示方式是： **可见性 名称 ：类型 [ = 缺省值]**
方法的完整表示方式是： **可见性 名称(参数列表) [ ： 返回类型]**
> 注意：
> 1，中括号中的内容表示是可选的
> 2，也有将类型放在变量名前面，返回值类型放在方法名前面

### 类与类之间关系的表示方式
#### 关联关系
###### **单向关联**
在UML类图中单向关联用一个带箭头的实线表示。上图表示每个顾客都有一个地址，这通过让Customer类持有一个类型为Address的成员变量类实现。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/33764834/1668322583423-48251049-8957-4e31-850e-39b9981b7e68.png#averageHue=%23f0f0f0&clientId=u3314fbe6-f385-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=120&id=u154a371f&margin=%5Bobject%20Object%5D&name=image.png&originHeight=239&originWidth=1273&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16925&status=done&style=none&taskId=u05b412b2-2583-488f-9f80-52e482514bc&title=&width=636.5)
###### **双向关联**
从上图中我们很容易看出，所谓的双向关联就是双方各自持有对方类型的成员变量。
在UML类图中，双向关联用一个不带箭头的直线表示。上图中在Customer类中维护一个List<Product>，表示一个顾客可以购买多个商品；在Product类中维护一个Customer类型的成员变量表示这个产品被哪个顾客所购买。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/33764834/1668322605649-0796b280-92c8-4de0-b078-aa765910b2c4.png#averageHue=%23f1f1f1&clientId=u3314fbe6-f385-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=128&id=ua3948e5a&margin=%5Bobject%20Object%5D&name=image.png&originHeight=256&originWidth=1312&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22139&status=done&style=none&taskId=ucaaf2bfd-1d8a-4bf2-b516-a6568ad1a04&title=&width=656)
###### **自关联**
![image.png](https://cdn.nlark.com/yuque/0/2022/png/33764834/1668322808633-4b52a074-53d5-4a33-ad96-5440466e7f91.png#averageHue=%23f2f2f2&clientId=u3314fbe6-f385-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=139&id=u17f5ab1a&margin=%5Bobject%20Object%5D&name=image.png&originHeight=278&originWidth=608&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12401&status=done&style=none&taskId=u0d97a362-11dc-4c07-9bf0-25d71df14c6&title=&width=304)
自关联在UML类图中用一个带有箭头且指向自身的线表示。上图的意思就是Node类包含类型为Node的成员变量，也就是“自己包含自己”。

#### 聚合关系
聚合关系是关联关系的一种，是强关联关系，是整体和部分之间的关系。
聚合关系也是通过成员对象来实现的，其中成员对象是整体对象的一部分，但是成员对象可以脱离整体对象而独立存在。例如，学校与老师的关系，学校包含老师，但如果学校停办了，老师依然存在。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/33764834/1668321747429-593caa63-0541-43e3-87bd-dc198695f4be.png#averageHue=%23fbfbfb&clientId=u3314fbe6-f385-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=295&id=ua7ebac51&margin=%5Bobject%20Object%5D&name=image.png&originHeight=589&originWidth=1078&originalType=binary&ratio=1&rotation=0&showTitle=false&size=104310&status=done&style=none&taskId=u56db746d-6b40-4f42-8170-b565c6c593e&title=&width=539)
#### 组合关系
![image.png](https://cdn.nlark.com/yuque/0/2022/png/33764834/1668323142399-7a19284a-bad8-45f6-9ae5-54576e469cf1.png#averageHue=%23f2f2f2&clientId=u3314fbe6-f385-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=145&id=u5a3819d6&margin=%5Bobject%20Object%5D&name=image.png&originHeight=289&originWidth=1272&originalType=binary&ratio=1&rotation=0&showTitle=false&size=26804&status=done&style=none&taskId=u31d802bc-a95f-4dc4-bebc-a3e2af71732&title=&width=636)
组合表示类之间的整体与部分的关系，但它是一种更强烈的聚合关系。
在组合关系中，整体对象可以控制部分对象的生命周期，一旦整体对象不存在，部分对象也将不存在，部分对象不能脱离整体对象而存在。例如，头和嘴的关系，没有了头，嘴也就不存在了。
#### 依赖关系
依赖关系是一种使用关系，它是对象之间耦合度最弱的一种关联方式，是临时性的关联。在代码中，某个类的方法通过局部变量、方法的参数或者对静态方法的调用来访问另一个类（被依赖类）中的某些方法来完成一些职责。

#### 继承关系
继承关系是对象之间耦合度最大的一种关系，表示一般与特殊的关系，是父类与子类之间的关系，是一种继承关系。

![image.png](https://cdn.nlark.com/yuque/0/2022/png/33764834/1668320994476-e5f53786-80fd-4922-a71e-dd3250a3309b.png#averageHue=%23f9f9f9&clientId=u3314fbe6-f385-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=288&id=ucb194d4e&margin=%5Bobject%20Object%5D&name=image.png&originHeight=576&originWidth=1021&originalType=binary&ratio=1&rotation=0&showTitle=false&size=147974&status=done&style=none&taskId=u02b02430-ac8c-45c2-a789-a120bbd4a6f&title=&width=510.5)
#### 实现关系
实现关系是接口与实现类之间的关系。在这种关系中，类实现了接口，类中的操作实现了接口中所声明的所有的抽象操作。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/33764834/1668321683243-25aef5b1-d514-4ed0-846f-9624062c7c3b.png#averageHue=%23f9f9f9&clientId=u3314fbe6-f385-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=286&id=uef6cf059&margin=%5Bobject%20Object%5D&name=image.png&originHeight=571&originWidth=1017&originalType=binary&ratio=1&rotation=0&showTitle=false&size=145061&status=done&style=none&taskId=ub372f9a0-9955-4eb0-8df7-bf21cdf4be4&title=&width=508.5)
