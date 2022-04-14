<p align="center">
    <a href="https://dunwu.github.io/design/" target="_blank" rel="noopener noreferrer">
        <img src="https://raw.githubusercontent.com/dunwu/images/dev/common/dunwu-logo-200.png" alt="logo" width="150px"/>
    </a>
</p>

<p align="center">

  <a href="https://github.com/dunwu/design">
      <img alt="star" class="no-zoom" src="https://img.shields.io/github/stars/dunwu/design?style=for-the-badge">
  </a>

  <a href="https://github.com/dunwu/design">
      <img alt="fork" class="no-zoom" src="https://img.shields.io/github/forks/dunwu/design?style=for-the-badge">
  </a>

  <a href="https://github.com/dunwu/design/commits/master">
      <img alt="commit" class="no-zoom" src="https://img.shields.io/github/workflow/status/dunwu/design/CI?style=for-the-badge">
  </a>

  <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh">
      <img alt="code style" class="no-zoom" src="https://img.shields.io/github/license/dunwu/design?style=for-the-badge">
  </a>

</p>

<h1 align="center">DESIGN</h1>

> ☕ **DESIGN** 是个人对于软件系统架构的心得和总结。
>
> 架构之道，在于权衡；权衡之术，在于取舍。
>
> - 🔁 项目同步维护：[Github](https://github.com/dunwu/design/) | [Gitee](https://gitee.com/turnon/design/)
> - 📖 电子书阅读：[Github Pages](https://dunwu.github.io/design/) | [Gitee Pages](http://turnon.gitee.io/design/)

## 📖 内容

### 设计步骤

解决方案（Solution），就是针对某些已经体现出的，或者可以预期的问题、不足、缺陷、需求等等，所提出的一个解决整体问题的可行性方案。就软件系统而言，解决方案就是一个可以解决具体业务问题，并且可以落地的软件系统。

解决方案，毫无疑问是顶层系统设计，这需要设计者既懂技术，也懂业务。

#### 第一步：需求分析

把所有需要的东西聚集在一起，审视问题。不停的提问，以至于我们可以明确使用场景和约束。讨论假设。

- **What**：系统的作用是什么？系统的目标是什么？
- **Who**：系统的用户群体是谁？
- **How**：用户希望怎样使用系统？系统如何为用户提供服务？
- **How many**：有多少用户？日活/月活有多少？——用户体量会极大的影响系统的性能要求，从而影响系统的规模和复杂度。
  - **容量**：系统需要处理多少数据？
  - **并发量、吞吐量**：系统需要每秒钟处理多少请求？
  - **读写比率**：系统的读写比率是多少？——读多写少或写多读少决定了不同的架构方案。
- **How much**：系统的预算是多少（包括物料、人力成本等）？
- **输入输出**：系统的输入输出分别是什么？

#### 第二步：顶层设计

使用所有重要的组件来描绘出一个高层级的设计。

- 画出主要的组件和连接
- 证明你的想法

#### 第三步：组件设计

对每一个核心组件进行详细深入的分析。

#### 第四步：扩展设计

确认和处理瓶颈以及一些限制。举例来说就是你需要下面的这些来完成扩展性的议题吗？

- 负载均衡
- 水平扩展
- 缓存
- 数据库分片

### [架构](docs/01.架构)

> 如果把软件开发工作比作是一场战争，那么系统架构无疑是战略层面的工作。众所周知，万丈高楼平地起，系统架构就像是软件的地基，如果一开始就歪了，那么代码写得再漂亮，软件也难以成功。
>
> 软件整体结构与组件的抽象描述，用于指导大型软件系统各个方面的设计。重点是分而治之，先将大型系统抽象为各个组件或模块；然后逐一解决各组件、各模块的功能、性能问题；最后将这些组件、模块整合成对外服务的一个整体。

- [系统架构面试题](docs/01.架构/01.系统架构面试.md)
- [系统架构概述](docs/01.架构/02.系统架构概述.md)
- [系统高性能架构](docs/01.架构/03.系统高性能架构.md)
- [系统高可用架构](docs/01.架构/04.系统高可用架构.md)
- [系统伸缩性架构](docs/01.架构/05.系统伸缩性架构.md)
- [系统扩展性架构](docs/01.架构/06.系统扩展性架构.md)
- [系统安全性架构](docs/01.架构/07.系统安全性架构.md)
- [大型系统核心技术](docs/01.架构/08.大型系统核心技术.md)
- [领域驱动设计](docs/01.架构/09.领域驱动设计.md)

### [分布式](docs/02.分布式)

#### 分布式综合

- [分布式面试总结](docs/02.分布式/01.分布式综合/01.分布式面试总结.md)

#### 分布式理论

- [分布式理论](docs/02.分布式/02.分布式理论/01.分布式理论.md) - 关键词：`拜占庭将军`、`CAP`、`BASE`、`错误的分布式假设`
- [分布式算法 Paxos](docs/02.分布式/02.分布式理论/02.分布式算法Paxos.md) - 关键词：`共识性算法`
- [分布式算法 Raft](docs/02.分布式/02.分布式理论/03.分布式算法Raft.md) - 关键词：`共识性算法`
- [分布式算法 Gossip](docs/02.分布式/02.分布式理论/04.分布式算法Gossip.md) - 关键词：`数据传播`

#### 分布式关键技术

- 集群
- 复制
- 分区
- 选主

##### 流量调度

- [负载均衡](docs/02.分布式/03.分布式关键技术/01.流量调度/01.负载均衡.md) - 关键词：`轮询`、`随机`、`最少连接`、`源地址哈希`、`一致性哈希`、`虚拟 hash 槽`
- [流量控制](docs/02.分布式/03.分布式关键技术/01.流量调度/02.流量控制.md) - 关键词：`限流`、`熔断`、`降级`、`计数器法`、`时间窗口法`、`令牌桶法`、`漏桶法`
- 网关
- [分布式会话](docs/02.分布式/03.分布式关键技术/01.流量调度/03.分布式会话.md) - 关键词：`粘性 Session`、`Session 复制共享`、`基于缓存的 session 共享`

##### 数据调度

- [数据缓存](docs/02.分布式/03.分布式关键技术/02.数据调度/01.数据缓存.md) - 关键词：`进程内缓存`、`分布式缓存`、`缓存雪崩`、`缓存穿透`、`缓存击穿`、`缓存更新`、`缓存预热`、`缓存降级`
- [读写分离](docs/02.分布式/03.分布式关键技术/02.数据调度/02.读写分离.md)
- [分库分表](docs/02.分布式/03.分布式关键技术/02.数据调度/03.分库分表.md) - 关键词：`分片`、`路由`、`迁移`、`扩容`、`双写`、`聚合`
- [分布式 ID](docs/02.分布式/03.分布式关键技术/02.数据调度/04.分布式ID.md) - 关键词：`UUID`、`自增序列`、`雪花算法`、`Leaf`
- [分布式事务](docs/02.分布式/03.分布式关键技术/02.数据调度/05.分布式事务.md) - 关键词：`2PC`、`3PC`、`TCC`、`本地消息表`、`MQ 消息`、`SAGA`
- [分布式锁](docs/02.分布式/03.分布式关键技术/02.数据调度/06.分布式锁.md) - 关键词：`数据库`、`Redis`、`ZooKeeper`、`互斥`、`可重入`、`死锁`、`容错`、`自旋尝试`

##### 资源调度

- 弹性伸缩

##### 通信

- [消息队列](docs/02.分布式/03.分布式关键技术/04.通信/01.消息队列.md) - 关键词：`重复消费`、`消息丢失`、`消息顺序性`、`消息积压`

##### 服务治理

- 注册中心
- 服务发现
- 服务调用
- 服务调用链
- 服务依赖
- 服务编排
- 服务版本管理

### 设计

#### [UML](docs/03.设计/01.UML)

> 统一建模语言（英语 - Unified Modeling Language，缩写 UML）是非专利的第三代建模和规约语言。UML 是一种开放的方法，用于说明、可视化、构建和编写一个正在开发的、面向对象的、软件密集系统的制品的开放方法。UML 展现了一系列最佳工程实践，这些最佳实践在对大规模，复杂系统进行建模方面，特别是在软件架构层次已经被验证有效。

- [UML 快速入门](docs/03.设计/01.UML/01.UML快速入门.md)
- [UML 结构建模图](docs/03.设计/01.UML/02.UML结构建模图.md)
- [UML 行为建模图](docs/03.设计/01.UML/03.UML行为建模图.md)

#### [设计模式](docs/03.设计/02.设计模式)

> 设计模式（Design pattern）代表了最佳的实践，通常被有经验的面向对象的软件开发人员所采用。设计模式是软件开发人员在软件开发过程中面临的一般问题的解决方案。这些解决方案是众多软件开发人员经过相当长的一段时间的试验和错误总结出来的。

##### 创建型模式

- [简单工厂模式 (Simple Factory)](docs/03.设计/02.设计模式/01.简单工厂模式.md)
- [工厂方法模式 (Factory Method)](docs/03.设计/02.设计模式/02.工厂方法模式.md)
- [抽象工厂模式 (Abstract Factory)](docs/03.设计/02.设计模式/03.抽象工厂模式.md)
- [建造者模式 (Builder)](docs/03.设计/02.设计模式/04.建造者模式.md)
- [原型模式 (Prototype)](docs/03.设计/02.设计模式/05.原型模式.md)
- [单例模式 (Singleton)](docs/03.设计/02.设计模式/06.单例模式.md)

##### 结构型模式

- [适配器模式 (Adapter)](docs/03.设计/02.设计模式/07.适配器模式.md)
- [桥接模式 (Bridge)](docs/03.设计/02.设计模式/08.桥接模式.md)
- [组合模式 (Composite)](docs/03.设计/02.设计模式/09.组合模式.md)
- [装饰模式 (Decorator)](docs/03.设计/02.设计模式/10.装饰模式.md)
- [外观模式 (Facade)](docs/03.设计/02.设计模式/11.外观模式.md)
- [享元模式 (Flyweight)](docs/03.设计/02.设计模式/12.享元模式.md)
- [代理模式 (Proxy)](docs/03.设计/02.设计模式/13.代理模式.md)

##### 行为型模式

- [模板方法模式 (Template Method)](docs/03.设计/02.设计模式/14.模板方法模式.md)
- [命令模式 (Command)](docs/03.设计/02.设计模式/15.命令模式.md)
- [迭代器模式 (Iterator)](docs/03.设计/02.设计模式/16.迭代器模式.md)
- [观察者模式 (Observer)](docs/03.设计/02.设计模式/17.观察者模式.md)
- [解释器模式 (Interpreter)](docs/03.设计/02.设计模式/18.解释器模式.md)
- [中介者模式 (Mediator)](docs/03.设计/02.设计模式/19.中介者模式.md)
- [职责链模式 (Chain of Responsibility)](docs/03.设计/02.设计模式/20.职责链模式.md)
- [备忘录模式 (Memento)](docs/03.设计/02.设计模式/21.备忘录模式.md)
- [策略模式 (Strategy)](docs/03.设计/02.设计模式/22.策略模式.md)
- [访问者模式 (Visitor)](docs/03.设计/02.设计模式/23.访问者模式.md)
- [状态模式 (State)](docs/03.设计/02.设计模式/24.状态模式.md)

#### [重构](docs/03.设计/03.重构)

> **改善既有代码的设计**。
>
> 关键词：过长函数、过大的类、基本类型偏执、过长参数列、数据泥团、switch 声明、临时字段、被拒绝的馈赠、异曲同工的类、发散式变化、霰弹式修改、平行继承体系、过多的注释、重复代码、冗余类、纯稚的数据类、夸夸其谈未来性、依恋情结、狎昵关系、过度耦合的消息链、中间人、不完美的库类

- [代码的坏味道和重构](docs/03.设计/03.重构/01.代码的坏味道和重构.md)
- [代码坏味道之代码臃肿](docs/03.设计/03.重构/02.代码坏味道之代码臃肿.md)
- [代码坏味道之滥用面向对象](docs/03.设计/03.重构/03.代码坏味道之滥用面向对象.md)
- [代码坏味道之变革的障碍](docs/03.设计/03.重构/04.代码坏味道之变革的障碍.md)
- [代码坏味道之非必要的](docs/03.设计/03.重构/05.代码坏味道之非必要的.md)
- [代码坏味道之耦合](docs/03.设计/03.重构/06.代码坏味道之耦合.md)

## 📚 资料

- **书籍**
  - [《大型网站技术架构：核心原理与案例分析》](https://item.jd.com/11322972.html) - 浅显易懂的将解大型网站架构演进之路；简介了大型系统所面临的挑战以及核心技术点。
  - [《亿级流量网站架构核心技术：跟开涛学搭建高可用高并发系统》](https://item.jd.com/12153914.html)
  - [大型网站系统与 Java 中间件实践](https://item.jd.com/11449803.html)
  - [企业 IT 架构转型之道：阿里巴巴中台战略思想与架构实战](https://item.jd.com/12176278.html) - 阐述阿里巴巴中台系统发展，更多的是讲解应用场景和能力，没有讲解技术细节。
  - [逆流而上：阿里巴巴技术成长之路](https://item.jd.com/12238227.html) - 主要以运维的视角阐述系统运维中遇到的困难，定位思路以及解决方法。
  - [《Head First 设计模式》](https://book.douban.com/subject/2243615/)
  - [《大话设计模式》](https://book.douban.com/subject/2334288/)
  - [《重构——改善既有代码的设计》](https://book.douban.com/subject/4262627/)
- **教程**
  - [system-design-primer](https://github.com/donnemartin/system-design-primer/blob/master/README-zh-Hans.md)
  - [从 0 开始学架构](https://time.geekbang.org/column/intro/100006601)
  - [从 0 开始学微服务](https://time.geekbang.org/column/intro/100014401)
  - [RPC 实战与核心原理](https://time.geekbang.org/column/intro/100046201)
  - [微服务架构核心 20 讲](https://time.geekbang.org/course/intro/100003901)
  - [DDD 实战课](https://time.geekbang.org/column/intro/100037301)
  - [Sparx UML 教程](https://sparxsystems.cn/resources/uml2_tutorial/index.html)
  - [UML Tutorial](https://www.tutorialspoint.com/uml/index.htm)
  - [W3Cschool UML 教程](https://www.w3cschool.cn/uml_tutorial/)
  - https://sourcemaking.com/refactoring

## 🚪 传送

◾ 🏠 [DESIGN 首页](https://github.com/dunwu/design) ◾ 🎯 [我的博客](https://github.com/dunwu/blog) ◾

> 你可能会感兴趣：

- [Java 教程](https://github.com/dunwu/java-tutorial) 📚
- [JavaCore 教程](https://dunwu.github.io/javacore/) 📚
- [JavaTech 教程](https://dunwu.github.io/javatech/) 📚
- [Spring 教程](https://dunwu.github.io/spring-tutorial/) 📚
- [Spring Boot 教程](https://dunwu.github.io/spring-boot-tutorial/) 📚
- [数据库教程](https://dunwu.github.io/design/) 📚
- [数据结构和算法教程](https://dunwu.github.io/algorithm-tutorial/) 📚
- [Linux 教程](https://dunwu.github.io/linux-tutorial/) 📚
- [Nginx 教程](https://github.com/dunwu/nginx-tutorial/) 📚
