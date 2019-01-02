#QQ 群：419648337 
#专业解答Cobar /  MyCat  /  ClusterDB 使用问题和BUG 以及遇到的坑  

##### 下载：

*	高可用代理部署资:
	`链接: https://pan.baidu.com/s/1w5EwRqAfaabSq39X0M53Gw 提取码: m9cs `

# ClusterDB是什么？
   ClusterDB是数据库和表切分的代理，兼容MySQL协议、JDBC协议和MySQL SQL语法，仅支持MySQL支持前台业务，更简单、更稳定、更高效和更安全。
- 分片，您可以添加新的MySQL实例，因为您的业务增长。
- 高可用性的ClusterDB服务器和底层MySQL都是群集的，业务不会因为单个节点失败而受到影响。
- 兼容MySQL协议，使用ClusterDB作为MySQL。您可以用ClusterDB代替MySQL来为应用程序提供动力。
- 基于阿里开源的Cobar产品而研发,继承MyCat优化细节, 面向企业应用开发的“大数据库集群” 优化、改进、 扩展版
- 支持事务、ACID、可以替代MySQL的加强版数据库
- 一个可以视为“MySQL”集群的企业级数据库，用来替代昂贵的Oracle集群
- 一个融合内存缓存技术、Nosql技术、HDFS大数据的新型SQL Server
- 一个新颖的数据库中间件产品,结合传统数据库和新型分布式数据仓库的新一代企业级数据库中间件产品
- ClusterDB背后有一只强大的技术团队，其参与者都是5年以上资深软件工程师、架构师、DBA等，优秀的技术团队保证了ClusterDB的产品质量。

----

##优化
- 数据分片规则 
- 水平分表LIMIT限制
- Route路由规则
- JDBC连接Oracle 后端管理心跳语句检查优化

##改进
- JDBC连接Oracle高并发下Session不释放
- JDBC连接Oracle高并发下线程池阻塞问题
- Log4j日志框架升级为Logback
- druid1.0.26升级druid1.1.1

##扩展
- 后端为JDBC连接Oracle下，使用客户端连接中间件表显示和表数据展示
- 实现单库分表，按照日期分组，后按照日期分片
- 数据分片规则
- 数据分片节点查看
- 数据SQL执行调运链
- 通过ClusterDB Client替代第三方的Haproxy/LVS/F5等第三方高可用


----

###关键特性
*	支持SQL92标准
*	支持MySQL、Oracle、DB2、SQL Server、PostgreSQL等DB的常见SQL语法
*	遵守Mysql原生协议，跨语言，跨平台，跨数据库的通用中间件代理。
*	基于心跳的自动故障切换，支持读写分离，支持MySQL主从，以及galera cluster集群。
*	支持Galera for MySQL集群，Percona Cluster或者MariaDB cluster
*	基于Nio实现，有效管理线程，解决高并发问题。
*	支持数据的多片自动路由与聚合，支持sum,count,max等常用的聚合函数,支持跨库分页。
*	支持单库内部任意join，支持跨库2表join，甚至基于caltlet的多表join。
*	支持通过全局表，ER关系的分片策略，实现了高效的多表join查询。
*	支持多租户方案。
*	支持分布式事务（弱xa）。
*	支持XA分布式事务（1.6.5）。
*	支持全局序列号，解决分布式下的主键生成问题。
*	分片规则丰富，插件化开发，易于扩展。
*	强大的web，命令行监控。
*	支持前端作为MySQL通用代理，后端JDBC方式支持Oracle、DB2、SQL Server 、 mongodb 、巨杉。
*	支持密码加密
*	支持服务降级
*	支持IP白名单
*	支持SQL黑名单、sql注入攻击拦截
*	支持prepare预编译指令（1.6）
*	支持非堆内存(Direct Memory)聚合计算（1.6）
*	支持PostgreSQL的native协议（1.6）
*	支持mysql和oracle存储过程，out参数、多结果集返回（1.6）
*	支持zookeeper协调主从切换、zk序列、配置zk化（1.6）
*	支持库内分表（1.6）


---- 
##### 新版(1.9)支持以下特性
*	路由解析效率提升(50%-80%)  
*	支持后端数据库重启，无需重启业务应用和数据库中间件
*	加强跨库数据查询、关联查询
*	提供完善的分布式数据库监控管控平台( DaaSOS V1.0.3 )
*	提供分布式数据库运维WEB管理( DaaSOS V1.0.3 )
*	DaaSOS Client 替代第三方的Haproxy，LVS等第三方高可用.
*   提供基于SkyWalking 的SQL链路追踪 目前支持：1.Opentracing 方式    2.SkyWakling 自动探针模式
*   提供基于Apollo的配置文件动态跟新和动态下发 ,完成配置中心管理, 配置信息动态加载，无需重启中间件
*   完整的兼容ClusterDB集群节点的动态上下线( V2.0 DEV )
*	集群基于ZooKeeper管理，在线升级，扩容，智能优化，大数据处理( V2.0 DEV )
*	提供基于TCC的分布式事物管理，需应用结合使用 ( V2.0 DEV )

### 后期规划
*	完全实现分布式事务，完全的支持分布式。
*	通过DaaSOS 完成可视化配置，及智能监控，自动运维。
*	通过mysql 本地节点，完整的解决数据扩容难度，实现自动扩容机制，解决扩容难点。
*	支持基于zookeeper的主从切换及Mycat集群化管理。
*	接入Spark等第三方工具，解决数据分析及大数据聚合的业务场景。
*	通过ClusterDB智能优化，分析分片热点，提供合理的分片建议，索引建议，及数据切分实时业务建议。
*	在支持MySQL的基础上，后端增加更多的开源数据库和商业数据库的支持，包括原生支持PosteSQL等开源数据库，以及通过JDBC等方式间接支持其他非开源的数据库如Oracle、DB2、SQL Server等
*	实现更为智能的自我调节特性，如自动统计分析SQL，自动创建和调整索引，根据数据表的读写频率，自动优化缓存和备份策略等
*	实现更全面的监控管理功能
*	与HDFS集成，提供SQL命令，将数据库装入HDFS中并能够快速分析
*	集成优秀的开源报表工具，使之具备一定的数据分析的能力
*	实现TCC
*	实现在线扩容、在线升级、在线运维
 


