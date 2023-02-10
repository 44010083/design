---
home: true
heroImage: img/bg.gif
heroText: Design
tagline: Design 是个人对于架构的心得和总结。
bannerBg: none
postList: none
footer: CC-BY-SA-4.0 Licensed | Copyright © 2018-Now Dunwu
---

<p align="center">

  <a href="https://github.com/dunwu/design">
      <img alt="star" class="no-zoom" src="https://img.shields.io/github/stars/dunwu/design?style=for-the-badge">
  </a>

  <a href="https://github.com/dunwu/design">
      <img alt="fork" class="no-zoom" src="https://img.shields.io/github/forks/dunwu/design?style=for-the-badge">
  </a>

  <a href="https://github.com/dunwu/design/commits/master">
      <img alt="build" class="no-zoom" src="https://img.shields.io/github/actions/workflow/status/dunwu/design/deploy.yml?style=for-the-badge">
  </a>

  <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh">
      <img alt="code style" class="no-zoom" src="https://img.shields.io/github/license/dunwu/design?style=for-the-badge">
  </a>

</p>

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

### 分布式

#### 分布式综合

- [分布式面试总结](01.计算机科学/11.分布式/00.分布式综合/99.分布式面试.md)

#### 分布式理论

- [分布式理论](01.计算机科学/11.分布式/00.分布式综合/01.分布式基础理论.md) - 关键词：`拜占庭将军`、`CAP`、`BASE`、`错误的分布式假设`
- [分布式算法 Paxos](01.计算机科学/11.分布式/00.分布式综合/11.Paxos算法.md) - 关键词：`共识性算法`
- [分布式算法 Raft](01.计算机科学/11.分布式/00.分布式综合/12.Raft算法.md) - 关键词：`共识性算法`
- [分布式算法 Gossip](01.计算机科学/11.分布式/00.分布式综合/13.Gossip算法.md) - 关键词：`数据传播`

#### 分布式关键技术

- 集群
- 复制
- 分区
- 选主

##### 流量调度

- [流量控制](01.计算机科学/11.分布式/01.分布式技术/01.流量调度/03.流量控制.md) - 关键词：`限流`、`熔断`、`降级`、`计数器法`、`时间窗口法`、`令牌桶法`、`漏桶法`
- [负载均衡](01.计算机科学/11.分布式/01.分布式技术/01.流量调度/02.负载均衡.md) - 关键词：`轮询`、`随机`、`最少连接`、`源地址哈希`、`一致性哈希`、`虚拟 hash 槽`
- [服务路由](01.计算机科学/11.分布式/01.分布式技术/01.流量调度/01.服务路由.md) - 关键词：`路由`、`条件路由`、`脚本路由`、`标签路由`
- 服务网关
- [分布式会话](01.计算机科学/11.分布式/01.分布式技术/01.流量调度/10.分布式会话.md) - 关键词：`粘性 Session`、`Session 复制共享`、`基于缓存的 session 共享`

##### 数据调度

- [数据缓存](01.计算机科学/11.分布式/01.分布式技术/02.数据调度/01.数据缓存.md) - 关键词：`进程内缓存`、`分布式缓存`、`缓存雪崩`、`缓存穿透`、`缓存击穿`、`缓存更新`、`缓存预热`、`缓存降级`
- [读写分离](01.计算机科学/11.分布式/01.分布式技术/02.数据调度/02.读写分离.md)
- [分库分表](01.计算机科学/11.分布式/01.分布式技术/02.数据调度/03.分库分表.md) - 关键词：`分片`、`路由`、`迁移`、`扩容`、`双写`、`聚合`
- [分布式 ID](01.计算机科学/11.分布式/01.分布式技术/02.数据调度/04.分布式ID.md) - 关键词：`UUID`、`自增序列`、`雪花算法`、`Leaf`
- [分布式事务](01.计算机科学/11.分布式/01.分布式技术/02.数据调度/05.分布式事务.md) - 关键词：`2PC`、`3PC`、`TCC`、`本地消息表`、`MQ 消息`、`SAGA`
- [分布式锁](01.计算机科学/11.分布式/01.分布式技术/02.数据调度/06.分布式锁.md) - 关键词：`数据库`、`Redis`、`ZooKeeper`、`互斥`、`可重入`、`死锁`、`容错`、`自旋尝试`

##### 资源调度

- 弹性伸缩

##### 通信

- [消息队列](01.计算机科学/11.分布式/01.分布式技术/04.通信/01.消息队列.md) - 关键词：`重复消费`、`消息丢失`、`消息顺序性`、`消息积压`

##### 服务治理

- [服务注册和发现](01.计算机科学/11.分布式/01.分布式技术/05.服务治理/01.服务注册和发现.md)
- [服务监控](01.计算机科学/11.分布式/01.分布式技术/05.服务治理/02.服务监控.md)
- [服务链路监控](01.计算机科学/11.分布式/01.分布式技术/05.服务治理/03.服务链路监控.md)
- [服务容错](01.计算机科学/11.分布式/01.分布式技术/05.服务治理/04.服务容错.md)
- 服务编排
- 服务版本管理
- 流量调度
  - [流量控制](01.计算机科学/11.分布式/01.分布式技术/01.流量调度/03.流量控制.md) - 关键词：`限流`、`熔断`、`降级`、`计数器法`、`时间窗口法`、`令牌桶法`、`漏桶法`
  - [负载均衡](01.计算机科学/11.分布式/01.分布式技术/01.流量调度/02.负载均衡.md) - 关键词：`轮询`、`随机`、`最少连接`、`源地址哈希`、`一致性哈希`、`虚拟 hash 槽`
  - [服务路由](01.计算机科学/11.分布式/01.分布式技术/01.流量调度/01.服务路由.md) - 关键词：`路由`、`条件路由`、`脚本路由`、`标签路由`
  - 服务网关

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

◾ 🏠 [DESIGN 首页](https://github.com/dunwu/design) ◾ 🎯 [钝悟的博客](https://github.com/dunwu/blog) ◾

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
