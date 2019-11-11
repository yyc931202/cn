# 运维工具


## 简介
运维工具模板、操作、任务相关的接口


### 版本
v1


## API
|接口名称|请求方式|功能描述|
|---|---|---|
|**createTask**|POST|创建任务并执行|
|**createTemplate**|POST|增加自定义模板|
|**deleteTask**|DELETE|删除任务|
|**deleteTemplate**|DELETE|删除模板|
|**getInstanceLog**|GET|查看某一主机日志|
|**getLastInstances**|GET|获取当前模板最新一次执行成功的主机组|
|**getOperations**|GET|获取官方操作列表|
|**getTask**|GET|查看任务执行详情|
|**getTasks**|GET|获取任务列表|
|**getTemplate**|GET|查询模板详情|
|**getTemplates**|GET|列出所有模板|
|**listConfig**|GET|opswork字段国际化对应关系|
|**listInstances**|POST|通过uuids批量查询云主机|
|**updateTemplate**|PUT|编辑模板|
