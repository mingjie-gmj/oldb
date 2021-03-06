# Index



## Blogs

### Postgresql



#### SQL引擎

(201807) [《关系代数》](src/sql-kp-relation_algebra.md)

(201805) [《The Hospital案例——执行计划&成本分析（未完）》](src/sql-exec-hospital.md)

(201805 80%) [《Planet Express案例——执行计划&成本分析》](src/sql-exec-planetexpress.md)

(201805 80%) [《postgresql全文搜索》](src/pgsql-sql-fulltextsearch.md)

(201805) [《LT && SQL总结》](src/sql-exec-leetcode.md)

(201806 50%) [《拆解分析德哥给出的表膨胀检测SQL》](src/pgsql-sql-bloatsql.md)

#### 存储引擎

(201803) [《Postgresql并发控制总结实践》](src/pgsql-kp-concurrency.md)

(201804)[《两阶段提交》](src/pgsql-kp-twophase.md)

(201712)[《Fast-Path Lock》](src/pgsql-kp-fastpath.md)

(201801)[《MemoryContext分析》](src/pgsql-internal-memorycontext.md)

#### 应用案例

(201804)[《postgresql字符串操作总结（未完）》](src/pgsql-sql-string.md)

(201805)[《Postgresql DDL 审计实战》](src/pgsql-sql-ddlaudit.md)

(201804)[《Postgresql逻辑备份与恢复实战》](src/pgsql-fun-pgdumpbackup.md)

(201803)[《pg_dump几种导出方式测试》](src/pgsql-fun-pgdump.md)

(201804)[《Postgresql冷备份与恢复实战》](src/pgsql-fun-offlinebackup.md)

(201712)[《几种HA部署方式》](src/pgsql-fun-ha.md)

(201712)[《安装PostgresXL》](src/pgsql-deploy-xl.md)

(201807)[《Postgresql Tuning》](src/pgsql-tuning.md)

(201806 50%) [《构造postgresql测试数据库（填充一个数据库）》](src/pgsql-sql-testdatabase.md)

### Greenplum



### BitTorrent

(201808) [《BT Engine Research》](src/bt-research.md)



### Oracle

(201802) [《oracle12c安装记录》](src/orcl-deploy-12c.md)

(201801) [《Oracle监听连接》](src/orcl-fun-lsnrctl.md)

(201801) [orcl-cheatsheet.sql](src/orcl-cheatsheet.sql)

### Linux

(201712) [《Centos Firewalld》](src/linux-centos-firewalld.md)

(201807 30%) [《子网掩码 & vlsm》](src/linux-kp-netmask.md)

perf

### 运维

待整理：IP的分段子网掩码计算1.1.1.1/26；磁盘inode，删了文件空间未减少？；文件过滤，文件名正则、时间修改创建时间ctime

### 开发环境

() 补充一篇mac下docker的操作手册，笔记上的整理过来。

### 未归类



(201805) [《plantuml》](src/utils-plantuml.md)

(201801) [《win多网卡路由》](src/utils-win-doalnetwordcardrounting.md)

(201805) [《Google Style Guides-Shell Style Guide(翻译)》](src/shell-style.md)



(201804) [《Postgresql 执行计划&索引相关》delete](src/pgsql-fun-explain.md)



---



## Database Paper

后面在EXCEL上总结，md格式太不方便了。





### [1]概述

DBSI

(201806 20%) [1_System_R_relational_approach_to_database_management.pdf](paper/1_System_R_relational_approach_to_database_management.pdf)

(201806 50%) [1_The_design_and_implementation_of_INGRES.pdf](paper/1_The_design_and_implementation_of_INGRES.pdf)

### [2]存储管理

### [3]索引

### [4]查询执行

### [5]查询编译器

### [6]日志

> DBSI
>
> 最重要的文献是5，这本书的部分材料来自Jim Gray关于事务的一些非正规、广为传播的文献3；后者以及文献4和8是许多日志和恢复技术的主要来源。
>
> 文献2是对事务处理基础一个更早、更简洁的描述。文献7是对这一主题的较近期的论述。
>
> 两个早期的综述1和6，都描绘了关于恢复的大量技术性工作，并且将这一主题按照undo-redo-undo/redo3部分来组织，这本书也采用这种形式。

(1) (下不到) Recovery algorithms for database systems

(2) (下不到) Concurrency control and recovery in database systems

(3) (下不到) Notes on data base operating systems

(4) (201806) [6_The_recovery_manager_of_the_System_R_database_manager.pdf](paper/6_The_recovery_manager_of_the_System_R_database_manager.pdf)

(5) (J Gray那本经典书) Transaction processing: concepts and techniques

(6) (201806) [6_Principles_of_transaction-oriented_database_recovery.pdf](paper/6_Principles_of_transaction-oriented_database_recovery.pdf)

(7) (下不到 书) Recovery mechanisms in database systems

(8) (201806) [6_ARIES_a_transaction_recovery_method_supporting_fine-granularity_locking_and_partial_rollbacks_using_write-ahead_logging.pdf](paper/6_ARIES_a_transaction_recovery_method_supporting_fine-granularity_locking_and_partial_rollbacks_using_write-ahead_logging.pdf)

