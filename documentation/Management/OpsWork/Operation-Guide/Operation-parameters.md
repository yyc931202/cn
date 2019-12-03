# 操作基础参数

基础参数是每一个操作都会带有的参数。

| 字段    | 必须 | 类型        | 含义                                                         | 示例                                                |
| ------- | ---- | ----------- | ------------------------------------------------------------ | --------------------------------------------------- |
| name    | 是   | string      | 操作名，要符合 C 语言变量命名规范，可以结合 `when` 来判断本操作返回值、stdout、stderr 等信息 | prepare_install                                     |
| kind    | 是   | string      | 操作类型，_enum_: `package`-软件安装 `file`-文件操作 `command`-自定义命令 | package                                             |
| runas   | 否   | string      | 以用户身份执行，默认 root                                    | root                                                |
| timeout | 否   | int         | 超时时间（s），默认300                                       | 300                                                 |
| retry   | 否   | int         | 失败重试次数，默认0                                          | 0                                                   |
| exit    | 否   | bool        | 失败退出，默认 true<br> 若为false则失败跳过该操作                                     | true                                                |
| when    | 否   | object list | 满足此条件才执行本操作，默认空                               | key: verify.code <br> operator: "=" <br> value: "0" |

**when 对象定义**

| 字段     | 必须 | 类型   | 含义                                                         | 示例                 |
| -------- | ---- | ------ | ------------------------------------------------------------ | -------------------- |
| connect  | 否   | string | 逻辑连接， _enum_: `and`、`or`，默认空，左优先               |                      |
| key      | 是   | string | 要比较的变量名，内置支持 `$name.code`获取已执行完成操作的返回值 | prepare_install.code |
| operator | 是   | string | _enum_: <br>`>`、`<`、`=`、`>=`、`<=`、`!=`、`<`<br>`in`-key 字符串包含于 value 字符串<br>`notIn`-key 字符串不包含于 value 字符串<br>`contain`-key 字符串包含 value 字符串<br>`notContain`-key 字符串不包含 value 字符串 | notIn                |
| value    | 是   | string | 要比较的值，`$name.code`返回值只有0，1.代表正常结束和异常结束 | 0                    |
