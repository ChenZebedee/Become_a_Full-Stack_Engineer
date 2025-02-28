# HTML 基础学习

<!-- toc -->

- [TODO LIST](#todo-list)
- [环境配置](#%E7%8E%AF%E5%A2%83%E9%85%8D%E7%BD%AE)
- [HTML 基础](#html-%E5%9F%BA%E7%A1%80)
- [HTML 元素](#html-%E5%85%83%E7%B4%A0)
  * [语法](#%E8%AF%AD%E6%B3%95)
  * [HTML 元素嵌套](#html-%E5%85%83%E7%B4%A0%E5%B5%8C%E5%A5%97)
  * [空元素](#%E7%A9%BA%E5%85%83%E7%B4%A0)
  * [HTML 提示：使用小写标签](#html-%E6%8F%90%E7%A4%BA%E4%BD%BF%E7%94%A8%E5%B0%8F%E5%86%99%E6%A0%87%E7%AD%BE)
- [HTML 属性](#html-%E5%B1%9E%E6%80%A7)
  * [HTML 属性参考手册](#html-%E5%B1%9E%E6%80%A7%E5%8F%82%E8%80%83%E6%89%8B%E5%86%8C)
- [HTML 标题](#html-%E6%A0%87%E9%A2%98)
  * [标题很重要](#%E6%A0%87%E9%A2%98%E5%BE%88%E9%87%8D%E8%A6%81)
- [HTML 段落](#html-%E6%AE%B5%E8%90%BD)
- [HTML 文本格式化](#html-%E6%96%87%E6%9C%AC%E6%A0%BC%E5%BC%8F%E5%8C%96)
  * [HTML 文本格式化标签](#html-%E6%96%87%E6%9C%AC%E6%A0%BC%E5%BC%8F%E5%8C%96%E6%A0%87%E7%AD%BE)
  * [HTML "计算机输出" 标签](#html-%E8%AE%A1%E7%AE%97%E6%9C%BA%E8%BE%93%E5%87%BA-%E6%A0%87%E7%AD%BE)
  * [HTML 引文、引用及标签定义](#html-%E5%BC%95%E6%96%87%E5%BC%95%E7%94%A8%E5%8F%8A%E6%A0%87%E7%AD%BE%E5%AE%9A%E4%B9%89)
- [HTML 链接](#html-%E9%93%BE%E6%8E%A5)
  * [1. href](#1-href)
  * [2. target](#2-target)
  * [3. rel](#3-rel)
  * [4. download](#4-download)
  * [5. title](#5-title)
  * [6. id](#6-id)
  * [7. hreflang](#7-hreflang)
  * [8. type](#8-type)
  * [9. class](#9-class)
  * [10. style](#10-style)
- [HTML head](#html-head)
  * [title 元素](#title-%E5%85%83%E7%B4%A0)
  * [base 元素](#base-%E5%85%83%E7%B4%A0)
  * [link 元素](#link-%E5%85%83%E7%B4%A0)
  * [style 元素](#style-%E5%85%83%E7%B4%A0)
  * [meta 元素](#meta-%E5%85%83%E7%B4%A0)
  * [script 元素](#script-%E5%85%83%E7%B4%A0)
- [css 基础学习](#css-%E5%9F%BA%E7%A1%80%E5%AD%A6%E4%B9%A0)
- [响应式仪表盘](#%E5%93%8D%E5%BA%94%E5%BC%8F%E4%BB%AA%E8%A1%A8%E7%9B%98)
- [踩坑记录](#%E8%B8%A9%E5%9D%91%E8%AE%B0%E5%BD%95)
- [参考资源](#%E5%8F%82%E8%80%83%E8%B5%84%E6%BA%90)

<!-- tocstop -->

## TODO LIST

2025-02-26

- [x] HTML 基础
- [x] HTML 元素
- [x] HTML 属性
- [x] HTML 标题
- [x] HTML 段落
- [x] HTML 文本格式化
- [x] HTML 链接
- [x] HTML head

2025-02-27

- [x] css基础

2025-02-28

- [x] 实现一个响应式仪表盘

## 环境配置

开发工具：neovim
node版本：20.18.0

## HTML 基础

HTML 标题（Heading）是通过`<h1> - <h6>` 标签来定义的。

```html
<h1>这是一个标题</h1>
<h2>这是一个标题</h2>
<h3>这是一个标题</h3>
```

HTML 段落是通过标签 `<p>` 来定义的。

```html
<p>这是一个段落。</p>
<p>这是另外一个段落。</p>
```

HTML 链接是通过标签 `<a>` 来定义的。

```html
<a href="https://www.runoob.com">这是一个链接</a>
```

HTML 图像是通过标签 `<img>` 来定义的.

```html
<img src="/images/logo.png" width="258" height="39" />
<!-- 网络图片 -->
<img
  src="https://th.bing.com/th/id/R.ffb2572d8f621f31d632fcb0a9947524?rik=xxaJsqmGoZLWdQ&riu=http%3a%2f%2fpic.kuaizhan.com%2fg3%2ff8%2fc4%2ff9e2-c03f-4afa-af6d-7b22091f9d4d99%2fimageView%2fv1%2fthumbnail%2f640x0&ehk=16sdTJ2KFXPOGZFAsTz7ktuhsr%2foo775NAXQYyakPyI%3d&risl=&pid=ImgRaw&r=0&sres=1&sresct=1"
  width="258"
  height="39"
/>
<!-- 原始大小 -->
<img
  src="https://th.bing.com/th/id/R.ffb2572d8f621f31d632fcb0a9947524?rik=xxaJsqmGoZLWdQ&riu=http%3a%2f%2fpic.kuaizhan.com%2fg3%2ff8%2fc4%2ff9e2-c03f-4afa-af6d-7b22091f9d4d99%2fimageView%2fv1%2fthumbnail%2f640x0&ehk=16sdTJ2KFXPOGZFAsTz7ktuhsr%2foo775NAXQYyakPyI%3d&risl=&pid=ImgRaw&r=0&sres=1&sresct=1"
/>
```

## HTML 元素

| 开始标签 \*              | 元素内容     | 结束标签 \* |
| ------------------------ | ------------ | ----------- |
| `<p>`                    | 这是一个段落 | `</p>`      |
| `<a href="default.htm">` | 这是一个链接 | `</a>`      |
| `<br>`                   | 换行         |             |

\*开始标签常被称为起始标签（opening tag），结束标签常称为闭合标签（closing tag）。

### 语法

- HTML 元素以开始标签起始
- HTML 元素以结束标签终止
- 元素的内容是开始标签与结束标签之间的内容
- 某些 HTML 元素具有空内容（empty content）
- 空元素在开始标签中进行关闭（以开始标签的结束而结束）
- 大多数 HTML 元素可拥有属性

### HTML 元素嵌套

大多数 HTML 元素可以嵌套（HTML 元素可以包含其他 HTML 元素）。

HTML 文档由相互嵌套的 HTML 元素构成。

多个HTML元素嵌套组成一个完整的HTML页面

包含3个元素的嵌套：

```html
<!DOCTYPE html>
<html>
  <body>
    <p>这是第一个段落。</p>
  </body>
</html>
```

### 空元素

没有内容的 HTML 元素被称为空元素。空元素是在开始标签中关闭的。

`<br>` 就是没有关闭标签的空元素（`<br>` 标签定义换行）。

在 XHTML、XML 以及未来版本的 HTML 中，所有元素都必须被关闭。

在开始标签中添加斜杠，比如 `<br />`，是关闭空元素的正确方法，HTML、XHTML 和 XML 都接受这种方式。

即使 `<br>` 在所有浏览器中都是有效的，但使用 `<br />` 其实是更长远的保障。

### HTML 提示：使用小写标签

HTML 标签对大小写不敏感：`<P>` 等同于 `<p>`。许多网站都使用大写的 HTML 标签。

因为万维网联盟（W3C）在 HTML 4 中推荐使用小写，而在未来 (X)HTML 版本中强制使用小写。

## HTML 属性

属性是 HTML 元素提供的附加信息。

属性通常出现在 HTML 标签的开始标签中，用于定义元素的行为、样式、内容或其他特性。

属性总是以 `name="value"` 的形式写在标签内，name 是属性的名称，value 是属性的值

### HTML 属性参考手册

查看完整的HTML属性列表: HTML 标签参考手册。

下面列出了适用于大多数 HTML 元素的属性：

| 属性名        | 适用元素                          | 说明                                                     |
| ------------- | --------------------------------- | -------------------------------------------------------- |
| `id`          | 所有元素                          | 为元素指定唯一的标识符                                   |
| `class`       | 所有元素                          | 为元素指定一个或多个类名，用于 CSS/JavaScript 选择       |
| `style`       | 所有元素                          | 直接在元素上应用 CSS 样式                                |
| `title`       | 所有元素                          | 提供额外提示信息（鼠标悬停时显示）                       |
| `data-*`      | 所有元素                          | 存储自定义数据（`*` 为自定义名称，如 `data-user`）       |
| `href`        | `<a>`, `<link>`                   | 指定链接的目标 URL                                       |
| `src`         | `<img>`, `<script>`, `<iframe>`   | 指定外部资源（图片/脚本/框架）的 URL                     |
| `alt`         | `<img>`                           | 图像无法显示时的替代文本                                 |
| `type`        | `<input>`, `<button>`             | 指定输入控件类型（如 `text`, `password`, `checkbox` 等） |
| `value`       | `<input>`, `<button>`, `<option>` | 指定元素的初始值                                         |
| `disabled`    | 表单元素                          | 禁用元素交互                                             |
| `checked`     | `<input type="checkbox/radio">`   | 指定复选框/单选框默认选中                                |
| `placeholder` | `<input>`, `<textarea>`           | 输入框中显示提示文本                                     |
| `target`      | `<a>`, `<form>`                   | 指定链接/表单提交的目标（如 `_blank` 新标签页）          |
| `readonly`    | 表单元素                          | 输入框只读（不可编辑）                                   |
| `required`    | 表单元素                          | 指定输入字段为必填项                                     |
| `autoplay`    | `<audio>`, `<video>`              | 自动播放媒体                                             |
| `onclick`     | 所有元素                          | 点击元素时触发 JavaScript 代码                           |
| `onmouseover` | 所有元素                          | 鼠标悬停时触发 JavaScript 代码                           |
| `onchange`    | 表单元素                          | 元素值变化时触发 JavaScript 代码                         |

样例模板，html代码

```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8" />
    <title>HTML 属性示例大全</title>
    <style>
      pre {
        background-color: #f5f5f5;
        padding: 15px;
        border-radius: 5px;
        border: 1px solid #ddd;
      }
      .comment {
        color: #666;
        margin: 20px 0 10px;
      }
    </style>
  </head>
  <body>
    <h1>HTML 属性示例</h1>

    <!-- ========== 全局属性 ========== -->
    <!-- id：为元素指定唯一的标识符。 -->
    <div id="header">This is the header</div>

    <!-- class：为元素指定一个或多个类名，用于 CSS 或 JavaScript 选择。 -->
    <p class="text highlight">This is a highlighted text.</p>

    <!-- style：用于直接在元素上应用 CSS 样式。 -->
    <p style="color: blue; font-size: 14px;">This is a styled paragraph.</p>

    <!-- title：为元素提供额外的提示信息，通常在鼠标悬停时显示。 -->
    <abbr title="HyperText Markup Language">HTML</abbr>

    <!-- data-*：用于存储自定义数据，通常通过 JavaScript 访问。 -->
    <div data-user-id="12345">User Info</div>

    <!-- ========== 特定元素属性 ========== -->
    <!-- href（用于 <a> 和 <link> 元素）：指定链接的目标 URL 。 -->
    <a href="https://www.example.com ">Visit Example</a>

    <!-- src（用于 <img>, <script>, <iframe> 等元素）：指定外部资源的 URL 。 -->
    <img src="image.jpg" alt="An example image" />

    <!-- alt（用于 <img> 元素）：为图像提供替代文本。 -->
    <img src="image.jpg" alt="An example image" />

    <!-- type（用于 <input> 和 <button> 元素）：指定输入控件的类型。 -->
    <input type="text" placeholder="Enter your name" />

    <!-- value（用于 <input>, <button>, <option> 等元素）：指定元素的初始值。 -->
    <input type="text" value="Default Value" />

    <!-- ========== 布尔属性 ========== -->
    <!-- disabled：禁用元素。 -->
    <input type="text" disabled />

    <!-- checked：指定复选框或单选按钮是否被选中。 -->
    <input type="checkbox" checked />

    <!-- readonly：使输入框只读。 -->
    <input type="text" readonly />

    <!-- required：指定输入字段为必填项。 -->
    <input type="text" required />

    <!-- autoplay（用于 <audio> 和 <video> 元素）：自动播放媒体。 -->
    <video src="video.mp4" autoplay></video>

    <!-- ========== 自定义属性 ========== -->
    <!-- data-*：用于存储自定义数据。 -->
    <div data-user-id="12345" data-role="admin">User Info</div>

    <!-- ========== 事件处理属性 ========== -->
    <!-- onclick：当用户点击元素时触发。 -->
    <button onclick="alert('Button clicked!')">Click Me</button>

    <!-- onmouseover：当用户将鼠标悬停在元素上时触发。 -->
    <div onmouseover="this.style.backgroundColor='yellow'">Hover over me</div>

    <!-- onchange：当元素的值发生变化时触发。 -->
    <input type="text" onchange="alert('Value changed!')" />
  </body>
</html>
```

## HTML 标题

### 标题很重要

请确保将 HTML 标题 标签只用于标题。不要仅仅是为了生成粗体或大号的文本而使用标题。

搜索引擎使用标题为您的网页的结构和内容编制索引。

因为用户可以通过标题来快速浏览您的网页，所以用标题来呈现文档结构是很重要的。

应该将 h1 用作主标题（最重要的），其后是 h2（次重要的），再其次是 h3，以此类推。

| 标签          | 描述           |
| ------------- | -------------- |
| `<html>`      | 定义 HTML 文档 |
| `<body>`      | 定义文档的主体 |
| `<h1> - <h6>` | 定义 HTML 标题 |
| `<hr>`        | 定义水平线     |
| `<!--...-->`  | 定义注释       |

## HTML 段落

段落是通过 `<p>` 标签定义的。

```html
<p>这是一个段落</p>
<p>这是另一个段落</p>
```

如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 `<br>` 标签：

```html
<p>这个<br />段落<br />演示了分行的效果</p>
```

`<p>` 分段 `<br>` 分行

## HTML 文本格式化

### HTML 文本格式化标签

| 标签       | 描述              |
| ---------- | ----------------- |
| `<b>`      | 定义粗体文本      |
| `<em>`     | 定义着重文字      |
| `<i>`      | 定义斜体字        |
| `<small>`  | 定义小号字        |
| `<strong>` | 定义加重语气      |
| `<sub>`    | 定义下标字        |
| `<sup>`    | 定义上标字        |
| `<ins>`    | 定义插入字,下划线 |
| `<del>`    | 定义删除字        |

### HTML "计算机输出" 标签

| 标签     | 描述               |
| -------- | ------------------ |
| `<code>` | 定义计算机代码     |
| `<kbd>`  | 定义键盘码         |
| `<samp>` | 定义计算机代码样本 |
| `<var>`  | 定义变量           |
| `<pre>`  | 定义预格式文本     |

### HTML 引文、引用及标签定义

| 标签           | 描述             |
| -------------- | ---------------- |
| `<abbr>`       | 定义缩写         |
| `<address>`    | 定义地址         |
| `<bdo>`        | 定义文字方向     |
| `<blockquote>` | 定义长的引用     |
| `<q>`          | 定义短的引用语   |
| `<cite>`       | 定义引用、引证   |
| `<dfn>`        | 定义一个定义项目 |

## HTML 链接

HTML 链接（Anchor）是网页之间跳转的核心部分。

HTML 使用链接与网络上的另一个文档相连。

HTML中的链接是一种用于在不同网页之间导航的元素。

链接通常用于将一个网页与另一个网页或资源（如文档、图像、音频文件等）相关联。

链接允许用户在浏览网页时单击文本或图像来跳转到其他位置，从而实现网页之间的互联。

HTML 链接 通过 `<a>` 标签创建，通常用于将用户从一个页面导航到另一个页面、从一个部分跳转到页面中的另一个部分、下载文件、打开电子邮件应用程序或执行 JavaScript 函数等。

### 1. href

- **功能**：定义链接目标（网页/文件/邮件/电话/JavaScript）
- **示例**：

  ```html
  <a href="https://www.example.com">访问 Example</a>
  ```

### 2. target

- **取值**：
  - `_blank`：新窗口/标签打开
  - `_self`：当前窗口打开（默认）
  - `_parent`：父框架打开
  - `_top`：全窗口打开（无视框架）
- **示例**：

  ```html
  <a href="https://www.example.com" target="_blank" rel="noopener"
    >新窗口打开</a
  >
  ```

### 3. rel

- **常用值**：
  - `nofollow`：禁止搜索引擎跟踪
  - `noopener`：防止新页面访问`window.opener`
  - `noreferrer`：不发送Referer头
- **组合使用**：

  ```html
  <a href="https://www.example.com" rel="noopener noreferrer">安全链接</a>
  ```

### 4. download

- **功能**：强制下载链接资源
- **命名下载**：

  ```html
  <a href="file.pdf" download="example.pdf">下载文件</a>
  ```

### 5. title

- **功能**：鼠标悬停提示文本
- **示例**：

  ```html
  <a href="https://www.example.com" title="访问 Example 网站">访问 Example</a>
  ```

### 6. id

- **功能**：页面锚点跳转
- **示例**：

  ```html
  <a href="#section1">跳转到第1部分</a>
  <div id="section1">内容区域</div>
  ```

### 7. hreflang

- **功能**：指定目标页面语言
- **示例**：

  ```html
  <a href="https://www.example.com/es" hreflang="es">西班牙语网站</a>
  ```

### 8. type

- **功能**：声明资源MIME类型
- **示例**：

  ```html
  <a href="style.css" type="text/css">CSS样式表</a>
  ```

### 9. class

- **功能**：CSS类选择器
- **示例**：

  ```html
  <a href="https://www.example.com" class="external-link">外部链接</a>
  ```

### 10. style

- **功能**：内联CSS样式
- **示例**：

  ```html
  <a href="https://www.example.com" style="color: red;">红色链接</a>
  ```

## HTML head

`<head>` 元素包含了所有的头部标签元素。在 `<head>`元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。

可以添加在头部区域的元素标签为: `<title>`, `<style>`, `<meta>`, `<link>`, `<script>`, `<noscript>` 和 `<base>`。

所有头部元素应放置在 `<head>` 标签内，建议的书写顺序：`<title>` → `<base>` → `<meta>` → `<link>` → `<style>` → `<script>`

### title 元素

- **作用**: 定义文档标题
- **必要性**: HTML/XHTML 文档必须包含
- **功能特性**:
  - 显示在浏览器工具栏
  - 作为收藏夹中的保存标题
  - 显示在搜索引擎结果页面
- **示例**:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>文档标题</title>
  </head>
  <body>
    文档内容......
  </body>
</html>
```

### base 元素

- **作用**: 为页面所有相对链接设置默认地址/目标
- **属性**:
  - `href`: 基础链接地址
  - `target`: 默认打开方式（如 \_blank,\_self 等）
- **示例**:

```html
<head>
  <base href="https://www.example.com/images/" target="_blank" />
</head>
```

### link 元素

- **作用**: 定义文档与外部资源的关系
- **典型用途**: 链接 CSS 样式表
- **属性**:
  - `rel`: 关系类型（如 stylesheet）
  - `type`: MIME 类型（如 text/css）
  - `href`: 资源路径
- **示例**:

```html
<head>
  <link rel="stylesheet" type="text/css" href="mystyle.css" />
</head>
```

### style 元素

- **作用**: 定义文档内嵌样式
- **示例**:

```html
<head>
  <style type="text/css">
    body {
      background-color: yellow;
    }
    p {
      color: blue;
    }
  </style>
</head>
```

### meta 元素

- **作用**: 提供文档元数据
- **常见用途**:

| 属性                 | 示例                                           | 用途说明               |
| -------------------- | ---------------------------------------------- | ---------------------- |
| name="keywords"      | `<meta name="keywords" content="HTML, CSS">`   | 定义搜索引擎关键词     |
| name="description"   | `<meta name="description" content="免费教程">` | 定义页面描述           |
| name="author"        | `<meta name="author" content="作者名">`        | 声明页面作者           |
| http-equiv="refresh" | `<meta http-equiv="refresh" content="30">`     | 设置页面刷新间隔（秒） |

### script 元素

- **作用**: 加载客户端脚本（如 JavaScript）
- **注意**: 可放置在 `<head>` 或 `<body>` 中
- **示例**:

```html
<script>
  function myFunction() {
    document.getElementById("demo").innerHTML = "Hello JavaScript!";
  }
</script>

<!-- 外部脚本示例 -->
<script src="myscripts.js"></script>
```

## css 基础学习

东西很多

## 响应式仪表盘

```html
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>响应式仪表盘</title>
    <style>
      /* 顶部展示区 */
      .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px 20px;
        background-color: #f0f0f0;
        flex-wrap: wrap;
      }

      .header-left {
        display: flex;
        align-items: center;
        flex-shrink: 1;
      }

      .logo {
        max-width: 100px;
        height: auto;
      }

      .company-name {
        font-size: 24px;
        margin-left: 10px;
        white-space: nowrap;
      }

      .header-right {
        display: flex;
        align-items: center;
        flex-wrap: wrap;
      }

      .device-stats {
        margin-right: 20px;
        white-space: nowrap;
      }

      .add-device-btn {
        padding: 10px 20px;
        background-color: #00000f;
        color: white; /*字体颜色*/
        border: none;
        border-radius: 5px;
        cursor: pointer;
        white-space: nowrap;
      }

      /* 动态变化设置 */
      @media (max-width: 768px) {
        .header {
          flex-direction: column;
          align-items: flex-start;
        }
        .header-right {
          margin-top: 10px;
        }
      }

      @media (max-width: 480px) {
        .header-right {
          flex-direction: column;
          align-items: flex-start;
        }
        .device-stats {
          margin-bottom: 10px;
        }
      }
      /* 设备卡片区域 */
      .main-content {
        display: flex;
        flex-wrap: wrap;
        padding: 20px;
      }

      .device-card {
        width: calc(33.33% - 20px);
        margin: 10px;
        padding: 20px;
        background-color: #fff;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        border-radius: 5px;
      }

      .device-card h3 {
        margin: 0 0 10px 0;
      }

      .device-card p {
        margin: 0 0 10px 0;
      }

      .delete-btn,
      .detail-btn {
        padding: 5px 10px;
        margin-right: 10px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
      }

      .delete-btn {
        background-color: #dc3545;
        color: white;
      }

      .detail-btn {
        background-color: #007bff;
        color: white;
      }

      @media (max-width: 768px) {
        .device-card {
          width: calc(50% - 20px);
        }
      }

      @media (max-width: 480px) {
        .device-card {
          width: 100%;
        }
      }

      /* 设备详情页面 */

      .detail-content {
        padding: 20px;
        background-color: #fff;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        border-radius: 5px;
        max-width: 600px;
        margin: 20px auto;
      }

      .detail-content h2 {
        margin-bottom: 20px;
      }

      .detail-content p {
        margin: 10px 0;
      }

      .back-btn {
        padding: 10px 20px;
        background-color: #6c757d;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
      }
    </style>
  </head>
  <body>
    <header class="header">
      <div class="head-left">
        <img src="logo.png" alt="Logo" class="logo" />
        <h1 class="company-name">公司名称</h1>
      </div>
      <div class="header-right">
        <div class="device-stats">
          <span>设备总数：100</span>
          <span>离线设备：5</span>
        </div>
        <button class="add-device-btn">添加设备</button>
      </div>
    </header>

    <main class="main-content">
      <div class="device-card">
        <h3>设备名称</h3>
        <p>ai地址</p>
        <button class="delete-btn">删除</button>
        <button class="detail-btn">详细信息</button>
      </div>
      <div class="device-card">
        <h3>设备名称2</h3>
        <p>ai地址</p>
        <button class="delete-btn">删除</button>
        <button class="detail-btn">详细信息</button>
      </div>
      <div class="device-card">
        <h3>设备名称3</h3>
        <p>ai地址</p>
        <button class="delete-btn">删除</button>
        <button class="detail-btn">详细信息</button>
      </div>
    </main>
  </body>
</html>
```

## 踩坑记录

基础学习，没有踩坑记录

## 参考资源

- [菜鸟教程](https://www.runoob.com/html/html-basic.html)
