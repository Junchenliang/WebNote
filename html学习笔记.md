# Html笔记

## 一、基本概念

### 1. 什么事html?

> **Hyper Text Markup Language**
>
> 超文本标记语言
>
> 超文本指定是：流媒体、声音、视频、图片等
>
> 这种语言都由一个个标签构成。开始标签、结束标签。

### 2. html在哪里运行?

> 在浏览器上

### 3. html在哪里写？

> 记事本打开就可以写，不需要编译。



### 4. html的作用？

> 起初，网络速度很慢，为了节省时间，把用户的输入放在本地来判断，判断输入是否合规，是否正确。
>
> 后来，拓展了功能，用于美化装饰服务器返回的信息。





***



## 二、基本知识





### 1. 基本构架



```html
<!DOCTYPE html>
<html>
  <head>
    	<meta charset="utf-8">
      <title>标签的内容</title>
  </head>
  
  <body>
    	存放内容的地方
  </body>
</html>
```



### 2. 基本标签

##### 2.1 段落标签

> 1. 把文字分段 `<p>`....</p>
> 2. 分标题等级
>    1. \<h1>一级标题</h1>
>    2. \<h2>二级标题</h2>
> 3. 换行符 `<br>`
> 4. 水平线 `<hr>`
> 5. 保留格式，再HTML上是什么样子的，现实的时候就是怎样的`<pre>.......</pre>`



##### 2.2 文字修饰

> 1. 粗体：`<b>...</b>`
> 2. 斜体：`<i>...</i>`
> 3. 插入字：`<ins>...</ins>`
> 4. 删除字：`<del>...</del>`
> 5. 右上角字：`10<sup>2</sup>` 表示10的平方
> 6. 右下角字：`m<sub>2</sub>` 表示平方米
> 7. 字体：`<font,color="red" size="12"> hello world </font>`



##### 2.3 实体符号

> 1. 空格：`&nbsp;`
> 2. 大于号：`&gt;`
> 3. 小于号：`&lt;`



##### 2.4 表格

基本框架

```html
<tabel border='1px' width="300px" height="200px">
	<thead>
  	<tr>
    	<th>存货名称</th>
      <th>数量</th>
      <th>金额</th>
    </tr>
  </thead>
  
  <tbody>
  	<tr>
      <td>611077A</td>
      <td>61</td>
      <td>200</td>
    </tr>
  </tbody>
  
  <tfont>
    <tr>
      <td>合计</td>
      <td>61</td>
      <td>200</td>
    </tr>
  </tfont>
</tabel>

```

> **说明：**
>
> 一个表格以`<table>`开始，以`</table>`结束。
>
> 标题行以`<thead>`开始，以`</thead>`结束。
>
> 内容以`<tbody>`开始，以`</tbody>`结束。
>
> 结尾行以`<tfont>`开始，以`</tfont>`结束。
>
> 每一行都以`<tr>`开始，以`</tr>`结束
>
> 每一行里的每个元素以`<td>`或者`<th>`开始，以对应的标签结束，td是普通元素，th是标题行用的元素，加了居中对齐、粗体等效果。
>
> **合并单元格：**
>
> rowspan="2" 表示从当前行向下合并1行
>
> colspan="2" 表示从当前行向右合并一列



##### 2.5 给网页加背景颜色、背景图片

<body bgcolor="red"> 设定网页的颜色

<body background="file path"> 设置网页的背景图片



##### 2.6 插入图片

`<img src="path" width="200px" title="xxx" alt="图片找不到！">`

* src 指定图片的路径
* width 设置了宽度，高度会自动缩放，不需要设置。
* title 设置鼠标悬停时的提示信息
* alt 当图片找不到时设置



##### 2.7插入超链接

`<a href="path" target="_blank">超链接显示的名字</a>`

* href 路径可以使网络中的路径，也可以是本地路径。

* target（指定链接的地址从哪个窗口打开）

  * _blank 链接在新的窗口打开
  * _self 链接从当前窗口打开
  * _parent 链接从父窗口打开
  * _top 链接从当前当前窗口的顶级窗口打开

  

##### 

##### 2.8 列表



<u>无序列表</u>

<ul>
  <li>石家庄</li>
  	<ul>
      <li>销售部</li>
      <li>财务部</li>
      <li>仓储部</li>
  	</ul>
  <li>天津</li>
  <li>保定</li>
</ul>



<u>有序列表</u>

<ol>
  <li>石家庄</li>
  	<ol>
      <li>销售部</li>
      <li>财务部</li>
      <li>仓储部</li>
  	</ol>
  <li>天津</li>
  <li>保定</li>
</ol>

> 在ul 或者 ol 里面加个type属性可以改变列表的样式



##### 2.9 表单

`<form action="path">..... </form>`在form里面写入内容,在里面有一个`<input type="submi" value="提交"/>`

就会把写的内容以键值对的方式传给action里面的网址。



*表单里包含的其他控件:*

**重点** <u>控件里的属性必须有name，name的值作为key,控件获得的值为value，然后把key=value提交给网址</u>

如：`https://www.google.com/search?q=python&oq=python&
aqs=chrome.0.69i59j35i39j0i512j69i60j69i61j69i65l2j69i60.3778j0j7&sourceid=chrome&ie=UTF-8`



> 1. `<input type="text" name="username"/>`<u>（文本框）</u>
>
>    1. 文本框 read_only;disabled 属性都可以使控件不能动，但是read_only可以上传值，而disabled不能上传值
>    2. text 控件中加入属性maxlength="3" ，表示只允许输入3个字符。
>
> 2. `<input type="password" name="userpwd"/>` <u>（密码框）</u>
>
> 3. `<input type="radio" name="sex" value="1" />男
>     <input type="radio" name="sex" value="0" checked />女`<u>（单选框）</u>
>
>    1. checked 默认选中
>
> 4. `<input type="checkbox" name="aihao" value="eat">吃
>      <input type="checkbox" name="aihao" value="drink">喝
>     <input type="checkbox" name="aihao" value="piap">嫖`<u>（多选框）</u>
>
> 5. `<select name="grade" size="2" multiple >
>    							<option value="gz">高中</option>
>    							<option value="zk"selected>专科</option>
>    							<option value="bk">本科</option>
>    							<option vlaue="ss">硕士</option>
>    						</select>`<u>（下拉列表）</u>
>
>    1. size 表示可显示两个
>    2. multiple 表示 可以连续
>    3. selected 表示默认选中
>
> 6. `<textarea row="10" cols="18" name="mesg"></textarea>`<u>（多行多列文本框）</u>
>
>    1. Row 指定多少行
>    2. Cols 指定多少列
>
> 7. `<input type='file' />`<u>（文件选择框）</u>
>
> 8. <input type='hidden' name="ie" value="UTF-8"/> <u>（隐藏项目）</u>
>
>    1. 有些属性不需要用户输入，是默认值，可以隐藏起来，提交的时候一起提交上去。
>
> 9. `<input type="reset" value="清空" /><u>（重置、清除数据按钮）</u>
>
> 10. div 和 span 都是图层
>
>     1. Div 一行
>     2. Span 一个
>
>     
>
>     
>
> 11. 

























