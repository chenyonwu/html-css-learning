# html 表格

<img src="https://gitee.com/chenyonwu/blogimage/raw/master/img/202209062022305.jpeg"/>

表格由 `<table>` 标签来定义。每个表格均有若干行（由 `<tr>` 标签定义），每行被分割为若干单元格（由 `<td>` 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容

数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等

**表格的普通实例**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <!-- table标签定义一个表格 -->
    <table border="1">
      <!-- caption标签定义表格标题 -->
      <caption>
        Monthly savings
      </caption>
      <!-- thead标签定义表格中的表头内容 -->
      <thead>
        <!-- tr标签定义表格中的行 -->
        <tr>
          <!-- th标签表格中的表头单元格 -->
          <th>Month</th>
          <th>Savings</th>
        </tr>
      </thead>
      <!-- tbody标签定义表格中的主体内容 -->
      <tbody>
        <tr>
          <!-- td定义表格中的单元 -->
          <td>January</td>
          <td>$100</td>
        </tr>
        <tr>
          <td>February</td>
          <td>$80</td>
        </tr>
      </tbody>
      <!-- tfoot定义表格中的表注内容（脚注） -->
      <tfoot>
        <tr>
          <td>Sum</td>
          <td>$180</td>
        </tr>
      </tfoot>
    </table>

    <table border="1">
      <!-- colgroup标签定义表格中供格式化的列祖 -->
      <colgroup>
        <!-- col标签定义表格中一个或多个列的属性值 -->
        <col span="2" style="background-color: red" />
        <col style="background-color: yellow" />
      </colgroup>
      <tr>
        <th>ISBN</th>
        <th>Title</th>
        <th>Price</th>
      </tr>
      <tr>
        <td>3476896</td>
        <td>My first HTML</td>
        <td>$53</td>
      </tr>
    </table>
  </body>
</html>
```

## 没有边框的表格

设置`<table border="0">`可以去除所有的边框。

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <h4>这个表格没有边框:</h4>
    <table border="0">
      <tr>
        <td>100</td>
        <td>200</td>
        <td>300</td>
      </tr>
      <tr>
        <td>400</td>
        <td>500</td>
        <td>600</td>
      </tr>
    </table>
  </body>
</html>
```

## 表格设置表头

`<th>`用于设置表头

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <h4>垂直标题:</h4>
    <table border="1">
      <tr>
        <th>First Name:</th>
        <td>Bill Gates</td>
      </tr>
      <tr>
        <th>Telephone:</th>
        <td>555 77 854</td>
      </tr>
      <tr>
        <th>Telephone:</th>
        <td>555 77 855</td>
      </tr>
    </table>
  </body>
</html>
```

## 表格设置标题

`<caption>`标签用于设置标题

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <table border="1">
      <caption>
        Monthly savings
      </caption>
      <tr>
        <th>Month</th>
        <th>Savings</th>
      </tr>
      <tr>
        <td>January</td>
        <td>$100</td>
      </tr>
      <tr>
        <td>February</td>
        <td>$50</td>
      </tr>
    </table>
  </body>
</html>
```

## 跨行或跨列的表格

`clospan`和`rowspan`属性设置单元格跨列和跨行

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <h4>单元格跨两列:</h4>
    <table border="1">
      <tr>
        <th>Name</th>
        <th colspan="2">Telephone</th>
      </tr>
      <tr>
        <td>Bill Gates</td>
        <td>555 77 854</td>
        <td>555 77 855</td>
      </tr>
    </table>

    <h4>单元格跨两行:</h4>
    <table border="1">
      <tr>
        <th>First Name:</th>
        <td>Bill Gates</td>
      </tr>
      <tr>
        <th rowspan="2">Telephone:</th>
        <td>555 77 854</td>
      </tr>
      <tr>
        <td>555 77 855</td>
      </tr>
    </table>
  </body>
</html>
```

## 单元格内嵌套标签

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <h4>单元格跨两列:</h4>
    <table border="1">
      <tr>
        <td>
          <p>这是一个段落</p>
          <p>这是另一个段落</p>
        </td>
        <td>
          这个单元格包含一个表格:
          <table border="1">
            <tr>
              <td>A</td>
              <td>B</td>
            </tr>
            <tr>
              <td>C</td>
              <td>D</td>
            </tr>
          </table>
        </td>
      </tr>
      <tr>
        <td>
          这个单元格包含一个列表
          <ul>
            <li>apples</li>
            <li>bananas</li>
            <li>pineapples</li>
          </ul>
        </td>
        <td>HELLO</td>
      </tr>
    </table>
  </body>
</html>
```

## 单元格设置边距

`cellpadding`属性设置单元格边距

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <h4>没有单元格边距:</h4>
    <table border="1">
      <tr>
        <td>First</td>
        <td>Row</td>
      </tr>
      <tr>
        <td>Second</td>
        <td>Row</td>
      </tr>
    </table>

    <h4>有单元格边距:</h4>
    <table border="1" cellpadding="10">
      <tr>
        <td>First</td>
        <td>Row</td>
      </tr>
      <tr>
        <td>Second</td>
        <td>Row</td>
      </tr>
    </table>
  </body>
</html>
```

## 单元格间距

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>html 表格</title>
  </head>
  <body>
    <h4>没有单元格间距:</h4>
    <table border="1">
      <tr>
        <td>First</td>
        <td>Row</td>
      </tr>
      <tr>
        <td>Second</td>
        <td>Row</td>
      </tr>
    </table>

    <h4>单元格间距="0":</h4>
    <table border="1" cellspacing="0">
      <tr>
        <td>First</td>
        <td>Row</td>
      </tr>
      <tr>
        <td>Second</td>
        <td>Row</td>
      </tr>
    </table>

    <h4>单元格间距="10":</h4>
    <table border="1" cellspacing="10">
      <tr>
        <td>First</td>
        <td>Row</td>
      </tr>
      <tr>
        <td>Second</td>
        <td>Row</td>
      </tr>
    </table>
  </body>
</html>
```

