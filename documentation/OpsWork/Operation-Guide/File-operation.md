# 文件操作 schema
| 字段     | 必须 | 类型   | 含义                                                         | 示例                                                         |
| -------- | ---- | ------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| path     | 是   | string | 要操作的文件绝对路径                                         | /usr/opt/openjdk.tar.gz                                      |
| action   | 是   | string | _enum_: `copy`、`delete`、`update`、`create`                           | copy                                                         |
| source   | 否   | string | 如果 action=copy，不能为空，可以是本机绝对路径或下载地址<br>支持OSS下载。 | https://download.java.net/java/GA/jdk13/5b8a42f3905b406298b72d750b6919f6/33/GPL/openjdk-13_linux-x64_bin.tar.gz |
| force    | 否   | bool   | 如果 action=copy，表示是否覆盖已有的同名文件，默认 true      | true                                                         |
| content  | 否   | string | 如果 action=update，不能为空，要更新的文件内容               | hello world!                                                 |
| backup   | 否   | bool   | 如果 action=copy/update 且设为 true，则将原同名文件重命名为 "filename.bak.${timestamp}" 形式，默认 false | false                                                        |
| md5check | 否   | string | 如 action=copy/update 且非空，则进行 md5sum 检查             | 1d9af91cd042b403e75badd110ccf751                             |
| mode     | 否   | string | 如 action=copy/update 且非空，执行 chmod                     | 0644                                                         |
| owner    | 否   | string | 如 action=copy/update 且非空，执行 chown                     | work                                                         |
| group    | 否   | string | 如 action=copy/update 且非空，执行 chown                     | root                                                         |