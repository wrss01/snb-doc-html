# WorkSpace成员
---
团队成员在相同的WorkSpace下开始协同工作。

![图 7](/assets/workspace/Xnip2024-06-28_16-11-04.png)  

## 邀请团队成员

单击页面右上角的<img src="../images/dbe125f81ed8e0b3ddb2b6c93e077acc7b6cc9c053b97c022c9621a0d7af1432.png"  style="display: inline-block;padding:0px;border:0px"  />按钮转到邀请页面，填写受邀请用户的Email并设置其角色（编辑者/查看者），点击`发送邀请`：

![图 14](../images/76ee534439740d1adc3f27de09fdfbdd2d0d9e7805153ca9bc5d205689648192.png)  


发送邀请后，被邀请的团队成员状态将显示为"邀请中..."：

![图 3](../images/6b651e876bfd5155f63c947d7ba1d3b0f46e7cff9b59e75d74fb70d76bfb2c9c.png)  

被邀请成员点击邮件确认后状态切换为"正常"，此时被邀请人加入该WorkSpace并获得相应的权限参与到协同工作。

![图 4](../images/35e5c77dbbd54089997b23c154c21a52476554c8c88ea7182d6a4809edab0f6c.png)  

> [!NOTE|style:flat]
> 受邀请用户需要先成功注册SNB的账号，否则无法接收邀请：

<!-- ![图 6](../images/accounterror.png)   -->
![图 15](../images/5a661936b6b49e44e429741af9f06208b7b8427a7e54f187fb06d9d3b51c9173.png)  



## 修改角色权限

- 编辑者：拥有除`WorkSpace设置`以及环境资源配置外，其他一切该WorkSpace拥有者的权限（查看、新建、编辑、删除）
- 查看者：看到的功能与编辑者一致，但只拥有查看权限

管理员可以对状态正常的成员修改角色权限：

<!-- ![图 15](../images/ac845f080f0c98fb11eb16b6cc583f54ce0cabf21e2806f07811cd57cdd74d8b.png)   -->
![图 5](../images/ac845f080f0c98fb11eb16b6cc583f54ce0cabf21e2806f07811cd57cdd74d8b.png)  


## 移除成员

管理员可以在成员列表中点击`操作`-`移除`将已加入的成员移除出团队。

被移除的成员将无法看到该WorkSpace，如需重新访问，需被重新邀请。

<!-- ![图 16](../images/a3054855578a9b9b87f73b44d7480afc4188374c8af24a8c75d02cc36420f3e8.png)   -->
![图 6](../images/a3054855578a9b9b87f73b44d7480afc4188374c8af24a8c75d02cc36420f3e8.png)  

## 禁用

管理员可以对成员的状态进行修改（禁用）。

被禁用的成员将无法看到该WorkSpace直到状态被修改为正常状态。

<!-- ![图 17](../images/408c31bd962f63a4b91285a795d0be699ec28a740d1933ac6e0b3ac553266ff5.png)   -->
![图 7](../images/408c31bd962f63a4b91285a795d0be699ec28a740d1933ac6e0b3ac553266ff5.png)  

## 实时协作

<span id="teamw"></span>


SNB支持实时协作模式，允许团队成员实时跟踪代码的编写进度。

在这个模式下，首位进入NoteBook的团队成员将获得编辑权，其他成员则可以即时查看其编码过程。这一设计特点不仅便于团队间的沟通协作，更使**教学过程变得直观易懂：学生可以清晰地看到老师的编程逻辑，从而更好地吸收知识。**

SNB的实时协作模式通过促进信息同步，极大地提升了用户的交互体验。


![图 13](../images/19571b74bff84280b0c566f16d0efbabe396972e1477c76a58e46178884d8064.png)  

> [!TIP]
> 所有进入NoteBook的团队成员，头像将出现在NoteBook的右上角。
