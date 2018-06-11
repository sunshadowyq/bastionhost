# SFTP协议运维 {#task_zhx_clm_xdb .task}

运维工程师、云盾堡垒机管理员、持有阿里云账号的管理员。

运维员通过本地的客户端工具登录云盾堡垒机，再访问目标主机。

**说明：** 您必须先在本地安装好支持SFTP协议的运维工具，如：Xftp、WinSCP、FlashFXP等。

下文以Xftp为例介绍运维登录流程：

1.   打开Xftp工具，在登录窗口中输入云盾系统的IP、端口号60022、用户名、密码。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12746/4087_zh-CN.png)

    **说明：** 如果管理员在云盾堡垒机中配置了用户公钥，则用户可以通过公私密钥对的方式登录，无需输入密码。 在用户身份验证设置中，选择**Public Key**，输入云盾堡垒机用户名，选择对应的私钥。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12746/4088_zh-CN.png)

2.   单击 **确定**，连接云盾堡垒机。 

    **说明：** 如果管理员启用了双因子登录，将会弹出双因子口令对话框，请输入您手机上收到的6位数字。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12746/4089_zh-CN.png)

    **说明：** 云子帐号账户使用MFA进行二次验证。

3.   成功登录云盾堡垒机后，在右侧可以看到已授权的服务器主机列表。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12746/4090_zh-CN.png)

4.   双击需要操作的服务器，进入该服务器主机的目录，即可进行文件传输操作。 

    **说明：** SFTP运维必须将有效凭据添加到相应授权组，否则无法登入ECS。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12746/4091_zh-CN.png)

    **说明：** 主机列表中第一个目录是为了转码使用，如果主机列表编码有问题，可双击第一个目录后刷新进行转码。


