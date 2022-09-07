# html5 新元素与被移除的元素

<img src="https://gitee.com/chenyonwu/blogimage/raw/master/img/202209062022305.jpeg"/>

## 1 html5 简介

### 1.1 html5 新特性

HTML5 中的一些有趣的新特性：

- 用于绘画的 canvas 元素
- 用于媒介回放的 video 和 audio 元素
- 对本地离线存储的更好的支持
- 新的特殊内容元素，比如 article、footer、header、nav、section
- 新的表单控件，比如 calendar、date、time、email、url、search

### 1.2 DOCTYPE 声明

```html
<!-- 
  DOCTYPE的作用是定义文档类型，声明文档的解析类型，避免浏览器的怪异模式

  怪异模式（BackCompat），浏览器使用自己的怪异模式解析渲染页面

  标准模式（CSS1Compat），浏览器使用W3C的标准解析渲染页面

  DOCTYPE属性会被浏览器识别并使用，但是如果页面中没有DOCTYPE的声明，那么compatMOde 默认就是BackCompat，这就是噩梦的开始——浏览器会按照自己的方式解析渲染，那么不同的浏览器就会显示不同的样式

  在页面中添加<!DOCTYPE html>就等同于开启了标准模式，那么浏览器就得老老实实的按照W3C的标准解析渲染页面，这样我们编写的页面在所有的浏览器中就都是一个样子。

  要注意，<!DOCTYPE> 声明不是HTML标签，它是指示web浏览器关于页面使用哪个HTML版本进行编写的指令。

  在HTML 4.01中，<!DOCTYPE>声明引用 DTD，因为HTML 4.01基于SGML。DTD规定了标记语言的规则，这样浏览器才能正确地呈现内容。HTML5 不基于SGML，所以不需要引用 DTD。

  在HTML5中声明<!DOCTYPE>只有一种方式：<!DOCTYPE html>，没有结束标签，对大小写不敏感

  在HTML 4.01中则有三种声明<!DOCTYPE>的方式：
    1. HTML 4.01 Strict 
      该DTD包含所有 HTML 元素和属性，但不包括展示性的和弃用的元素（比如font）。不允许框架集（Framesets）
      <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
    2. HTML 4.01 Transitional
      该DTD包含所有HTML元素和属性，包括展示性的和弃用的元素（比如font）。不允许框架集（Framesets）
      <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd"
    3. HTML 4.01 Frameset
      该DTD等同于HTML 4.01 Transitional，但允许框架集内容
      <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
 -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body></body>
</html>
```

### 1.3 html5 改进

- 新元素
- 新属性
- 完全支持 CSS3
- Video 和 Audio
- 2D/3D 制图
- 本地存储
- 本地 SQL 数据
- Web 应用

### 1.4 html5 应用

使用 HTML5 你可以简单地开发应用：

- 本地数据存储
- 访问本地文件
- 本地 SQL 数据
- 缓存引用
- Javascript 工作者
- XHTMLHttpRequest 2

## 2 新元素

HTML5添加了很多新元素及功能，比如: 图形的绘制，多媒体内容，更好的页面结构，更好的形式 处理，和几个api拖放元素，定位，包括网页 应用程序缓存，存储，网络工作者，等。

### 2.1 canvas 新元素

`<canvas>`标签定义图形，比如图标和其他图像。该标签基于 JavaScript 的绘图 API

### 2.2 新多媒体元素

| 标签       | 描述                                                         |
| ---------- | ------------------------------------------------------------ |
| `<audio>`  | 音频内容                                                     |
| `<video>`  | 视频                                                         |
| `<source>` | 定义多媒体资源 `<video>` 和 `<audio>`                        |
| `<embed>`  | 定义多媒体资源`<video>` 和 `<audio>`                         |
| `<track>`  | 为诸如`<video>` 和 `<audio>`元素之类的媒介规定**外部文本轨道** |

### 2.3. 新表单元素

| 标签         | 描述                               |
| ------------ | ---------------------------------- |
| `<datalist>` | 定义选项列表                       |
| `<keygen>`   | 规定用于表单的密钥对生成器字段     |
| `<output>`   | 定义不同类型的输出，比如脚本的输出 |

### 2.4 新的语言和结构元素

HTML5提供了新的元素来创建更好的页面结构：

| 标签         | 描述                                     |
| ------------ | ---------------------------------------- |
| `<article`   | 页面独立的内容区域                       |
| `<aside>`    | 页面的侧边栏内容                         |
| `<command>`  | 命令按钮，比如单选按钮、复选框或按钮     |
| `<details>`  | 描述文档或文档某个部分的细节             |
| `<dialog>`   | 对话框，比如提示框                       |
| `<summary>`  | 标签包含 details 元素的标题              |
| `<footer>`   | 定义 section 或 document 的页脚          |
| `<header>`   | 文档的头部区域                           |
| `<mark>`     | 带有记号的文本                           |
| `<meter>`    | 定义度量衡。仅用于已知最大和最小值的度量 |
| `<nav>`      | 导航链接的部分                           |
| `<progress>` | 任何类型的任务的进度                     |
| `<section>`  | 文档中的节（section、区段）              |
| `<time>`     | 日期或时间                               |

## 3 被移除的元素

以下的 HTML 4.01 元素在HTML5中已经被删除：

- `<acronym>`
- `<applet>`
- `<big>`
- `<center>`
- `<dir>`
- `<font>`
- `<frame>`
- `<frameset>`
- `<noframes>`
- `<strike>`
- `<tt>`