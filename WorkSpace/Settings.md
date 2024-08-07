# WorkSpace设置
---
用于配置WorkSpace的头像，`名称`,`备注`,`仓库类型`,`仓库地址`,`仓库token`,`仓库id`

## 编辑/新建/切换WorkSpace

###  编辑当前WorkSpace信息

当前WorkSpace下点击左侧菜单栏`WorkSpace设置`-->`编辑`。

![图 1](../images/edit_workspce.png)  

可修改WorkSpace的名称和描述，并上传喜欢的头像，点击`保存`。

| 功能 | 解释 | 
| :-----| :---- | 
| WorkSpace 名称 | 必填 | 
| WorkSpace 描述 | 选填 | 
| 仓库类型 | 选填， 目前支持的仓库类型：gitlab 和 github| 
| 仓库地址 | git仓库的url，如：`http://172.30.81.xxx:8000`| 
| 仓库token | git仓库的Access Token ，获取方式见下方的tips| 
| 仓库ID或目录 | git仓库的ID或目录 | 
| 分支 | git仓库分支 | 
| 测试仓库链接 | git仓库配置完成后，点击测试是否成功 |
| WorkSpace 图标 | 单击上方的图标修改并上传新的图标 | 

<span id="git"></span>

### 如何获取gitlab的Access Token？

1. 登录gitlab，点击`Settings`-->`Access Tokens`，并按照页面填写信息和勾选权限后，点击下方的绿色按钮

    ![图 2](../images/ack_tk.png)  

2. Token创建成功，复制使用

    ![图 3](../images/ack_token_gen.png)  

### 如何配置github？

1.登录GitHub，点击右上角的头像选择`Settings`

![](./../images/1679304801747.png)

2.左侧菜单点击`Developer settings`

![](./../images/1679304287856.png)

3.点击`Personal access tokens`-->`Tokens(classic)`-->右上角按钮`Generate new tokens(classic)`

![](./../images/1679304460665.png)

4.填写Note（必填）、选择过期时间Expiration，并勾选权限范围，鼠标滑到页面最下方点击绿色按钮`Generate token`

![](./../images/1679304643450.png)

![](./../images/1679304688101.png)

5.复制Access Token

![](./../images/1679304738391.png)

6.复制仓库ID或目录

![](./../images/1679306218178.png)

7.将上面拿到的Access Token和仓库目录以及分支信息填入WorkSpace的仓库设置，点击按钮`测试仓库链接`，如配置正确系统会提示连接成功，点击保存即可。

![](./../images/1679305311829.png)


## 删除

![图 3](../images/delwork.png)  

> [!Warning]
> 注：删除WorkSpace时，如该WorkSpace下如存在任何文件或使用记录，需将所有内容删除后才能删除。