---

>TPCT
>
>

首先要看看IMS的文章，后面的很多理论在IMS中实现：



1978年Gray实现了IMS系统作者Ron Obermarck、Homer Leonard提出的日志系统，这篇文章/书非常重要，事务处理书中的一些基础概念来自这篇文章，这篇文章对一些非正规、广为传播的知识作了汇总：

(1) (下不到) Notes on data base operating systems

1985年Dieter Gawlick提出了成组提交的方案，并在IMS的Fastpath中实现了这一方案：

(2) Varieties of Concurrency Control in IMS/VS FastPath

1987年用于设置成组提交定时器的优化公示被提出：

(3) Group Commit Timers and High Volume Transaction Systems





(2)  [6_Crash_recovery_in_a_distributed_data_storage_system.pdf](paper/6_Crash_recovery_in_a_distributed_data_storage_system.pdf)

(3) (下不到) System level concurrency control for distributed database systems



### [7]并发控制



TPCT文章：





### [8]事务

### [9]分布式数据库



---



## Database Book

> https://github.com/digoal/blog/blob/master/201804/20180425_01.md

### 

####  事务处理：概念与技术 (Jim Gray)

(20180601 10%) 日志恢复

#### 数据库系统实现

(20180201 - 0202 100%) 6-日志恢复

(20180320 - 0325 100%) 7-并发控制

(20180402 - 0404 100%) 8-事务管理

\>>> (20180724 - ing) 7-并发控制（重点看基于锁的并发控制）

#### PostgreSQL数据库内核分析

(20180423 - 0512 100%) SQL引擎部分

(20180504 - 0520 100%) 存储引擎部分

(20180601 - 0603 100%) 事务

(20180701 - 0715 100%) 存储引擎部分

#### 算法导论

\>>> (20180724 - ing) 3-数据结构

---

### 

#### The Internals of PostgreSQL

http://www.interdb.jp/pg/

(20180701 100%) Chapter 1 Database Cluster, Databases, and Tables

(20180704 100%) Chapter 2 Process and Memory Architecture



---

## Practice

### 01 德哥第五重场景把玩 (60天)

> https://github.com/digoal/blog/blob/master/201804/20180425_01.md
>
> 第五重：场景把玩 (60天)：了解场景，以及数据库特性，加深对PG的了解。
>
> 个人电脑，格式结果仅供参考
>
> 机器配置1：Centos7 Intel(R) Core(TM) i5-4250U CPU @ 1.30GHz   SSD-120GB  Memory-8GB
>
> 机器配置2:   Mac Intel Core i7 2.2 GHz SSD-250GB   Memory-16GB

| TEST             | CLASS | SCRIPT                                      | tps         | latencies(ms) |
| ---------------- | ----- | ------------------------------------------- | ----------- | ------------- |
| 点查             | SQL   | [scenario_test01.sh](sh/scenario_test01.sh) | 5849.152002 | 19.143        |
| 多表JOIN         | SQL   | [scenario_test02.sh](sh/scenario_test02.sh) | 599.122652  | 187.458       |
| 大表JOIN统计查询 | SQL   | [scenario_test03.sh](sh/scenario_test03.sh) |             |               |

### 02 xxx







---

## Scripts & Extensions

### postgresql

(script 100%) [genv](scripts/genv)

(script 100%) [pg_archive.sh](scripts/pg_archive.sh)



(extentions 100%) [pg_memorycontext (release on pgxn)](https://pgxn.org/dist/pg_memorycontext/1.0.1/)

### linux

[SetupSSH](scripts/SetupSSH)   ing...



---



# A4 Plan

<details>
<summary>A4 Plan</summary>
x

</details>

---



## OJ:)

| source    | subject                                  | tags                           | answer                                   | note |
| --------- | ---------------------------------------- | ------------------------------ | ---------------------------------------- | ---- |
| codeforce | [1A-TheatreSquare](http://codeforces.com/problemset/problem/1/A) | math                           | [1A-TheatreSquare.cc](codeforces/1A-TheatreSquare.cc) |      |
| codeforce | [1B-Spreadsheet](http://codeforces.com/problemset/problem/1/B) | implementation,math            | [1B-Spreadsheet.cc](codeforces/1B-Spreadsheet.cc) |      |
| codeforce | [948A-ProtectSheep](http://codeforces.com/problemset/problem/948/A) | brute force                    | [948A-ProtectSheep.cc](codeforces/948A-ProtectSheep.cc) |      |
| codeforce | [923B-ProducingSnow](http://codeforces.com/problemset/problem/923/B) | binary search, data structures | [923B-ProducingSnow.cc](codeforces/923B-ProducingSnow.cc) |      |
|           |                                          |                                |                                          |      |
|           |                                          |                                |                                          |      |
|           |                                          |                                |                                          |      |
|           |                                          |                                |                                          |      |
|           |                                          |                                |                                          |      |







---



<details>
<summary>乱七八糟记录</summary>

pg_man: select pg_man('max_connections')返回手册中这参数的介绍，自动识别版本。

这个思路不错https://github.com/NikolayS/postgres_dba

https://github.com/joyent/pgsqlstat

</details>

