# html 元素解析与基础

<img src="https://gitee.com/chenyonwu/blogimage/raw/master/img/202209061719144.jpg"/>

## 1 元素解析

### 1.1 元素

![image-20220906195731716](https://gitee.com/chenyonwu/blogimage/raw/master/img/202209061957811.png)

HTML文档由 HTML 元素定义

- 元素以**开始标签**起始，以**结束标签**终止
- 开始标签与结束标签中间的内容即为**元素的内容**
- 某些元素具有空内容，如`<img />`。这样的标签**在开始标签进行关闭**
- 大多数元素可以拥有**属性**

### 1.2 属性

属性是 HTML 元素提供的附加信息，一般描述于**开始标签**，总是以**名称/值**对的形式出现，比如：`name="value"`

```html
<a href="https://www.bilibili.com/">点我进入b站</a>
```

HTML 的全局属性完整列表如下：

| 属性            | 描述                                                       |
| --------------- | ---------------------------------------------------------- |
| contenteditable | 规定是否可编辑元素的内容                                   |
| contextmenu     | 指定一个元素的上下文菜单。当用户右击该元素，出现上下文菜单 |
| data-           | 用于存储页面的自定义数据                                   |
| dir             | 设置元素中内容的文本方向                                   |
| lang            | 设置元素中内容的语言代码                                   |
| accesskey       | 设置访问元素的键盘快捷键                                   |
| draggable       | 指定某个元素是否可以拖动                                   |
| dropzone        | 指定是否将数据复制，移动，或链接，或删除                   |
| hidden          | hidden 属性规定对元素进行隐藏                              |
| spellcheck      | 检测元素是否拼写错误                                       |
| tabindex        | 设置元素的 Tab 键控制次序                                  |
| title           | 规定元素的额外信息                                         |
| translate       | 指定是否一个元素的值在页面载入时是否需要翻译               |

## 2 基础示例

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
<!-- html标签用于定义一个html文档 -->
<html>
  <!-- head标签用于定义关于文档的信息 -->
  <head>
    <!-- meta标签用于定义关于文档的元信息 -->
    <!-- 设置文字编码为UTF-8 -->
    <meta charset="UTF-8" />
    <!-- 
       IE兼容性设置，有 IE=5、IE=7、IE=8、IE=edge、IE=Edge,chrome=1、IE=EmulateIE7 这些模式
 
       IE=edge模式通知 Windows Internet Explorer 以最高级别的可用模式显示内容
      -->
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <!-- 
       移动端和pc端不同。现在手机屏幕分辨率越来越高，但屏幕大小并没有太大的变化，这意味着每个物理像素里装了多个实际像素。
       
       还有一个因素也会引起css中px的变化，那就是用户缩放。例如，当用户把页面放大一倍，那么css中1px所代表的物理像素也会增加一倍；反之把页面缩小一倍，css中1px所代表的物理像素也会减少一倍。
 
       所以在做移动端开发时，为了使移动端的页面在不同的手机上同样的大小来显示，我们可以将页面的宽度固定，然后获取设备的宽度，可以得到我们之前设定的宽度与设备宽度的比例，再使用HTML5新增的viewport来对页面进行缩放，并固定不允许用户再重新缩放。
 
       layout viewport 使网页的所有内容，它可以全部或部分展示给用户
 
       visual viewport 就是当前显示给用户内容的窗口，我们可以拖动或者放大缩小网页
         - width 设置layout viewport的宽度，为一个正整数，或字符串“width-device”
         - initial-scale 设置页面的初始缩放值，为一个数字，可以带小数
         - minimum-scale 允许用户的最小缩放值，为一个数字，可以带小数
         - maximum-scale 允许用户的最大缩放值，为一个数字，可以带小数
         - height 设置layout viewport的高度，不重要，很少使用
         - user-scalable 是否允许用户进行缩放，可选值为"yes"或"no"
 
       总之一切都是为了适应手机端网页的浏览
      -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!-- title标签为文档定义一个标题 -->
    <title>HTML基础</title>
    <!-- 
       base标签定义页面中所有链接的默认地址或默认目标
       
       在base标签作用下
         <img src="example-01.jpg"> 相当于
         <img src="/here/is/my/deeply/nested/set/of/images/example-01.jpg">
     -->
    <base href="http://example.com/here/is/my/deeply/nested/set/of/images/" />
    <!-- style标签定义文档的样式信息 -->
    <style>
      body {
        background-color: orangered;
      }
    </style>
    <!-- script标签定义客户端脚本 -->
    <script>
      window.onload = function () {
        console.log('hello, world')
      }
    </script>
    <!-- link标签定义文档与外部资源的关系 -->
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>一级标题</h1>
    <h2>二级标题</h2>
    <h3>三级标题</h3>
    <h4>四级标题</h4>
    <h5>五级标题</h5>
    <h6>六级标题</h6>

    <!-- p标签定义一个段落 -->
    <p>
      HTML stands for HyperText Markup Language. It's a markup language that web developers use to structure and
      describe the content of a webpage (not a programming language).
    </p>

    <!-- br标签定义简单的换行 -->
    <br />
    <!-- hr标签定义水平线 -->
    <hr />

    <!-- a标签定义超文本链接 -->
    <a href="https://www.bilibili.com/" target="_blank">点我进入b站</a>

    <!-- button标签定义一个点击按钮 -->
    <button onclick="alert('hello, world~')">点我一下</button>

    <!-- img标签定义图像 -->
    <img src="image1.jpg" alt="这是图片1的描述" />

    <!-- 有序列表 -->
    <ol>
      <li>第一</li>
      <li>第二</li>
      <li>第三</li>
    </ol>

    <!-- 无序列表 -->
    <ul>
      <li>第一</li>
      <li>第二</li>
      <li>第三</li>
    </ul>
  </body>
</html>
```

