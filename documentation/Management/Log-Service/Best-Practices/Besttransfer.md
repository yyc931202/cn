## 日志转储配置——ALB访问日志转储

本节将通过一个实际的案例，完成一个日志转储的配置。旨在通过描述整个配置过程让用户更容易地理解日志转储的功能。

### 一、转储需求场景：

1.在京东云上购买了ALB，想将ALB的访问日志自动存储到我的对象存储桶中，以便于后面将日志数据下载下来，对响应时间处理分析，对用户侧进行监控统计。

2.查看一些日志数据转储的执行状态。

### 二、转储任务设置：

达成上述转储配需求需要执行以下操作：

1.在京东云上购买了ALB服务，并且开通了日志服务，在日志服务下创建了日志集，在该日志集下创建了日志主题，创建了采集配置，选择访问日志，将购买的ALB添加到采集实例中，采集日志。购买的ALB产生了访问日志。

2.选择需要转储的ALB访问日志所在的日志集，进入日志主题列表。

![](https://raw.githubusercontent.com/jdcloudcom/cn/zhangwenjie-only/image/LogService/bestpractice/besttransfer01.jpg)

3.点击该日志主题下的子菜单“日志转储”，点击“日志转储”后方的“添加”按钮，或者进入转储任务列表页，点击“新建转储任务”按钮。

![](https://raw.githubusercontent.com/jdcloudcom/cn/zhangwenjie-only/image/LogService/bestpractice/besttransfer02.jpg)

4.转储任务名称输入：**ALB访问日志转储**。

5.转储对象，即转储至对象存储OSS中，选择我账户下的转储桶**logshipper-test-10**，ALB产生的访问日志将会转储至该转储桶内，我可以在对象存储页面中选择该转储桶，并将转储的日志数据下载至本地。对象存储会根据转储的数据量及存储时间进行收费。

6.目录前缀输入：**myappversion1/**。在转储时，会将ALB的访问日志转储至该目录下。

7.分区格式输入：**%Y/%m/%d**。转储时会根据strptime时间格式化自动生成目录，年/月/日的格式目录，如：2019/08/08。

8.转储文件大小：根据自己的需求，选择了**500MB**。单个日志文件达到500MB时会进行切分，每个日志文件不大于500MB。

9.转储时间间隔：根据自己的需求，选择了**30min**。每30分钟会对把时间段内产生的日志文件转储至选择的转储对象中。

10.为了便于查看访问日志中每个字段代表的含义，转储格式选择了**JSON**。

11.为了节省对象存储的存储费用，选择了对日志文件进行压缩，压缩的格式选择了**gzip**。

### 二、查看转储任务历史：

转储任务创建完成后，可以查看转储任务的执行历史，以及转储任务的状态，对于失败的转储任务，1小时内支持重试：

1.点击日志转储下的子菜单“转储历史”。

2.根据需求选择需要查看的转储任务和时间范围。

![](https://raw.githubusercontent.com/jdcloudcom/cn/zhangwenjie-only/image/LogService/bestpractice/besttransfer03.jpg)





