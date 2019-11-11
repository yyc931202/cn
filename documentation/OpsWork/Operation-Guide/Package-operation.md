# 软件操作 schema

| 字段     | 必须 | 类型   | 含义                                                         | 示例          |
| -------- | ---- | ------ | ------------------------------------------------------------ | ------------- |
| name     | 是   | string | 包名                                                         | openjdk-devel |
| provider | 是   | string | green代表绿色安装，auto代表从yum或apt源自动安装              | green         |
| version  | 是   | string | 版本。provider字段为auto时该字段无效。                       | 1.0.1         |
| rootdir  | 否   | string | 自定义根路径，默认 /usr/opt。provider字段为auto时该字段无效。 | /usr/opt      |
| force    | 否   | bool   | 覆盖已有版本（默认 true）；如传 false 且探测到已安装其他版本，返回127 | true          |

**tips：**

​		provider：green的情况下，安装软件时会提前检测该版本的软件是否存在，若存在。则会直接掉过软件安装操作，并忽略rootdir字段。

​		**在此情况下，软件操作并没有在指定目录完成安装。**

