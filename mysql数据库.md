# 基础篇
* [基础架构：一条SQL查询语句是如何执行的？](#基础架构：一条SQL查询语句是如何执行的？)
* [日志系统：一条SQL更新语句是如何执行的？]
## 基础架构：一条SQL查询语句是如何执行的？
我们经常说，看一个事儿千万不要直接陷入细节里，你应该先鸟瞰其全貌，这样能够帮助你从高维度理解问题。比如，你有个最简单的表，表里只有一个 ID 字段，在执行下面这个查询语句时：
```sql
mysql> select * from T where ID=10；
```
我们只知道它返回了一个结构，那么它内部是如何工作的呢？
下面我给出的是 MySQL 的基本架构示意图，从中你可以清楚地看到 SQL 语句在 MySQL 的各个功能模块中的执行过程。

<div align="center"> <img src="https://static001.geekbang.org/resource/image/0d/d9/0d2070e8f84c4801adbfa03bda1f98d9.png"/> </div><br>
