# OSS Select
OSS Select用于对文件执行SQL语句，返回执行结果。
## 使用场景
在使用OSS进行数据处理的场景下，需要将数据仓库的海量数据文件存放在OSS。OSS提供的GET Object接口只能获取整个对象或某段Range数据，使得大数据平台只能把OSS数据全部下载到本地然后进行分析过滤，在很多查询场景下浪费了大量带宽和客户端资源。
OSS Select可以让数据的分析过滤下推到OSS层，接口只返回有用的数据。既减少了客户端的网络带宽，又减少了客户端的数据处理量，节省了客户端的CPU、内存等计算资源。
## 规则限制
OSS Select支持的文件格式：
* 支持UTF-8编码的CSV文件。
OSS Select支持的SQL子句：
* SELECT子句
* FROM子句
* WHERE子句
* LIMIT子句
OSS Select支持的函数：
* 
OSS Select支持的运算符：
* 逻辑运算符：AND，NOT,OR
## 使用方法
通过(Select Content Object)[]接口调用

