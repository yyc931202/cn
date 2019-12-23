# 插件安装

1. 安装VScode

   > https://code.visualstudio.com/Download

2. 安装插件：

   VScode的位置在：

3. 安装完成后需要输入AK/SK

   第一次使用插件时需要输入AK/SK。

   进入京东云控制台-账号管理-Access Key管理，创建并获取Access Key。

   ![AK管理.png](../../../../image/IDE-plugin/2.png)

   在File-Preferences-Settings-Extensions-JDCloud中填入AK/SK，并设置要使用的region，目前仅支持单region。填写AK/SK之后可以直接进行连接测试。

   ![AK管理2.png](../../../../image/IDE-plugin/vscode6.png)

目前IDE插件支持VScode，并从内置的插件市场中直接安装。
4. public key导入

   windows存放public key的位置是：

   > C:\Users\XXXXX\\.ssh

   在该目录下，使用命令ssh-keygen生产密钥。并将public key导入到代码托管中。具体位置在：

   代码托管-管理-SSH key管理，参考文档：

   > https://docs.jdcloud.com/cn/codecommit/ssh-key