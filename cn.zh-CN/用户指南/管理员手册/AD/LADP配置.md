# AD/LADP配置 {#concept_zr3_154_ydb .concept}

本文受众范围：云盾堡垒机管理员、持有阿里云帐号的管理员。

云堡垒机与AD/LDAP服务器对接，可将AD/LDAP服务器用户同步进堡垒机，作为堡垒机用户使用。 此功能需具有部署好的AD/LDAP环境，且保证堡垒机至服务器网络可达。

## AD域设置 {#section_jr2_d54_ydb .section}

1.  登录堡垒机web管理页面，进入**用户****AD/LDAP设置**，将模式调整为**AD** 。
2.  在页面内依次填入**AD服务器IP、端口**、**要同步的用户所在的组织**、**域名**、**域用户账号、密码** ，以及**姓名**、**邮箱**、**手机号码**等属性字段名称（带\*为必填项）。

    **Note:** 需保证填入的用户账号有权限访问Base DN 。

    **Note:** 若拉取的用户无手机号码属性，或内容为空，同步下来的用户手机号字段将置空，若打开设置中的**二次认证**选项，同步的用户将无法登录堡垒机 。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12736/4141_zh-CN.png)

3.  配置完成后，单击页面下方**测试连接**，若结果如图所示，单击**保存设置**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12736/4142_zh-CN.png)

    若结果如下图所示，则证明堡垒机与AD服务器之间网络或端口不通，需对网络进行排查。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12736/4144_zh-CN.png)

      

4.   配置完成后，进入堡垒机**用户** \> **用户管理**菜单，单击右上方**导入AD/LDAP用户**，可将Base DN中的用户加入至堡垒机。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12736/4145_zh-CN.png)

5.  用户加入堡垒机后，可以运维登录操作。

## LDAP设置 {#section_cvg_s54_ydb .section}

1.  登录堡垒机Web管理页面，进入**用户** \> **AD/LDAP设置**菜单，将模式调整为**LDAP**。
2.  在页面依次填入LDAP服务器信息。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12736/4146_zh-CN.png)

3.  测试连接通过后，保存设置。
4.  参考AD域设置，导入用户，并使用LDAP用户进行认证登录。

