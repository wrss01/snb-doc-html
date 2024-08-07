# 侧边栏

<!-- 7101752 -->
---
侧边栏为NoteBook提供一系列扩展功能。

## 功能概览

| 图标 | 功能 | 解释 | 
| :----- | :-----| :---- | 
| <img src="../images/b6d1fe4186dfc7a2c2695730a9bdc350c8b806b7aa7c64205cf66bf1bcd2d5a8.png"  style="display: inline-block;padding:0px;border:0px"  />  | 数据资源 | 文件和数据库管理 | 
| <img src="../images/1ab063d310d3e0578f81a902d81951e0ac5934876a4263097c990d2a5001e308.png"  style="display: inline-block;padding:0px;border:0px"  />  | 计算环境 | 查看和管理当前NoteBook的计算资源和调度器 | 
| <img src="../images/3f306e38968ead0be8721c7f61265cbdd797974f47a351b4ea3082b50961c1ad.png"  style="display: inline-block;padding:0px;border:0px"  />  | 导航目录 | NoteBook根据Markdown单元格中使用的标题显示文档结构 | 
| <img src="../images/46ef8d78353da30ffc22347995c6d1772f01646429ff3396233972cf0cff0b8d.png"  style="display: inline-block;padding:0px;border:0px"  />  | 变量预览 | 浏览NoteBook中使用的变量、值和值的一些属性 | 
| <img src="../images/202b15b6e06157b55053916a8e7dd88a5962d6b361da5a43c525aeb342c33615.png"  style="display: inline-block;padding:0px;border:0px"  />  | 版本列表 | 保存NoteBook版本并可还原至历史记录的状态 | 
| <img src="../images/c358ef50700576b2173750a2c94fdff8b84fe1da312eead1f610f24b04a06365.png"  style="display: inline-block;padding:0px;border:0px"  />  | 软件包 | NoteBook的包管理 | 
| <img src="../images/5a98854492fc793f7aeede1e487e8da4a90bc98ef3158ad689f06a87fd318b00.png"  style="display: inline-block;padding:0px;border:0px"  />  | 代码片段库 | 包含`公有库`（NoteBook提供的常用代码片段）和`我的收藏`（用户收藏的代码片段）。 | 
| <img src="/assets/notebook/Xnip2024-07-01_10-31-09.png"  style="display: inline-block;padding:0px;border:0px"  />  | 快捷键 | 快捷键包含notebook编辑模式、命令模式、文档级别（全局Global） | 

## Packages

<span id="pk"></span>

默认情况下，NoteBook的运行环境已经为用户安装了常用的数据分析、机器学习以及可视化的包。

<!-- ![图 11](../images/packages.png)   -->
![图 7](/assets/notebook/Xnip2024-07-01_10-23-58.png)  

### 搜索并查看包版本

![图 12](../images/search.gif)  

### 安装/升级包

* 在`安装`的Tab页搜索要安装的包名称
* 点击放大镜或敲击回车进行搜索
* 在结果列表找到需要安装/升级的包和版本号，点击右侧的下载图标开始安装

![图 14](../images/inspac.png)  

### 删除包

* 在`已安装`的Tab页搜索要删除的包名称
* 在结果列表找到需要删除的包和版本号，点击右侧的删除图标

 ![图 15](../images/delpack.png)  


## 数据资源

<span id="ds"></span>

集成和管理用户的数据资产，显示包括已建立的数据连接（数据库）和已上传的数据文件（csv/excel/txt/json等）。

<!--在SmartNoteBook中，非结构的文件资源存储机制分为两级：

* 通过Workspace文件管理上传后，会将文件传输到MinIO分布式存储的公共区域。该操作详见<a href="../WorkSpace/Files.md" title="上传文件">上传文件</a>

* 通过NoteBook的数据资源同步，可以根据需要将MinIO公共区域的资源文件同步至Node节点使用

![](/assets/身教重于言教.png)-->

### 数据连接

#### 复制连接

已建立的数据库连接将显示在数据资源板块中，可点击`复制数据连接`按钮，将数据连接代码拷贝至单元格使用。（新建数据连接以及当前支持的数据源类型请参考前面的教程<a href="../WorkSpace/DataSource.md" title="数据源">数据源</a>）

