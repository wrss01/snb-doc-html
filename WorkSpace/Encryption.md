# 变量密保箱
---
变量密保箱的用处：

1. 将敏感值（如API令牌或重要密码）加密

2. 作为全局变量使用


建立密保/变量后，用户可以在NoteBook中通过名称访问密保/变量的值，而不是通过明文或者硬编码的方式进行调用。

![图 1](/assets/workspace/Xnip2024-06-28_13-40-03.png)  

## 新建密保/变量

点击右上角的`新建变量`,输入`名称（英文）`和`值`。

如需加密请勾选`加密`，配置完成后点击提交。

<!-- ![图 2](../images/newpass.png)   -->
![图 1](../images/8986f6ae307741256cee95ef3bf2aa6d090afbbbbb290de876d009d134804352.png)  

 

## 密保/变量列表

在列表处对已有的密保/变量进行编辑或删除：

<!-- ![图 4](../images/%E5%AF%86%E4%BF%9D%E7%AE%B1%E5%88%97%E8%A1%A8.png)   -->
![图 2](../images/1eab3c581d72249ba042a2e6b3a89553dfd97950ce71b4b344de95df8b356a48.png) 

## 密保/变量的使用

### 复制密保/变量

<p>单击名称<img src="../images/%E5%A4%8D%E5%88%B6icon.png"  style="display: inline-block;padding:1px; background: white;border:0px;" />复制密保/变量</p>

<!-- ![图 5](../images/%E5%A4%8D%E5%88%B6%E5%AF%86%E4%BF%9D.png)   -->

![图 3](../images/fefdace323db07437d0dec76ba3dcadf1728b349a9945af912b8b2d26826cb35.gif)  

### 使用密保/变量

- 在Python单元格中使用密保：

![picture 1](../images/%E5%BC%95%E7%94%A8%E5%AF%86%E4%BF%9D.png)  

- 在MarkDown中使用变量：

![图 3](../images/passmd.png)  

- 作为CSS样式使用:

详见<a href="../NoteBook/Markdown.md/#mdsecret" title="设置MarkDown的标签样式（高级用法）">设置MarkDown的标签样式（高级用法）</a> 


