**安装agent**

目前仅支持Linux中安装Agent。此agent与云部署产品中的agent为同一款软件，安装一次即可。

**安装**

1）在购买云主机时可以直接安装agent。

在购买云主机的界面中，使用高级选项，并编写agent安装命令即可。如图所示：

 ![](../../../../image/opswork/install1.PNG)


注意：要分两行，第一行的内容是：“#!/bin/bash” 第二行是agent安装命令。

2）在已有的云主机中

手动安装，请登录到待安装/异常主机，执行以下命令

```shell
curl -fsSL http://deploy-code-vpc.jdcloud.com/dl-ifrit-agents/install_deploy | bash
```

以向华北-北京地域的云主机安装Agent为例，

 ![](../../../../image/opswork/install2.PNG)

**获取Agent状态**

Agent状态为“正常”、“异常”两种。

**版本升级**

当Agent发布新版本时，将自动进行版本升级，且更新过程对用户透明，不会影响云部署的功能使用。