![图 21](/assets/notebook/Xnip2024-07-01_10-35-10.png)  

#### 浏览元数据

点击数据库右侧按钮查看库表元数据。

![图 22](/assets/notebook/Xnip2024-07-01_10-40-25.png)  

#### 元数据浏览（如元数据有更新，可点击上方刷新按钮重新获取）

![图 23](/assets/notebook/Xnip2024-07-01_10-42-05.png)  

#### 复制数据源到MindsDB

复制代码至SQL单元格执行，能够快捷无缝的将数据源引入到MindsDB。

MindsDB结合NoteBook的使用教程可以参考<a href="../Tutorial/Mindsdb_demo.md" title="MindsDB(SQL+ML)实战案例">MindsDB(SQL+ML)实战案例</a>

![图 19](/assets/notebook/Xnip2024-07-01_10-43-33.png)  


### WorkSpace文件

- 查看和同步文件

点击右侧小箭头查看已上传至WorkSpace的文件

![图 17](../images/fileup2.png)  

- 批量同步至Node环境：点击`文件一键同步到Node`按钮可将文件批量同步至环境文件

- 单个文件同步至Node环境：如需同步单个文件，则点击该文件右侧的操作按钮，单击`同步到Node`即可

![图 8](../images/1158d489339f8536829f138472f7544b6a8cd170b1748239e9f59ecb1fd8b4d6.png)  

<!-- - 复制文件路径

点击复制按钮拷贝文件路径

![图 19](../images/cppath.png)   -->

- 下载文件

点击文件列表右侧下载按钮可将文件下载至本地

![图 20](../images/downl.png)  


### 环境文件

- 查看文件：点击右侧小箭头查看当前环境下的文件

![图 11](../images/0d6270e207ba9fabd4632ad64fe31d1b2c2bc29ffa9aec0c7e5356c2895a0b78.png)  

- 文件上传：直接上传文件至环境下

- 刷新：刷新文件列表

- 复制路径：点击复制按钮可拷贝文件路径

![图 19](../images/cppath.png)  

- 下载文件：点击文件列表右侧下载按钮可将文件下载至本地

<!-- ![图 20](../images/downl.png)   -->
![图 12](../images/e4705c5fe4f26974bb16460283d94e714d31fd1276722d844b2b649cf5119c43.png)  

- 删除文件：将文件从环境下删除

- 文件预览（可编辑内容并保存）

点击环境文件下的csv数据文件（蓝色），可以像操作Excel表格一样对数据进行预览和编辑（编辑内容后记得点击保存）。

<!-- ![图 13](../images/af7368f26e9d9eaeeaafffb4ccc93c1a77ed57bd67cd5d28a17ae1ab617246fa.png)   -->

<!-- ![图 14](../images/0e3919a6bb58772b6f37009dd1d683e7d4b522c904fe19ea79387c53e669ab15.png)   -->

![图 15](../images/ffd27cc2d857470cdf6920b80f716a3a3353ae3925bfe9d87aac0c4c7caa09f6.png)  

> [!WARNING]
> 目前NoteBook仅支持csv数据文件的预览，且文件大小不超过10M

## 目录
<span id="idx"></span>
目录是一种工具，它根据MarkDown单元格中当前使用的标题显示NoteBook的结构。

MarkDown使用"#"表示不同级别的标题，例如：
- "#  一级标题"
- "##  二级标题"
- "###  三级标题"

NoteBook采集MarkDown的标题层级配合层次缩进自动生成目录

同时，目录是交互式的：单击标题可导航到NoteBook中的相应部分

![图 24](../images/indexall.png)  

## 环境

<span id="env"></span>

### 查看配置/负载情况

![图 25](../images/workload.png)  

### 切换环境

当用户购买和构建了多个环境资源，可根据需要切换NoteBook的运行环境

![图 26](../images/switchenv.gif)  

### 当前环境信息

<!-- ![图 22](../images/68590f66bff70edda1a8e60c727fa27c8aead0132f7b87851e28616982c35975.png)   -->

在NoteBook的底部状态栏中，您可以看到当前环境的基本配置以及实时的使用状态。

