## 2020 级新生培养计划

培养方向：分布式数据库研发

培养目标：

1. 具备一定的软件工程能力
2. 掌握基础数据结构和数据库关键技术
3. 掌握分布式原理和应用开发

技能培养：

 **C++ / JAVA / GO 任选一门主力学习、Python 选修**

1. Git、Stencil、Visio 、Docker 等工具的使用
2. 软件工程能力（代码规范、协作开发、UML 的使用、代码测试、文档撰写）
3. Research、Presentation 能力

时间安排表：

| 时间                                   | 知识点                   | 说明                                                         | Project                                                      |
| -------------------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [week1](./Week1-Database-Introduction) | 数据库分类及内部组件功能 | 学习关系型、文档型、KV 型、图数据库等不同类别等数据库，了解其中架构及功能模块 | 安装相关类别的数据库并简单使用（可以使用 Docker 等工具，分组完成） |
| week2、3                               | 数据结构1                | B-Tree、B+TreeSkipList 、LSM Tree                            | 选取一个数据结构并实现。使用 UML 建模完成功能和测试（代码符合统一规范，具有完备的测试用例）最后形成文档。（后续的Project同样的流要求） |
| week4                                  | 数据结构2                | Bloom Filter、Cuckoo Filter、Consistent Hash、Chord 环       | 实现两种过滤器，并进行性能测试                               |
| week5、6                               | 数据库关键技术           | 事务及 ACID、并发控制（乐观、悲观）、MVCC、数据持久化和故障恢复（日志、检查点、快照） | 选一个数据结构实现并发读写，保证数据一致性                   |
| week7                                  | SQL Engine & Parser      | 了解 SQL Engine 组件及功能，学习 SQL 解析流程及抽象语法树    | 使用 Yacc 现有开源库实现简单的 SQL 解析（选修）              |
| week8，9                               | SQL Optimizer            | 学习常见优化器架构，如 Volcano、Cascades 等，学习查询优化具体流程 | 实现一个并发的 MergeSort 算法（pipeline 或多线程并发 merge），并完成性能调优 |
| week10、11                             | Executor                 | 学习执行算子，如 Join、Agg、Scan 的不同实现                  | 实现 Hash Join 算子并完成性能调优                            |
| week12、13                             | 分布式基础               | 分布式相关概念、时钟、CAP、BASE、分布式事务（2PC/3PC、TCC、Percolator、LCN、Seata)、RPC、MapRudece | 阅读 MapReduce 论文，并结合相关框架实现一个单词统计程序。参考 MIT6.824 课程、Spark |
| week14                                 | 一致性协议               | 学习Paxos，Raft，Zab，Gossip, Quorum等协议                   | 实现 Raft 算法，参考 MIT6.824 课程                           |
| week15                                 | 分布式数据库             | 阅读 BigTable、DynamoDB、TiDB、等论文，了解它们的设计        |                                                              |



说明：整个学习流程的作业和文档需要在实验室 Github 仓库里面提交，每个 Project 会事先建立好框架，每个同学按照框架进行代码和文档的撰写。并且在代码过程中抽象公共代码库方便后续同学的使用，且需做好 todo-list，方便功能的完善。



## 如何提交作业

1. 第一次提交作业的时候请先 `fork` 当前项目到自己的仓库

2. 在自己的仓库里面进行作业的更新

   以第一次作业为例，比如你 `fork` 之后你的代码地址为 `git@github.com:ehds/training-plan.git`

   1. 克隆仓库到本地：

      `git clone git@github.com:ehds/training-plan.git`

   2. 进入当前实验文件夹`Week1-Databse-Introduction`

      `cd Week1-Databse-Introduction`

   3. 新建一个自己的文件夹，名字+实验名称，参考 Example

      `cp -r Example DongShengHe-Week1`

      完善实验文档 Markdown 文件

   4. add 作业内容

      `git add .`

   5. commit 修改

      `git commit -m "message"` （message使用英文填写你所做的修改）如 `git commit -m “complete week1 experiment`

   6. push 分支

      `git push origin master`

3. 提交 PR

   在 Gihub 仓库界面新建一个 pull request 到实验室仓库

4. 审核与修改

   待审核人审核后，根据修改意见进行修改，待通过后即可

## 如何提问

大家遇到问题首先合理利用搜索引擎，网络上可能已经存在比较完美的解决方案

在向同学和老师提问的时候，请先描述问题出现的背景和出现问题的状况，这样更加有利于问题的解决。

请参考[提问的智慧](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/master/README-zh_CN.md)