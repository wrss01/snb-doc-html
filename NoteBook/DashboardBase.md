# 基础仪表板配置

---

基础仪表板是一种简化的仪表板应用，主要用于定期展示数据图表和文字说明。通过Notebook调度，仪表板可以定期生成和更新，而无需用户进行页面交互。

## 配置和特点

1. **图表展示**：
   - 提供多种图表类型（如柱状图、折线图、饼图等）以可视化数据。
   - 图表用于展示关键数据指标和趋势，帮助用户直观地理解数据变化。

2. **文字展示**：
   - 在图表旁提供文字说明，以解释数据的含义和关键发现。
   - 文字展示可以包括标题、注释和简要分析。

3. **Notebook调度**：
   - 通过Notebook进行数据处理和图表生成。
   - 设定Notebook定期调度任务，自动生成和更新仪表板内容，确保数据的实时性和准确性。

4. **无页面交互**：
   - 仪表板主要用于展示数据，无需用户进行页面交互。
   - 适合于需要定期查看数据报告的用户，例如管理层和决策者。

通过以上步骤，可以实现一个基础的仪表板，用于定期展示数据，无需用户进行页面交互，适合于需要定期查看数据报告的用户群体。

![图 0](../images/426a75ba60aa205938e2fd63314f7e55ea3c0bfae86f6cbffb8f5fbac3b6192f.png)  

---

* **配置仪表板步骤：**

  - 1.添加仪表板单元 （包括Notebook基础单元格(输入，输出)、UI模版
  - 2.编辑仪表板单元的基础属性（在相对仪表板左上顶点的x、y轴位置、单元的宽、高、层级基础属性）
  - 3.删除仪表板单元
  - 4.预览/保存仪表板
  - 5.发布/更新仪表板
  
---

## 0. 仪表板节点命名
 <p>仪表板的每个单元都会被命名。</p><br>

 <p>演示视频</p>
  
<video tabindex="0" controls class="video-stream html5-main-video" controlslist="nodownload" style="width: 1200px; height: 620px; left: 0px; top: 0px;">
  <source src="../assets/dashboard/2024062011584.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

## 1. 添加仪表板单元（包括Notebook基础单元格(输入，输出)、UI模版）
### 1.1 添加Notebook单元格到仪表板中
  <p>点击Notebook左侧radio框，选中的Notebook的的input和output会自动排版到仪表板中。</p>
  
![图 0](../assets/dashboard/2024-06-17 11.07.54.png) 

  演示操作：
![图 1](../assets/dashboard/2024-06-17 10.02.55.gif) 

### 1.2 添加UI模版到仪表板中
  <p>点击仪表盘左侧的模版区域，添加UI模版到仪表盘中。</p>
  <p>UI模版类型：<b style="color:#3793EF">标题模版、背景模版、文本模版、装饰模版、主题模版。</b></p>
  <p>模版定义请跳转<a href="/WorkSpace/DashboardTemplates.md#jump_1">模版定义</a></p>
  
![图 2](../assets/dashboard/2024-06-17 11.27.40.png) 

  演示示例：
![图 3](../assets/dashboard/2024-06-17 10.51.00.gif) 

---

## 2.编辑仪表板节点的基础属性（在相对仪表板左上顶点的x、y轴位置、单元的宽、高、层级基础属性）
 双击仪表板上需要编辑的节点、右侧弹出抽屉弹框，可以修改单元格基础属性（宽高、位置、层级等）
 同时也支持鼠标操作：<br>

<p>改变<b style="font-weight:600;color:blue;display:inline-block">(宽、高)</b>: 鼠标移入要修改的单元，拖动线框矩形柄则完成相对应的编辑操作。</p>
<p>改变<b style="font-weight:600;color:blue;display:inline-block">(位置)</b>: 鼠标移入要修改的单元，鼠标右击不放，移动鼠标则完成相对应的移动操作。</p>

![图 4](../assets/dashboard/2024-06-17 13.25.35.png) 

 演示示例
![图 5](../assets/dashboard/2024-06-17 14.37.36.gif) 

---

## 3.删除仪表板单元
  删除如下图：<br>
    a:鼠标移入要删除的单元，点击单元右上角的删除按钮。<br>
    b:点击Notebook 选中按钮，则也会删除右侧的单元。<br>
![图 6](../assets/dashboard/2024-06-17 14.46.56.png) 

---
## 4.预览/保存仪表板

设计完成后，可以先点击 <img src="../images/5d90b2f9bb7e02451e4de36754818428ba41b3a17cc59002834fead908b4afaf.png"  style="display: inline-block;padding:0px;border:0px"  /> 查看效果。

![图 20](../assets/dashboard/2024-06-11 17.07.20.gif)  

## 5.发布/更新发布

点击<img src="../images/2c7204369c33a2052cc32653e373563e1ca4bd1fab1ff863c7244a73fd026b42.png"  style="display: inline-block;padding:0px;border:0px"  /> 可以发布正式的仪表板链接。

用户可以直接通过打开链接在网络浏览器中实时查看和互动这个仪表板。此外，这个链接也可以轻松地嵌入到其他应用程序中，为您的业务流程提供即时的数据洞察。如果需要，您也可以将此链接投射到大屏幕上，以便在团队会议或演示中展示数据。这种多元化的展示方式为数据分析带来前所未有的灵活性和方便性，让您可以随时随地获取到最新、最准确的业务洞察。

每当您对仪表板进行更改时，您的仪表板都不会自动重新发布。您需要在更改完之后重新保存并 “更新发布”。

> [!NOTE]
> 已发布的仪表板的 URL 在更新发布后保持不变，因此您不必担心重新共享或在应用中修改URL的问题。

#更多<a href="/NoteBook/DashboardInterac.md">高级设置</a>

<p>以上就是设计/保存/发布基本仪表板的演示流程。发布的仪表板都在 <b> <a href="/WorkSpace/Dashboard.md">报告和看板</a> </b>列表中 </p>

