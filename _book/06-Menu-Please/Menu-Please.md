# 请给个菜单

> 来源：[Menu, Please!](http://howtocodeinhtml.com/chapter6.html)

网站的另一个受欢迎的部分是菜单。基本上，它是一个项目列表，通常只是简单的链接指向网站上的其他位置。让我们来实现吧！我们将从以下HTML代码开始：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
      <meta charset="utf-8">
      <title>Menu</title>
      <link rel="stylesheet" href="main.css" media="screen">
  </head>
  <body>
    <nav>
      <ul>
        <li>
          <a href="index.html">Home</a>
        </li>
        <li>
          <a href="training.html">Training</a>
        </li>
        <li>
          <a href="conferences.html">Conferences</a>
        </li>
        <li>
          <a href="about.html">About us</a>
        </li>
      </ul>
    </nav>
  </body>
</html>
```

我们的菜单包括四个项目：

- Home
- Training
- Conferences
- About us

我们希望它看起来像这样：

![menu-preview.png](https://i.loli.net/2018/11/22/5bf64749e86aa.png)

您可能会注意到，在标记下，我们添加了新标记 < nav>，< ul>和< li>。

< nav> 用于指定包含内部或外部信息链接的网站上的各种导航功能。因此，将< nav>放入代码中会说 “< nav> 中的所有内容都将用于浏览网站。”

在 < nav> 中，我们放置 < ul> 标记，后跟几个 < li> 标记。标签 < ul> 表示“无序列表”（如子弹列表），< li> 标签表示该列表的每个单独组件（单个项目符号）。在创建网站时，在映射菜单页面时，无序列表通常是最合理的选择。实际上，菜单是一种链接列表，它是在没有关于其元素顺序的预定规则的情况下创建的。

只有上面的代码仍未完成，我们的列表应显示如下：

![pure-list.png](https://i.loli.net/2018/11/22/5bf6474a1df10.png)

当您想要创建带有项目符号的列表时，即使在文字处理器上创建文本文档时，您可能也会看到类似的内容。但是，如果没有 CSS <  ul>，我们的列表将以 “.” 开头。相比之下，我们的菜单可能要复杂得多。我们可以给它一个边框，颜色，背景等。每个链接默认显示为蓝色，如上图所示。

现在让我们尝试在 CSS 代码中生成一个更加风格化的菜单。

通常，我们从 HTML 代码中最常用的标记开始，对吧？在这种情况下，最顶层的代码以 < nav> 开头，因为它负责我们的导航菜单。在此标记内，没有太多事情要做，因为此标记不直接处理项目符号列表的外观变化。 

接下来的标签是 < ul>，它开始无序列表。我们希望我们的列表显示与默认列表略有不同。最重要的是要有一个新的背景：

```css
nav ul {
  background-color: PaleVioletRed;
}
```

对于背景颜色，我们选择名称 PaleVioletRed。重新加载页面会显示添加此代码后的更改。

![list-background.png](https://i.loli.net/2018/11/22/5bf6471b52c0a.png)

实际上，我们已经将青色应用为<ul>的整个元素的背景。这是因为我们将其应用于 < nav>和 < ul>标签，如下面的选择器所示。

```css
nav ul {}
```

现在我们想摆脱这个列表中的黑色圆点，使它看起来更像菜单。我们可以隐藏它，这要归功于属性 “list-style”，如下所示：

```css
nav ul {
  background-color: PaleVioletRed;
  list-style: none;
}
```

将 list-style 设置为 none 会使列表没有区别标记。

看起来好多了：

![menu-no-bullets.png](https://i.loli.net/2018/11/22/5bf6471bf22dc.png)

大片的颜色令人惊讶地大。我们将使用与之前图像边界相同的练习（例如填充）将其修剪一下。

```css
nav ul {
  background-color: PaleVioletRed;
  list-style: none;
  padding: 0;
}
```

正如你在下面看到的，它现在看起来好多了，慢慢接近一个漂亮的形式：

![menu-no-padding.png](https://i.loli.net/2018/11/22/5bf6471c1781d.png)

现在是时候处理尺寸了。我们的导航必须是 200 像素宽：

```css
nav ul {
  background-color: PaleVioletRed;
  list-style: none;
  padding: 0;
  width: 200px;
}
```

最后，我们将在列表中添加一个与图像完全相同的边框。它将以实线表示，具有 1 像素宽度和 “浅蓝” 颜色：

```css
nav ul {
  background-color: PaleVioletRed;
  list-style: none;
  padding: 0;
  width: 200px;
  border: 1px solid MediumVioletRed;
}
```

这是结果，它看起来很棒！

![menu-border.png](https://i.loli.net/2018/11/22/5bf6471be1b12.png)

所以有我们美丽的外框。是时候构建列表中的每个单独项目，可以使用以下CSS选择器进行寻址：

```css
nav ul li {}
```

因此，此代码查看 < nav>，< ul>，然后 < li>。似乎是关闭的是列表中的每个项目都需要自己的边框：

```css
nav ul li {
  border-bottom: 1px solid MediumVioletRed;
}
```

使用此代码，我们添加了一个 border-bottom，因此每个 < li>项目现在与文本底部的外边框具有相同的边框类型。

目前，我们的菜单应如下所示：

![menu-item-border.png](https://i.loli.net/2018/11/22/5bf6471bf2409.png)

我们现在有两个问题。第一个是边框和元素列表之间的左侧间距。让我们用我们的朋友 “填充” 来改变它：

```css
nav ul li {
  border-bottom: 1px solid MediumVioletRed;
  padding: 5px;
}
```

它好多了，对吧？我们在文本和边框之间添加了一个 5 像素宽的填充。

![menu-item-padding.png](https://i.loli.net/2018/11/22/5bf6471be244b.png)

我们的第二个问题不太明显，但仍然存在于菜单底部的双线。这是因为当我们添加“底部边框”时，我们的菜单边框代码会添加到最后一个项目的边框代码中。请记住，我们使用 < nav> 的 < ul> 中的代码 来指定边框：

```css
nav ul {
  background-color: PaleVioletRed;
  list-style: none;
  padding: 0;
  width: 200px;
  border: 1px solid MediumVioletRed;
}
```

还要记住，我们将列表样式设置为“无”，以便不显示项目符号或任何其他符号：

```css
list-style: none;
```

因此，通过将 “none” 设置为值，我们将禁用属性，以使其不具有任何图形效果。

让我们做同样的事情，只使用属性 “bottom-border” 并将值设置为 “none”。但是，我们希望仅定位菜单中的最后一项，以使其底部边框不与较大的底部边框冲突。

```css
nav ul li:last-child {
  border-bottom: none;
}
```

应用此代码的结果非常有效：

![menu-no-double-border.png](https://i.loli.net/2018/11/22/5bf6471c0d1fb.png)

双边界已经消失，因为我们查看 < nav> 的 < ul> 中的 “last-child” 属性，然后我们选择了最后一个 < li> 并关闭了底部边框。伪选择器是 “last-child”，表示列表中的最后一项。

```css
nav ul li:last-child {}
```

此选择器可以翻译如下：

“查看 < nav>，然后 < ul>，并将所有更改应用于 ”last“  < li> 元素。

我们需要做的最后一件事是调整链接中的文本。您可以在 HTML 中创建链接，如下所示：

```html
<a href="url">Text entered here will take you to the specified web address</a>
```

我们正在使用 < a> 标签以及属性 href。此属性的值应该是用户在单击链接时要移动到的地址。在我们的示例中，我们有四个链接。其中一个看起来像这样：

```html
<a href="training.html">Training</a>
```

这意味着浏览器将显示单词 “Training”，可单击该单词，然后将浏览器发送到已保存在 “training.html” 文件中的页面。

知道这个标签是HTML代码的一部分，我们可以创建一个特殊的 CSS 选择器，专门查找这个标签：

```css
nav ul li a {}
```

瞧！

让我们为新选择器添加新属性。首先，让我们将字体颜色更改为白色。

```css
nav ul li a {
  color: white;
}
```

刷新浏览器会显示我们的新更改：

![menu-white.png](https://i.loli.net/2018/11/22/5bf6474a01827.png)

大！我们现在有白色链接。现在让我们改变一些重点标记。浏览器设置为突出显示CSS中 “text-decoration：underline” 形式的所有链接。我们想要改变这个值，就像我们之前使用的值 “none” 一样。

```css
nav ul li a {
  color: white;
  text-decoration: none;
}
```

![menu-white-links.png](https://i.loli.net/2018/11/22/5bf6474a1f95f.png)

美丽！我们已经完成了我们想要的菜单。

作为旁注，如果您正在处理许多链接，您可能还记得在将鼠标悬停在链接上的许多页面上，文本会以某种方式被强调。

看看我在 Twitter 上发布的这个链接（没有下划线）：

![twitter.png](https://i.loli.net/2018/11/22/5bf6474ac961d.png)

当鼠标悬停在此链接上时，会发生一些有趣的事情，许多互联网用户都知道 - 文本会被强调，或者在这种情况下，下划线：

![twitter-hover.png](https://i.loli.net/2018/11/22/5bf6474b5553d.png)

让我们尝试在菜单中做类似的事情，只要我们将鼠标悬停在链接上，就可以突出显示或强调链接。我们将使用一个名为 “hover” 的伪选择器：

```css
nav ul li a:hover {
  text-decoration: underline;
}
```

这次我们将它添加到链接 < a>。这意味着当您将鼠标悬停在链接上时，将应用该效果。这适用于将鼠标悬停在其他元素上：

```css
div:hover
li:hover
img:hover
```

当我们将鼠标悬停在 “会议” 链接上时，效果如下所示。

![menu-hover.png](https://i.loli.net/2018/11/22/5bf6471bcc907.png)

总之，最终的 CSS 代码应如下所示：

```css
nav ul {
  background-color: PaleVioletRed;
  list-style: none;
  padding: 0;
  width: 200px;
  border: 1px solid MediumVioletRed;
}

nav ul li {
  border-bottom: 1px solid MediumVioletRed;
  padding: 5px;
}

nav ul li:last-child {
  border-bottom: 0;
}

nav ul li a {
  color: white;
  text-decoration: none;
}

nav ul li a:hover {
  text-decoration: underline;
}
```

新出现的伪选择器（last-child 和 hover）将来会很有用。

顺便说一句，在本章中，您已经学习了如何使用链接并将它们放入HTML文档中。此时，我们只使用了指向保存在您计算机上的本地文件（如 training.html）的地址，但是您也可以使用指向网络上的外部网站的链接，如下所示：

```html
<a href="https://wildgrass.top">My Blog</a>
```

浏览器中的上述代码将显示为[My Blog](https://wildgrass.top)。请注意，地址在最初的地方包含 “https：//”。通常，要了解您在 HTML 文档中使用的指向其他网站的每个链接都必须以 “https：//” 作为前缀。否则，您的链接不会将用户重定向到他们应该使用的位置。