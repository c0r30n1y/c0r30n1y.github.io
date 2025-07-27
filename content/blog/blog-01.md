---
title: "blog-01"
date: 2023-07-21T15:00:00+08:00
author: "guts"
tags: ["Hugo", "Markdown", "Tutorial"]
categories: ["Introduction"]
draft: false
---

# Intro
超文本标记语言（英语：HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。

{{< highlight html >}}
<!DOCTYPE html> <!-- 声明为 html5 文档，止浏览器的怪异模式，强制浏览器按照标准模式渲染网页！ -->
<html> <!-- html 页面根 -->
  <head> <!-- 元（meta）数据 -->
    <meta charset="utf-8"> <!-- 定义网页编码格式为 utf-8，防止中文乱码 -->
    <title>The Outliers</title> <!-- 标题 -->
  </head>

  <body> <!-- 可见页面内容 -->
    <h1>This is a title.</h1> <!-- 大标题 -->
    <p>This is a paragraph.</p> <!-- 段落 -->
  </body>
</html>
{{< /highlight >}}

> [!tip]+ 设置 utf-8 后依然乱码？
> 请检查文本编辑器的编码格式是否与meta设置的一致。

# Elements
## Basic
{{< highlight html >}}
    <!-- Headings -->
    <h1>This is heading 1</h1>
    <h2>This is heading 2</h2>
    <h3>This is heading 3</h3>
    <h4>This is heading 4</h4>
    <h5>This is heading 5</h5>
    <h6>This is heading 6</h6>

    <!-- paragraph -->
    <p>This is a paragraph.</p>
    <p>This is another paragraph.</p>

	<!-- Horizontal  -->
	<hr>

	<!-- preformatted text  -->
	<pre>
	  My Bonnie lies over the ocean.

	  My Bonnie lies over the sea.

	  My Bonnie lies over the ocean.

	  Oh, bring back my Bonnie to me.
	</pre>

	<!-- Line Breaks -->
	<p>This is a <br> paragraph with a line break.</p>
{{< /highlight >}}

## Attributes
### Global
- `id`：为元素指定唯一的标识符。
	- `<div id="header">This is the header</div>`
- `class`：为元素指定一个或多个类名，用于 CSS 和 JS 选择。
	- `<p class="text highlight">This is a highlighted text.</p>`
- `style` ：直接在元素上使用 css 样式。 
	- `<p style="color: blue; font-size: 14px;">This is a styled paragraph.</p>`
- `title` ：额外信息，鼠标悬停时显示。
	- `<abbr title="HyperText Markup Language">HTML</abbr>`
- `data`：存储自定义数据，用于 JavaScript 访问。
	- `<div data-user-id="12345">User Info</div>`

### Specifies 
- `herf`：用于`<a>` 和`<link>`，指定链接的目标 URL。
	- `<a href="https://www.example.com">Visit Example</a>`
- `src`：用于 `<img>`、`<script>`、`<iframe>`等元素，指定外部资源的 URL。
	- `<img src = "image.jpg">`
- `alt`：用于 `<img>`，替代文本，图像无法显示时显示
	- `<img src="image.jpg" alt="An example image">`
- `type`：用于 `<input>`、`<button>`，指定控件的类型
	- `<input type="text" placeholder="Enter your name">`
- `value`：用于`<input>`、`<button>`、`<option>`等元素，指定元素的初始值
	- `<input type="text" value="Default Value">`
- `disabled`（用于表单元素）：禁用元素，使其不可交互。
	- `<input type="text" disabled>`
- `checked`（用于 `<input type="checkbox">` 和 `<input type="radio">`）：指定复选框或单选按钮是否被选中。
	- `<input type="checkbox" checked>`
- `placeholder`（用于 `<input>` 和 `<textarea>` 元素）：在输入框中显示提示文本。
	- `<input type="text" placeholder="Enter your email">`
- `target`（用于 `<a>` 和 `<form>` 元素）：指定链接或表单提交的目标窗口或框架。
	- `<a href="https://www.example.com" target="_blank">Open in new tab</a>`

### Bool
- `disabled`:禁用
	- `<input type="text" disabled>`
- `readonly`：使输入框只读。
	- `<input type="text" readonly>`
- `required`：指定输入字段为必填项。
	- `<input type="text" required>`
- `autoplay`（用于 `<audio>` 和 `<video>` 元素）：自动播放媒体。
	- `<video src="video.mp4" autoplay></video>`

