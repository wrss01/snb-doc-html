# 下拉框输入

---

根据用户从枚举数字或字符串列表中选择的单个值来参数化您的分析。

---

## 静态
  静态值是手动输入的。<br />
  - 数组的集合
  - label是下拉框显示的名称
  - value是下拉框python变量引用的值

   ```
    [{"label":"业务类型a","value":"a"},{"label":"业务类型b","value":"b"},{"label":"业务类型c","value":"c"}]
   ```

![图 3](../../assets/dashboard/WX20240617-181412.png)

## 动态
  动态值允许您将下拉列表的可用选项从代码本身链接到数据框列、列表、numpy 数组或 Pandas 系列。

![图 4](../../assets/dashboard/1718620041029.jpg)


## 多选下拉框
  如果开启多选选项则python变量输出变成以逗号分隔的（,）str

![图 4](../../assets/dashboard/WX20240617-184342.png)

```
  提示
  下拉菜单将仅显示前 10,000 个结果，所有后续选项将被截断。
```