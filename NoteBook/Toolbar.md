# 工具栏
---

工具栏提供对NoteBook的一系列扩展操作

![图 1](../images/toobar%E7%9A%84%E6%93%8D%E4%BD%9C.png)  

功能概览

<table>
  <tr>
    <th>主菜单</th>
    <th>二级菜单</th>
    <th>功能介绍</th>
  </tr>
  <tr>
    <td rowspan="6">文件</td>
    <td>最近打开的</td>
    <td>查看最近编辑过的NoteBook文档（点击可在新的标签页打开）</td>
  </tr>
  <tr>
    <td>分享</td>
    <td>功能同NoteBook右上角的`分享` 按钮，分享的操作详见<a href="./Share.md" title="分享">分享</a></td>
  </tr>
  <tr>
    <td>重命名</td>
    <td>点击修改NoteBook上方的文件名</td>
  </tr>
  <tr>
    <td>导出.ipynb</td>
    <td>导出snb格式文件（SmartNoteBook专用格式）</td>
  </tr>
  <tr>
    <td>导出.snb</td>
    <td>导出.ipynb文件(兼容Jupyter NoteBook)</td>
  </tr>
  <tr>
    <td>保存</td>
    <td>手动保存NoteBook（除此之外提供每30s自动保存）</td>
  </tr>
  <tr>
    <td rowspan="11">工具</td>
    <td>保存版本</td>
    <td>保存NoteBook版本，该功能参见侧边栏的<a href="./Sidebar.md/#sv" title="保存版本">版本列表-->保存版本</a></td>
  </tr>
  <tr>
    <td>数据资源</td>
    <td>打开`数据资源`，该功能参见侧边栏的<a href="./Sidebar.md/#ds" title="数据资源">数据资源</a></td>
  </tr>
  <tr>
    <td>计算环境</td>
    <td>打开`计算环境`，该功能参见侧边栏的<a href="./Sidebar.md/#env" title="计算环境">计算环境</a></td>
  </tr>
  <tr>
    <td>导航目录</td>
    <td>打开`导航目录`，该功能参见侧边栏的<a href="./Sidebar.md/#idx" title="导航目录">导航目录</a></td>
  </tr>
  <tr>
    <td>变量预览</td>
    <td>打开`变量预览`，该功能参见侧边栏的<a href="./Sidebar.md/#vr" title="变量预览">变量预览</a></td>
  </tr>
  <tr>
    <td>版本列表</td>
    <td>打开`版本列表`，该功能参见侧边栏的<a href="./Sidebar.md/#sv" title="保存版本">版本列表</a></td>
  </tr>
  <tr>
    <td>软件包</td>
    <td>打开`软件包`，该功能参见侧边栏的<a href="./Sidebar.md/#pk" title="软件包">软件包</a></td>
  </tr>
  <tr>
    <td>代码片段库</td>
    <td>打开`代码片段库`，该功能参见侧边栏的<a href="./Sidebar.md/#cd" title="代码片段库">代码片段库</a></td>
  </tr>
  <tr>
    <td>终端</td>
    <td>打开命令行界面与服务器交互</td>
  </tr>
  <tr>
    <td>模型视图</td>
    <td>分析代码中的变量关系生成关系图<a href="/NoteBook/Graph.md" title="模型视图">模型视图</a></td>
  </tr>
  <tr>
    <td>CELL宽度</td>
    <td>设置notebook页面，cell单元格的宽度窄、中和宽三种</td>
  </tr>
  <tr>
    <td rowspan="2">Kernel</td>
    <td>中断Kernel</td>
    <td>中断运行正在运行的代码</td>
  </tr>
  <tr>
    <td>重启Kernel</td>
    <td>重新启动Kernel（例如某些package安装后需要重启）</td>
  </tr>
  <tr>
    <td rowspan="6">运行</td>
    <td>全部运行</td>
    <td>运行NoteBook下所有的单元格（按照Sheet顺序）</td>
  </tr>
  <tr>
    <td>运行当前及上方所有单元格</td>
    <td>运行选中的单元格及之前所有单元格的代码（当前Sheet内）</td>
  </tr>
  <tr>
    <td>运行当前及下方所有单元格</td>
    <td>运行选中的单元格及之后所有单元格的代码（当前Sheet内）</td>
  </tr>
  <tr>
    <td>运行当前sheet的所有单元格</td>
    <td>运行当前sheet的所有单元格</td>
  </tr>
  <tr>
    <td>清除全部输出</td>
    <td>清除NoteBook中所有单元格的输出（全部Sheet）</td>
  </tr>
    <tr>
    <td>隐藏全部输入</td>
    <td>分享时隐藏NoteBook中所有单元格的输入（全部Sheet）</td>
  </tr>
  <tr>
    <td rowspan="2">帮助</td>
    <td>快捷键</td>
    <td>详见<a href="./Shortcuts.md" title="快捷键">快捷键</a></td>
  </tr>
  <tr>
    <td>帮助手册</td>
    <td>打开帮助手册</td>
  </tr>