### Custome
HTML5 引入了 `data-*` 属性，允许开发者自定义属性来存储额外的数据。
`<div data-user-id="12345" data-role="admin">User Info</div>`

### Event
- `onclick`：当用户点击元素时触发。
	- `<button onclick="alert('Button clicked!')">Click Me</button>`
- `onmouseover`：当用户将鼠标悬停在元素上时触发。
	- `<div onmouseover="this.style.backgroundColor='yellow'">Hover over me</div>`
- `onchange`：当元素的值发生变化时触发。
	- `<input type="text" onchange="alert('Value changed!')">`

## Style
- Background Color
	- `<body style="background-color:powderblue;">`
- Text Color
	- `<h1 style="color:blue;">This is a heading</h1>`
- Fonts
	- `<h1 style="font-family:verdana;">This is a heading</h1>`
- Text Size
	- `<h1 style="font-size:300%;">This is a heading</h1>`
- Text Alignment
	- `<h1 style="text-align:center;">Centered Heading</h1>`

## Formatting
- `<b>` - Bold text
- `<strong>` - Important text
- `<i>` - Italic text
- `<em>` - Emphasized text
- `<mark>` - Marked text
- `<small>` - Smaller text
- `<del>` - Deleted text
- `<ins>` - Inserted text
- `<sub>` - Subscript text
- `<sup>` - Superscript text

```html
<b>This text is bold</b>
<strong>This text is important!</strong>
<i>This text is italic</i>
<em>This text is emphasized</em>
<small>This is some smaller text.</small>
<p>Do not forget to buy <mark>milk</mark> today.</p>
<p>My favorite color is <del>blue</del> red.</p>
<p>My favorite color is <del>blue</del> <ins>red</ins>.</p>
<p>This is <sub>subscripted</sub> text.</p>
<p>This is <sup>superscripted</sup> text.</p>
```

## Quotation and Citation Elements
- `<blockquote>`：引用
- `<q>`：短引用
- `<abbr>`：缩写
- `<address>`：联系方式
- `<cite>`：作品标题
- `<bdo> `：反转文本方向

## Links
- `href`：链接目标
	- `<a href="https://www.example.com">访问 Example</a>`
- `target`：定义链接的打开方式。
	- `_blank`: 在新窗口或新标签页中打开链接
	- `_self`: 在当前窗口或标签页中打开链接（默认）。
	- `_parent`: 在父框架中打开链接。
	- `_top`: 在整个窗口中打开链接，取消任何框架。
	- `<a href="https://www.example.com" target="_blank" rel="noopener">新窗口打开 Example</a>`
- `rel`：定义链接与目标页面的关系。
	- `nofollow`：搜索引擎不应跟踪该链接，用于外部链接
	- `noopener`、`noreferrer`：  防止在新标签中打开链接时的安全问题，尤其是使用 `target="_blank"` 时
	- `<a href="https://www.example.com" target="_blank" rel="noopener noreferrer">安全链接</a>`
- `download`：提示浏览器下载链接目标而不是导航到该目标。
	- `<a href="file.pdf" download="example.pdf">下载文件</a>`
- `title`：定义链接的额外信息，当鼠标悬停在链接上时显示的工具提示。
	- `<a href="https://www.example.com" title="访问 Example 网站">访问 Example</a>`
- `id`：用于链接锚点，通常在同一页面中跳转到某个特定位置。
	- `<a href="#section1">跳转到第1部分</a>`
	- `<div id="section1">这是第1部分</div>`
- `hreflang`: 指定链接的目标URL的语言
	- `<a href="https://www.example.com/es" hreflang="es">访问西班牙语网站</a>`
- `type`: 指定链接资源的MIME类型
	- `<a href="style.css" type="text/css">样式表</a>`
- `class`: 用于指定元素的类名（CSS中定义）
	- `<a href="https://www.example.com" class="external-link">外部链接</a>`
- `style`: 直接在元素上定义CSS样式
	- `<a href="https://www.example.com" style="color: red;">红色链接</a>`

## Head
- `title`：标题
- `base`：该标签作为HTML文档中所有的链接标签的默认链接
	- `<base href="http://www.runoob.com/images/" target="_blank">`
- `link`：文档与外部资源之间的关系。
	- 通常用于链接样式表
	- `<link rel="stylesheet" type="text/css" href="mystyle.css">`
- `style`：定义了HTML文档的样式文件引用地址.
	- 可以直接在内部添加样式
