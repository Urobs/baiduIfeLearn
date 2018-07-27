# HTML ElEMENTS

[参考资料W3C](https://www.w3.org/TR/2017/REC-html52-20171214/index.html#contents)

## Document element

### <html>

html元素作为文档的文档元素（document element），代表了HTML文档的根

html里面元素的内容元素包括<body>和<head>

包括全局元素和manifest，其中鼓励使用lang属性指定语言

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Swapping Songs</title>
  </head>
  <body>
    <h1>Swapping Songs</h1>
    <p>Tonight I swapped some of the songs I wrote with some friends, who
    gave me some of the songs they wrote. I love sharing my music.</p>
  </body>
</html>
```

## Document metadata

### <head>

作为html元素的第一个子元素，代表这个文档的元数据集合

> Metadata content is content that sets up the presentation or behavior of the rest of the content, or that sets up the relationship of the document with other documents, or that conveys other "out of band" information.  // 元数据是指表示文档剩下内容的含义或者行为表现，或者设置此文档与其他文档的关系，或者其他带外管理的信息，即为表示数据的数据

### <title>

head里面的元数据，只能包含一个title元素，表示文档的名字或者主题

### <base>

元数据，唯一，设置此文档的主URL

`<base href="https://www.example.com/news/index.html">`

###  <link>

元数据，指定html文档连接其他资源文件如css

属性rel，必须，指定链接的类型

href，指定链接的文件地址

type，指定文件的MIME类型

### <meta>

元数据，用来表示不能被其他元数据标签如<base>等表示的多种元数据

属性name，表示描述的数据的类型

属性content，指定元数据的内容

特别的，`<meta http-equiv="X-UA-Compatible" content="IE=edge"> `表示告诉IE8以何种方式去渲染网页

### <style>

通常用来设置css

## Sections

### <body>

代表文档的内容

body元素是段落的根目录

### <article>

代表一份完整的内容，可以是报纸杂志上面的文章短文等

一般在内容加入<h1-h6>元素以明确

### <section>

代表文档或应用的一段内容或者一个章节，一块相对独立的部分

一般在内容加入<h1-h6>元素已明确

### <nav>

代表页面中包含导航到其他页面的链接部分的内容

### <aside>

代表段落中与段落内容区分开的不同但是有关联的内容

### <h1-h6>

标题

### <header>

一般包含段落简介和导航说明的内容

### <footer>

一般包含者段落文章相关的信息说明，比如作者，版权说明，编写时间，相关链接等等

## Grouping content

### <p>

代表一个段落

### <address>

个人组织或者单位的联系信息，包括社交媒体，住址电话等等

### <hr>

代表段落级的变化，如主题转变，过渡段，场景转变

```html
<section>
  <h1>Communication</h1>
  <p>There are various methods of communication. This section
  covers a few of the important ones used by the project.</p>
  <hr>
  <p>Communication stones seem to come in pairs and have mysterious
  properties:</p>
  <ul>
    <li>They can transfer thoughts in two directions once activated
    if used alone.</li>
    <li>If used with another device, they can transfer one’s
    consciousness to another body.</li>
    <li>If both stones are used with another device, the
    consciousnesses switch bodies.</li>
  </ul>
  <hr>
  <p>Radios use the electromagnetic spectrum in the meter range and
  longer.</p>
  <hr>
  <p>Signal flares use the electromagnetic spectrum in the
  nanometer range.</p>
</section>
```



### <pre>

代表一块需要展示的内容

### <blockquote>

代表引用的内容块

### <ol>

代表一块有序列表内容

### <ul>

代表一块无序列表内容

### <li>

<ol> 或<ul>元素的子节点

### <dl>

表示一组术语描述组

### <dt>

表示一项术语

### <dd>

表示一项术语的描述

### <figure>

表示一些流内容(flow content),一般表示主流内容里面的一个独立的单元

### <figcaption>

表示<figure>里面内容的标题

### <main>

表示<body>里面的主体内容

### <div>

没有任何具体的语义，它表示他的子节点，可以用class lang title 等属性去标记常见的语意

## Text-level sematics

### <a>

有href属性，表示被其内容标记的超链接

无href属性，表示占位符，或者仅表示元素的内容

### <em>

表示强调重点内容

### <strong>

表示重要，严肃或者很急的内容

### <small>

表示附带的注释

### <s>

表示不再准确或者不在相关的内容，如过期的价格

### <cite>

表示内容的参考，必须包括内容的标题或者作者或者url的引用链接

### <q>

表示作者引用的修辞，属性cite指定一个链接以查看引用内容的位置

### <dfn>

表示术语的缩写的描述示例，通常与<abbr>一起使用

### <abbr>

常作为<dfn>的子元素,title属性描述术语的全称

### <ruby>

来展示东亚文字注音或字符注释 

### <rb>

### <rt>

### <rtc>

### <rp>

#### <data>

### <time>

### <code>

代表一段代码

### <var>

代表一个变量

### <samp>

代表程序和计算机输出的一段例子或者引用

### <kbd>

代表用户输入，通常是键盘，也可能代表其他如

### <sub> <sup>

<sub>是子脚本，而<sup>是超脚本，超脚本就是这段脚本约定的变量

### <i>

表示引用的术语，专有名词，不同语境的词汇等等

### <b>

代表一系列不带有重要性暗示含义的文本如文章的关键词等等

### <u>

注释

### <mark>

表示标记

### <bdi>

 Text directionality isolation 

### <bdo>

 Text directionality formatting 

### <span>

类似<div>,没有语义上的标记含义，通常设置属性以语义化

### <br>

换行

### <wbr>

表示换行机会，我的理解是语义化的占位符

## Edit

### <ins>

常包含在<aside>内，表示文档的添加说明	

### <del>

表示文档中删除的部分

## Embedded content（嵌入式内容）

### <picture>

通常作为<img>的母元素，设置属性为其子元素提供源数据或者说明

### <source>

代表资源的容器

### <img>

嵌入的图像，可设置多个属性

### <iframe>

代表一个嵌套的浏览器上下文，可以是指向本页面也可以是其他页面

### <embed>

为外部应用或者交互式内容提供集成点，比如flash

#### <object>

表示一个外部的嵌入式对像，可以是图片也可以是插件，或者浏览器页面的一部分上下文

### <param>

无任何特殊含义，常用于<object>的内子元素

### <video>

用于视频或者带字幕的音频

### <audio>

声音或者音频

### <track>

用于为媒体元素指定明确的外部文本

### <map>

通常作为<area>或者<img>的母元素，定义一块地图

### <area>

代表地图上相应的区域及其超链接，或者地图上面的死区

## Links

Links代表两种资源之间的连接，其中一种是当前的文档

有两种类型的links：

1. 指向外部资源的链接，通常用于扩展本文档的内容
2. 超链接，导航向的外部资源

### <a> <area>

### <link>

## Tabular data

### <table>

代表多个维度的数据集合

### <caption>

表示表格的标题

### <colgroup>

代表表格的列的组合

### <col>

代表表格的一列，no end tag

### <tbody>

表示一块数据

### <thead>

一块数据的标题,通常忽略end tag

### <tfoot>

一块数据的注脚,通常忽略end tag

### <tr>

表示一行数据单元格,通常忽略end tag

### <td>

表示一个数据单元格,通常忽略end tag

### <th>

表示一个数据单元格的标题，可以理解为加粗的<td>,通常忽略end tag

```html
<table>
  <thead>
  <tr>
    <th>
    <th>2008
    <th>2007
    <th>2006
  <tbody>
  <tr>
    <th>Net sales
    <td>$ 32,479
    <td>$ 24,006
    <td>$ 19,315
  <tr>
    <th>Cost of sales
    <td>  21,334
    <td>  15,852
    <td>  13,717
  <tbody>
  <tr>
    <th>Gross margin
    <td>$ 11,145
    <td>$  8,154
    <td>$  5,598
  <tfoot>
  <tr>
    <th>Gross margin percentage
    <td>34.3%
    <td>34.0%
    <td>29.0%
</table>
```



## Forms

### <form>

表示一组可以编辑并且提交给服务器的数据集

### <label>

表示用户接口的标题

### <input> 



### <button>

### <select>

代表在一组选项中进行选择的控件

### <datalist>

作为<option>的母元素，一组数据选项

### <optgruop>

一组<option>

### <option>

选项

### <textarea>

As a child of a `select` element.

As a child of a `datalist` element.

As a child of an `optgroup` element.

### <output>

代表一组数据的结果

### <progress>

代表完成任务的的进度

### <meter>

代表一组标量的测量

### <fieldset>

代表一组相同主题的表单控件

### <legend>

一组表单控件的的标题

## Interactive elements

### <details>

表示公开小部件，用户可以从该小部件获得附加信息或控件 

### <summary>

作为<detail>的子元素，表示说明，概览

### <dialog>

表示一组交互的对话容器

## Scripting

### <script>

src指定外联的js文件，或者直接嵌入，也可以指定type类型

### <noscript>

表示容器，如果浏览器禁用脚本就会启用，如果脚本正常执行那么什么都不会显示

### <template>

在dom中并不会表示任何节点，也就是浏览器渲染时这个元素可忽略

用于声明可以通过脚本克隆并插入到文档中的HTML片段 

### <canvas>

画布，用于渲染游戏图像，图像

## 关于DOCTYPE

> DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications. 

简而言之就是忽略DOCTYPE的话会导致浏览器尝试使用不同的渲染模式，而这种渲染模式可能会导致与某些规范冲突，声明DOCTYPE保证浏览器尽最大可能遵循相关规范

## 关于web语义化

我的理解是人可以通过文章的内容和段落的结构，也就是上下文去判断一段内容的具体语义，而机器只能读取文本，也就是它并不能分辨哪一块内容代表的主题内容，web语义化就能够使文档在程序员编写的时候人为地去设置具体的语义结构，这样通过机器程序就能通过标签的语义去读取相关的内容，进而更好地进行相关的处理