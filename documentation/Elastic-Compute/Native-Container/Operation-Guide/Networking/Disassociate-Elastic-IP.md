# 解绑弹性公网IP

## 操作步骤

容器实例与Pod的弹性公网IP解绑流程除第一步其余流程完全一致
1a. 打开京东云控制台，选择【弹性计算】-【原生容器】-【容器实例】进入原生容器实例列表页。 
1b. 打开京东云控制台，选择【弹性计算】-【原生容器】-【Pod】进入Pod实例列表页。
2. 在实例列表中选择需要解绑弹性公网IP的实例，点击名称进入详情页。
3. 点击【弹性网卡】Tab，选择需要解绑弹性公网IP的弹性网卡，找到需要解绑的内网IP，点击【解绑公网IP】按钮。
4. 在弹出的二次确认窗中，点击【确定】。

此外，您还可以：

* 在实例列表页面操作对实例主网卡主内网IP解绑弹性公网IP，操作步骤如下：
	1a. 打开京东云控制台，选择【弹性计算】-【原生容器】-【容器实例】进入原生容器实例列表页。  
	1b. 打开京东云控制台，选择【弹性计算】-【原生容器】-【Pod】进入Pod实例列表页。  
	2. 在实例列表中选择需要对主网卡主内网IP解绑弹性公网IP的实例，点击解绑公网IP。
	3.  在弹出的二次确认窗中，点击【确定】。
	 
* 从弹性网卡控制台进行解绑操作，详细步骤请参见[弹性网卡侧解绑公网IP](../../../../Networking/Elastic-Network-Interface/Operation-Guide/Private-IP-Management/Disassociate-Elastic-IP.md)。

## 相关参考

[弹性网卡侧解绑公网IP](../../../../Networking/Elastic-Network-Interface/Operation-Guide/Private-IP-Management/Disassociate-Elastic-IP.md)
