# 模型视图

---

模型视图显示了SmartNoteBook项目中Notebook中单元格之间的关系。

> [!warning|style:flat]
> 您可以将模型视图视为逻辑的视觉镜像。您对 Notebook 视图中的单元格所做的任何更改都将反映在 Graph 视图中。


您选择模型视图中特定的节点，我们会在模型视图中突出显示上游祖先节点和下游后代节点，并在NoteBook视图中自动滚动到该单元格。这对于特别长或复杂的项目非常有用，因为在这些项目中很难看到单元格之间的依赖关系。

为了优化图形视图的可读性，可以使用不同的方法来组织图形视图中的元素。您可以通过将单元格拖放到图形视图中的任意位置来重新排列它们。还有鼠标操作，您可以使用它们来放大、缩小或缩放以适应宽度。可以通过拖动图形视图和逻辑之间的边框来调整此宽度。

您可以调整小地图是否显示。

---

## 示例
变量引用被自动推断为链接（或“边”），并以可视化布局显示，如下例所示：
<video tabindex="0" controls class="video-stream html5-main-video" webkit-playsinline="" playsinline="" controlslist="nodownload" style="width: 1200px; height: 640px; left: 0px; top: 0px;">
  <source src="../assets/dashboard/202406251645.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> 

