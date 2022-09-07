# html 文本格式化

<img src="https://gitee.com/chenyonwu/blogimage/raw/master/img/202209061719144.jpg"/>

## 1 文本格式化标签

| 标签       | 描述               |
| ---------- | ------------------ |
| `<b>`      | 粗体文本           |
| `<strong>` | 粗体文本，加重语气 |
| `<i>`      | 斜体字             |
| `<em>`     | 斜体字，着重文字   |
| `<small>`  | 小号字             |
| `<sub>`    | 下标字             |
| `<sup>`    | 上标字             |
| `<ins>`    | 插入字             |
| `<del>`    | 删除字             |

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>文本格式化</title>
  </head>
  <body>
    <!-- 
      b标签定义粗体文本
      
      根据HTML 5的规范，b标签应该作为最后的选择，只有在没有其他标记比较合适时才使用它。HTML 5规范声明：标题应该用h1-h6标签表示，被强调的文本应该用em标签表示，重要的文本应该用strong标签标识，被标记的或者高亮显示的文本应该是mark标签标识
     -->
    <p>这是一个普通的文本-<b>这是一个加粗文本</b>。</p>

    <!-- 
      i标签定义斜体文本
     -->
    <p><i>fundamental</i> html learning</p>

    <!-- small标签定义小号文本 -->
    <p>welcom to hust.</p>
    <p><small> Copyright 2022 by chenyonwu.</small></p>

    <!-- sub定义下标文本，sup定义上标文本 -->
    <p>这个文本包含 <sub>下标</sub>文本。</p>
    <p>这个文本包含 <sup>上标</sup> 文本。</p>

    <!-- del标签定义被删除文本, ins标签定义被插入文本 -->
    <p>My favorite color is <del>blue</del> <ins>red</ins>!</p>
  </body>
</html>
```

## 2 引文，引用，及标签定义

| 标签           | 描述       |
| -------------- | ---------- |
| `<abbr>`       | 缩写       |
| `<address>`    | 地址       |
| `<blockquote>` | 长的引用   |
| `<q>`          | 短的引用语 |
| `<cite>`       | 引用、引证 |

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>文本格式化</title>
  </head>
  <body>
    <!-- abbr标签定义一个缩写 -->
    <p>
      The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.
    </p>

    <!-- address标签定义文档作者或拥有者的联系信息 -->
    <p>
      <address>
        Written by <a href="1906167102@qq.com">chenyonwu</a>.<br />
        Visit us at:<br />
        qq.com<br />
        hust
      </address>
    </p>

    <!-- blockquote标签定义一个摘自另一个源的块引用 -->
    <blockquote cite="http://www.worldwildlife.org/who/index.html">
      For 50 years, WWF has been protecting the future of nature. The world's leading conservation organization, WWF
      works in 100 countries and is supported by 1.2 million members in the United States and close to 5 million
      globally.
    </blockquote>

    <!-- q标签定义短引用 -->
    <p>
      WWF's goal is to:
      <q>Build a future where people live in harmony with nature.</q>
      We hope they succeed.
    </p>

    <!-- cite标签定义引用 -->
    <p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>
  </body>
</html>
```