</table>


## 终端

用户通过终端连接至容器，使用bash命令查看和操作服务器的资源（慎用）。

![图 2](../images/termi.png)  

## 模型视图

分析代码中的变量关系生成关系图，直观展示NoteBook的整体分析脉络以及单元格间的相互关系。

- 可解释性：容易看到各单元格如何相互关联，查看整个NoteBook代码逻辑的“流动”，是跟踪复杂逻辑的可视化“思维导图”。

- 性能：在模型开发过程中，这种DAG模型几乎不会产生额外的性能开销，对性能无任何影响。
- 交互方面：
  - 点击模型视图中的代码框可以快速定位到左侧的单元格
  - 代码框右下角的图标可识别代码类型
  - 线条箭头的指向代表了代码逻辑的流向，线条中间为上下关联的变量
  - 模型视图中的代码框可以任意拖动

右上角支持打开/关闭小地图。小地图显示模型视图的预览，并且支持鼠标在小地图拖动控制显示的区域（对于模型视图显示面积过大的情况会很有帮助）

<!-- ![图 3](../images/gengraph.png)   -->
<!-- ![图 2](d:\00%20%E9%A1%B9%E7%9B%AE%E9%9B%86%E5%90%88\snb%E6%93%8D%E4%BD%9C%E6%89%8B%E5%86%8C%E4%B8%93%E9%A1%B9\snb_gitbook\images\f954e878763ace910f28057d809abad3be86a645a3f65db048c84389dcacca31.png)   -->

![图 1](../images/9f29ab8c8536f0fed522ad9965a300656397e3ed43d5aacb8a25a9dfe6d8417f.png)  




<!-- ![图 10](./../images/1679540175250.png) -->

<!-- ![图 3](../images/c81a7dca512bf6e630a676eaa79a57f01c35abc4423c9af81fda298acfc0857d.png)   -->

<!-- ![图 11](./../images/1679540232245.png) -->


## Kernel

Kernel是一个独立于NoteBook的进程，它运行用户编写的代码并处理NoteBook中的输入和输出。Kernel会将代码执行的结果返回给NoteBook，然后NoteBook会将结果渲染成适当的格式并显示出来，可以理解为是NoteBook和代码之间的中间层。

Kernel可以支持多种编程语言，包括Python、R、Julia等，用户可以根据需要选择不同的Kernel来运行不同的代码（参考<a href="./main.md/#newnb" title="新建NoteBook">新建NoteBook时选择Kernel</a>） 。

### 中断Kernel

中断Kernel是指中断kernel正在运行的代码，针对NoteBook内正在运行的单元格和待运行的单元格。
 
### 重启Kernel

当环境发生变化（如环境安装了新的包或其他情况），需要重启Kernel时使用。

> [!warning|style:flat]
> 重启Kernel的操作将会清除所有已存储的变量值。如果用户在某些变量中保存了非常重要的数据，请在重启Kernel前将重要变量的数据保留下来。



