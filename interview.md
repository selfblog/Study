# java基础
1. List和Set的区别
2. HashSet是如何保证不重复的?
3. HashMap是线程安全的吗, 为什么不是线程安全的(最好画图说明多线程环境下不安全)
4. HashMap的扩容过程
5. HashMap 1.7 与 1.8 的区别, 说明1.8做了哪些优化, 如何优化的?
6. final finally finalize
7. 强引用, 软引用, 弱引用, 虚引用
8. java反射
9. Array.sort的实现原理和Collection实现原理
10. LinkedHashMap的应用
11. cloneable接口实现原理
12. 异常分类以及处理机制
13. wait和sleep的区别
14. 数组在内存中如何分配

# java并发
1. synchronized的实现原理以及锁优化
2. volatile的实现原理是
3. java信号灯
4. synchronized在静态方法和普通方法的区别
5. 怎么实现所有线程在等待某个时间的发生才会去执行
6. CAS? CAS有什么缺陷? 如何解决?
7. synchronized和lock有什么区别?
8. HashTable是怎么加锁的?
9. HashMap的并发问题?
10. ConcurrentHashMap介绍? 1.8中为什么要用红黑树?
11. AQS
12. 如何检测死锁? 怎么预防死锁?
13. java内存模型
14. 如何保证多线程下i++结果正确
15. 线程池的种类, 区别和使用场景
16. 分析线程池的实现原理和线程的调度过程?
17. 线程池如何调优, 最大数目如何确认?
18. ThreadLocal原理, 用的时候需要注意什么?
19. CountDownLatch和CyclicBarrier的用法, 以及相互之间的差别?
20. LockSupport工具
21. Condition接口及其实现原理
22. Fork/Join框架的理解
23. 分段锁的原理, 锁力度减小的思考
24. 八种阻塞队列以及各个阻塞队列的特性

# Spring
1. BeanFactory 和 FactoryBean?
2. Spring IOC 的理解, 其初始化过程?
3. BeanFactory 和 ApplicationContext?
4. Spring Bean 的生命周期, 如何被管理的?
5. Spring Bean 的加载过程是怎样的?
6. 如果要你实现Spring AOP, 请问怎么实现?
7. 如果要你实现Spring IOC, 你会注意哪些问题?
8. Spring是如何管理事务的, 事务管理机制?
9. Spring的不同事务传播行为有哪些, 干什么用的?
10. Spring中用到了哪些设计模式?
11. Spring MVC 的工作原理?
12. Spring 的循环注入的原理?
13. Spring AOP 的理解, 各个术语, 他们是怎么相互工作的?
14. Spring 如何保证Controller并发的安全?

# Netty
1. BIO, NIO和AIO
2. Netty的各大组件?
3. Netty的线程模型?
4. TCP 粘包/拆包的原因及解决方法
5. 了解哪几种序列化协议? 包括使用场景和如何去选择
6. Netty的零拷贝实现
7. Netty的高性能体现在哪些方面?

# 分布式相关
1. Dubbo的底层实现原理和机制
2. 描述一个服务从发布到被消费的详细过程
3. 分布式系统怎么服务治理
4. 接口幂等性的概念
5. 消息中间件如何解决消息丢失的问题
6. Dubbo的服务请求失败怎么处理
7. 重连机制会不会造成错误
8. 对分布式事务的理解
9. 如何实现负载均衡? 有哪些算法可以实现?
10. Zookeeper的用途, 选举的原理是什么?
11. 数据的垂直拆分和水平拆分
12. Zookeeper的原理和适用场景
13. Zookeeper watch机制
14. redis/zk节点宕机如何处理
15. 分布式集群下如何做到唯一序列号
16. 如何做一个分布式锁
17. 用过哪些MQ, 怎么用的, 和其他MQ比较有什么优缺点, MQ的连接是线程安全的吗?
18. MQ系统的数据如何保证不丢失?
19. 列举出你能想到的数据库分库分表策略, 分库分表后, 如何解决全表查询问题
20. Zookeeper的选举策略
21. 全局ID

# 数据库
1. MySql分页有哪些优化?
2. 悲观锁, 乐观锁
3. 组合索引, 最左原则
4. mysql的表锁, 行锁
5. mysql性能优化
6. mysql的索引分类: B+, hash; 什么情况下用什么索引?
7. 事务的特性和隔离级别

# 缓存
1. Redis用过哪些数据结构, 以及Redis底层是怎么实现的?
2. Redis缓存穿透, 缓存雪崩
3. 如何使用Redis来实现分布式锁?
4. Redis的并发竞争问题是如何解决的?
5. Redis的持久化的几种方式, 优缺点是什么, 是怎么实现的?
6. Redis的缓存失效策略
7. Redis的集群, 高可用, 原理
8. Redis缓存分片
9. Redis的数据淘汰策略

# JVM
1. 详细jvm内存模型
2. 讲讲什么情况下会出内存溢出, 内存泄漏?
3. 说说java线程栈
4. JVM年轻代到老年代的晋升过程的判断条件是什么?
5. JVM出现fullGC很频繁, 怎么去线上排查问题?
6. 类加载为什么要使用双亲委派模式, 有没有什么场景是打破了这个模式?
7. 类的实例化顺序
8. JVM垃圾回收机制, 何时出发MinorGC等操作
9. JVM中一次完整的GC流程(从 ygc 到 fgc)是怎么样的
10. 各种回收器, 各自优缺点, 重点CMS, G1
11. 各种回收算法
12. OOM错误, stackoverflow错误, permgen space错误