# Mac系统运维 {#concept_o3c_blm_xdb .concept}

本文受众范围：运维工程师、云盾堡垒机管理员、持有阿里云帐号的管理员。适用于使用Mac电脑通过本地客户端工具登录云盾堡垒机，再访问目标主机的运维工程师。

## SSH协议运维 {#section_m1n_nm4_ydb .section}

以MAC自带的命令行终端APP为例：

1.  打开命令行终端APP。
2.  输入以下命令：`ssh 云盾堡垒机用户名@云盾堡垒机IP -p60022`

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4107_zh-CN.png)

3.  输入云盾堡垒机密码。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4108_zh-CN.png)

    **Note:** 如果管理员启用了双因子登录，将会弹出短信口令对话框，请输入您手机上收到的6位数字。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4109_zh-CN.png)

4.  回车后进入资产管理界面，用上下键选择已授权的资产。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4110_zh-CN.png)

5.  回车后进入目标主机界面，进行运维操作。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4111_zh-CN.png)


## RDP协议运维 {#section_l1f_tm4_ydb .section}

以远程桌面连接APP为例：

1.  打开命令行终端APP。
2.  输入云堡垒机的IP：`63389`

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4112_zh-CN.png)

3.  单击**连接**后，弹出是否仍要连接此计算机？

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4113_zh-CN.png)

4.  单击**连接**后，进入云堡垒机登录窗口，输入：`云堡垒机的用户名和密码`

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4114_zh-CN.png)

    **Note:** 如果管理员启用了双因子登录，将会弹出短信口令对话框，请输入您手机上收到的6位数字。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4115_zh-CN.png)

5.  单击**登录**后进入资产管理界面：用鼠标选择已授权的资产，或者通过搜索框搜索主机信息。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4116_zh-CN.png)

6.  双击之后即可进入目标主机进行运维操作。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4117_zh-CN.png)


## 文件传输运维 {#section_xcm_cn4_ydb .section}

**客户端访问堡垒机，再选择ECS方式运维**

以SecureFX工具为例：

1.  打开SecureFX工具。
2.  新建连接，输入云堡垒机IP，端口60022，账户信息。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4118_zh-CN.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4119_zh-CN.png)

3.  单击**连接**后，按提示输入堡垒机密码。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4120_zh-CN.png)

    **Note:** 如果管理员启用了双因子登录，将会弹出短信口令对话框，请输入您手机上收到的6位数字。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4121_zh-CN.png)

    **Note:** 云子账号使用MFA进行二次验证。

4.  单击<登录\>后进入资产管理界面，请双击选择转码目录（忽略报错信息），再右键选择刷新，进行转码。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4122_zh-CN.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4123_zh-CN.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4124_zh-CN.png)

5.  转码后资产列表显示正常。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4125_zh-CN.png)

6.  选择目录主机双击进入后，需要先退回到根目录，再右键选择刷新后，进入主机，即可进行运维操作。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4126_zh-CN.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4127_zh-CN.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4128_zh-CN.png)

7.  可正常进行上传下载操作。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4129_zh-CN.png)


**SSH网关+filezilla直连ECS方式运维**

1.  打开命令行终端APP。
2.  输入`ssh -T -N -D 127.0.0.1:1080 -oport=60022 用户名@堡垒机IP`，按Enter键。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4130_zh-CN.png)

3.  输入云盾堡垒机密码，按Enter键连接到堡垒机，不要关闭该窗口。

    **Note:** 如果管理员启用了双因子认证登录，将会提示输入双因子口令，请输入您手机上收到的6位数字。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4131_zh-CN.png)

    **Note:** 云子账号使用MFA进行二次验证。

4.  打开filezilla客户端，进入设置页面。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4132_zh-CN.png)

5.  单击**通用代理**，选择 SOCKS5，设置代理主机：127.0.0.1，端口：1080，单击**确定**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4133_zh-CN.png)

6.  打开站点管理器，输入需要连接运维的服务器IP，设置端口：22；登录类型：正常；输入服务器用户名、密码。

    **Note:** 若相关授权组中已添加正确凭据，则无需输入密码。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4134_zh-CN.png)

7.  单击**连接**，弹出窗口选择**确定**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4135_zh-CN.png)

8.  进入远程服务器后，即可进行文件传输运维，堡垒机可正常审计。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12747/4136_zh-CN.png)


