# html 图像

图像由`<img>`标签定义。

`<img>`标签是空标签，只包含属性，并且没有闭合标签。

**定义图像的语法是：**

```html
<img src="url" alt="some_text" width="width" height="height">
```

- url 指图像存储的位置
- alt 属性用来为图像定义一串预备的可替换的文本。在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。

**面试问题：**`<img>`的`title`和`alt`有什么区别

- `title` 通常当鼠标滑动到元素上的时候显示
- `alt`是`<img>`的特有属性，是图片内容的等价描述，用于图片无法加载时显示、读屏器阅读图片。可提图片高可访问性，除了纯装饰图片外都必须设置有意义的值，搜索引擎会重点分析