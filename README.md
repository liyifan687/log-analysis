# log-analysis
基于hadoop，hbase，java的日志分析系统

网上有很多类似的，数据来源百度一下很多大同小异，本人编写时也借鉴了许多。

目的：结合HDFS、MapReduce、HBase、Hive、Sqoop框架等技术，实现对论坛的日志的分析。
计算该论坛的一些关键指标：浏览量PV，注册用户数，IP数，跳出率。同时将分析结果存入mysql以便查看。

  我这里首先将数据上传到了hdfs中，在编写java程序通过mapreduce将数据清洗后导入hbase中。
  
  再将数据通过hive分析时，我是选择的映射hdfs中清洗过的文件，也可以通过修改配置，hbase和hive集成，使hive映射hbase。
  
  最后将分析结果建立汇总表，使用sqoop导入mysql方便查看，具体请查看文档与详细代码。
  （上传内容包括源码和说明文档）
