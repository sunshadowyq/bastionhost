# SSH协议运维 {#task_mbr_blm_xdb .task}

本文受众范围：运维工程师、云盾堡垒机管理员、持有阿里云帐号的管理员。

运维人员需要通过本地的客户端工具登录云盾堡垒机，再访问目标服务器主机进行运维操作。

**说明：** 请确认在本地主机已安装支持 SSH 协议的运维工具，如 Xshell、SecureCRT、PuTTY 等工具。

下文以Xshell工具为例，介绍运维登录流程：

1.   打开Xshell工具，在连接设置中输入云盾堡垒机的IP和SSH端口号（SSH端口号默认为 60022）。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12744/4074_zh-CN.png)

2.   在用户身份验证设置中输入云盾堡垒机的用户名和密码。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12744/4075_zh-CN.png)

    **说明：** 如果管理员在云盾堡垒机中配置了用户公钥，则用户可以通过公私密钥对的方式登录，无需输入密码。在用户身份验证设置中，选择**Public Key**，输入云盾堡垒机用户名，选择对应的私钥。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12744/4076_zh-CN.png)

3.   单击**确定**，连接云盾堡垒机。 
4.   （可选）如果管理员启用了双因子认证登录，将会弹出双因子口令对话框，请输入您手机上收到的6位数字。 

    **说明：** 云子帐号账户使用MFA进行二次验证。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12744/4077_zh-CN.png)

5.   成功登录云盾堡垒机后，进入资产管理界面。通过键盘上的上、下箭头选择您想要进行运维的服务器主机。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12744/4078_zh-CN.png)

6.   按 Enter 键即可登录目标服务器主机进行运维操作。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12744/4079_zh-CN.png)


