# RDP协议运维 {#task_egf_clm_xdb .task}

本文受众范围：运维工程师、云盾堡垒机管理员、持有阿里云帐号的管理员。

运维人员需要通过本地的客户端工具登录云盾堡垒机，再访问目标服务器主机进行运维操作。下文以 Windows 系统自带的 远程桌面连接工具（Mstsc）为例说明运维登录流程：

1.   在本地 Windows 系统主机中打开远程桌面连接工具（Mstsc）。 
2.   输入云盾堡垒机的 IP 和 RDP 端口号（RDP 端口号默认为 63389）：`< IP >:63389`，单击**连接**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12745/4080_zh-CN.png)

3.   在是否信任此远程连接？对话框中，单击**连接**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12745/4081_zh-CN.png)

4.   在无法验证次远程计算机的身份。是否仍要连接？对话框中，单击**是**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12745/4082_zh-CN.png)

5.   在云盾堡垒机登录窗口中，输入云盾堡垒机的用户名和密码。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12745/4083_zh-CN.png)

6.   单击**登录**，登录云盾堡垒机。 

    **Note:** \*\*如果管理员启用了双因子认证登录，将会弹出双因子口令对话框，请输入您手机上收到的6位数字。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12745/4084_zh-CN.png)

    **Note:** 云子帐号使用MFA进行二次验证。

7.   成功登录云盾堡垒机后，进入资产管理界面，双击您需要登录的已授权服务器主机进行登录。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12745/4085_zh-CN.png)

8.   进入目标服务器主机的登录界面，输入主机的账户和密码。 

    **Note:** 若已在堡垒机中添加凭据，且该凭据添加到该用户的授权组中，则无需输入主机账户密码可直接登录主机。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12745/4086_zh-CN.png)

9.   按Enter键即可登录服务器主机进行运维操作。 