![图 23](../images/4470611f7bf05ef813c991e24f3e13ef6b3d044f7d516c5fbb3077b8b4a1d520.png)  


> [!NOTE|style:flat]
> 环境名称旁边的小圆点通过颜色来直观表示环境的运行状况：蓝色表示环境状态正常，而红色则表示出现异常。

### 创建调度器

创建调度器的方法详见<a href="../WorkSpace/Schedule.md" title="Workspace调度器">WorkSpace调度器</a>

## 变量浏览
<span id="vr"></span>
浏览NoteBook中使用的变量、值和值的一些属性。

单元格的代码执行后，变量将出现在左侧的`变量浏览`列表中，其中包含有关其类型和内容的信息，如变量名、变量的值、变量类型、占用大小等。

![图 27](../images/varie.png)  


### 变量预览和编辑

点击变量列表中的DataFrame数据变量（蓝色），可以像操作Excel表格一样对变量进行预览和编辑（编辑内容后记得点击保存）。

> [!WARNING]
> 该手动编辑变量的操作不会被SNB记录，因此重新执行NoteBook该手动操作无法重现。

![图 16](../images/16248ee7fc528174b5bc8e3ca9d3e58fc0f3c5e16e5bfa314b3fb390f971df4d.png)  

![图 17](../images/4822bc6f155b5f1080267be40bce739141cb1b459bcb0a57ee7016cb0068a3cd.png)  

> [!warning|style:flat]
> 重启Kernel的操作将会清除所有已存储的变量值。如果用户在某些变量中保存了非常重要的数据，请在重启Kernel前将重要变量的数据保留下来。

## 版本列表

<!-- 用户可以通过保存版本，记录各阶段的工作成果。并可拿历史版本与当前内容进行比对，NoteBook会自动标注两个版本间的文件差异。用户可根据需要替换成某历史版本。

- 版本名称
- 版本提交人
- 版本提交时间
- 回退到该版本

![图 13](../images/new%20banbnexinxi%20.png)   -->

### 保存版本

<span id="sv"></span>

NoteBook文档在我们编写期间会每隔30秒保存一次内容，但如果需要永久保存NoteBook某一个时点的内容和状态，用户需要自行保存成版本。初始状态下版本列表是空的：

![图 28](../images/verso.png)  

按下`Ctrl + S`，输入`版本名称`和`版本信息`后点击确定按钮，提示版本保存成功。

![](/assets/bubbxx.png)

如用户在WorkSpace设置里配置了代码仓库GitLab或GitHub，保存版本可选择推送至代码仓库。

![图 18](../images/bd7a1644f4ea3337683a918c1f6b77487c74b87a225f7a85cad8b4973b76e300.png)  

版本列表会增加`已推送至代码仓库`标识：

![图 20](../images/ea66bfc65d7a8dc4aad7cfeba997569d4e7eafa7b396ba7ade482e4285543423.png)  

保存新版本时查看最近保存版本的信息：

![图 21](../images/60b5114987b8e19334b1727b2833099f6131806bceeee7dca4fd76f9f6b5b55a.png)  



### 版本对比

单击列表中某个版本，可打开该历史版本与当前NoteBook内容进行对比。

下图左侧为历史版本内容，右侧为当前NoteBook文档的内容

![](/assets/bbdb.png)

### 回退版本

点击版本列表右侧的回退按钮，可以将当前NoteBook文档内容恢复至历史版本

![图 30](../images/rollbakkk.png)  


## 代码片段

<span id="cd"></span>

### 公有库

SmartNoteBook帮用户内置了一些常用的代码片段，用户根据需要复制使用

鼠标移动到代码片段右侧会显示预览框，点击代码名称右侧的复制按钮可复制整块代码

![图 32](../images/cpdercoppp.png)  


### 我的收藏

个人收藏的代码片段，用户根据需要复制使用

同样的，鼠标移动到代码片段右侧会显示预览框

代码名称右侧两个按钮分别为`删除`代码块和`复制`整块代码

![图 33](../images/collcode.png)  

收藏代码的操作详见<a href="./Collections.md" title="代码收藏">代码收藏</a>