- `meta`：META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。
	- 为搜索引擎定义关键词: `<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">`
	- 为网页定义描述内容: `<meta name="description" content="免费 Web & 编程 教程">`
	- 定义网页作者: `<meta name="author" content="Runoob">`
	- 每30秒钟刷新当前页面: `<meta http-equiv="refresh" content="30">`
- `script`：用于加载脚本文件

## CSS
### 内部样式表
当单个文件需要特别样式时，就可以使用内部样式表。
```html
<head>
<style type="text/css">
body {background-color:yellow;}
p {color:blue;}
</style>
</head>
```

### 外部样式表
样式需要被应用到很多页面的时候，外部样式表将是理想的选择。
```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

更多信息：[HTML 中引入 CSS 的方式](https://www.runoob.com/w3cnote/html-import-css-method.html)

## Tables
![[Pasted image 20250712165436.png]]

`<table>`	定义表格
`<th>`	定义表格的表头
`<tr>`	定义表格的行
`<td>`	定义表格单元
`<caption>`	定义表格标题
`<colgroup>`	定义表格列的组
`<col>`	定义用于表格列的属性
`<thead>`	定义表格的页眉
`<tbody>`	定义表格的主体
`<tfoot>`	定义表格的页脚

## Lists
### Unordered HTML List
```html
<ul style="list-style-type:disc;"> <!-- circle,disc,square -->
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

### Ordered Lists
```html
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

- type="1"	 数字
- type="A"	大写字母
- type="a"	小写字母
- type="I"	大写罗马数字
- type="i"	小写罗马数字

### Description Lists
```html
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```

## Block and Inline
- Block
大多数 HTML 元素被定义为块级元素或内联元素。块级元素在浏览器显示时，通常会以新行来开始（和结束）。

- Inline
内联元素在显示时通常不会以新行开始。

- `<div>`
HTML `<div>` 元素是块级元素，它可用于组合其他 HTML 元素的容器。`<div>` 元素没有特定的含义。

- `<span>`
HTML `<span>` 元素是内联元素，可用作文本的容器。`<span>` 元素也没有特定的含义。当与 CSS 一同使用时，`<span>` 元素可用于为部分文本设置样式属性。

# Semantic HTML
## Header
```html
<!-- Non-semantic header -->
<div class="header">
  <h1>My Site</h1>
  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </nav>
</div>

<!-- Semantic header -->
<header>
  <h1>My Site</h1>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>
```

## Nav
```html
<!-- Non-semantic navigation -->
<div class="navigation">
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Contact</a>
</div>

<!-- Semantic navigation -->
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

## Main
```html
<!-- Non-semantic main content -->
<div class="main-content">
  <h2>About Us</h2>
  <p>Welcome to our website. We are a company that specializes in widgets.</p>
</div>

<!-- Semantic main content -->
<main>
  <h2>About Us</h2>
  <p>Welcome to our website. We are a company that specializes in widgets.</p>
</main>
```

## Article
```html
<!-- Non-semantic article -->
<div class="article">
  <h2>How to Make a Widget</h2>
  <p>Widgets are great. Here's how to make one.</p>
</div>

<!-- Semantic article -->
<article>
  <h2>How to Make a Widget</h2>
  <p>Widgets are great. Here's how to make one.</p>
</article>
```

## Aside
```html
<div>
  <article>
    <h2>Article Title</h2>
    <p>Article content goes here</p>
  </article>
  <aside>
    <h3>Related Articles</h3>
    <ul>
      <li><a href="#">Article 1</a></li>
      <li><a href="#">Article 2</a></li>
      <li><a href="#">Article 3</a></li>
    </ul>
  </aside>
</div>
```

## Section
```html
<section>
  <h2>Section Title</h2>
  <p>Section content goes here</p>
</section>
```

## Footer
```html
<!-- Non-semantic footer -->
<div class="footer">
  <p>&copy; 2021 My Site</p>
</div>

<!-- Semantic footer -->
<footer>
  <p>&copy; 2021 My Site</p>
</footer>
```

## Details and Summary
```html
<details>
  <summary>Click to expand</summary>
  <p>Content goes here</p>
</details>
```

## Figure and Figcaption
```html
<figure>
  <img src="image.jpg" alt="Image description" />
  <figcaption>Image caption</figcaption>
</figure>
```

## Mark
```html
<p>Here is some <mark>highlighted</mark> text.</p>
```

## Time
```html
<p>The event will take place on <time datetime="2021-01-01">January 1st, 2021</time>.</p>
```

## Progress
```html
<progress value="50" max="100"></progress>
```


