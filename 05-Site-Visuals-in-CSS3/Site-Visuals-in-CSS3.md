# CSS3 中的网站视觉效果

>来源：[Site Visuals in CSS3](http://howtocodeinhtml.com/chapter5.html)

您可能已经注意到，除了我们的图像，我们的网站看起来不是很有趣。在白色背景上的黑色文字不是非常欢迎我们的访客。让我们用 CSS（层叠样式表）来研究我们网站的外观。使用这种语言，我们可以操纵网站的特征，如颜色，字体大小和许多其他品质。CSS 提供了大量可能的可能性。

在前面的部分中，我们使用 HTML 来描述站点的内容，并根据它们的重要性将其划分为片段。CSS 将负责我们网站的外观。CSS 代码可以放在扩展名为.css的单独文件中，并通过特殊的HTML标记插入。您也可以将其直接放入 HTML 文档中。

想象一下，在这个抽象的例子中，我们想用 CSS 代码构建一个房子，在那里我们选择诸如窗户，门，屋顶，墙壁，排水沟等物品。我们想要购买特定尺寸的窗户，并为每个必要部件涂漆。如果我们在 CSS 中构建这个房子，这个任务的许多解决方案之一可能如下所示：

```css
roof {
  background-color: green;
}

doors {
  background-color: yellow;
  width: 100px;
  height: 300px;
}

windows {
  border: 5px solid brown;
  width: 150px;
}
```

让我们从上到下分析这段代码的“屋顶”块（注意，在阅读所有类型的代码时，从上到下阅读是一个规则，而不仅仅是 HTM L和 CSS ）。

```css
roof {
  background-color: green;
}
```

如果我们将上面的代码翻译成普通英语，我们选择了一个名为“roof”的元素，并将背景颜色设置为绿色。

```css
windows {
  border: 5px solid brown;
  width: 150px;
}
```

上面的代码说，“对于所有窗口，设置以下内容：宽度为 5 像素（5px）的框架（边框），用连续线（实线）颜色（棕色）标记。此外，窗口本身应该有一个（宽度）为 150 像素（150 像素）。

您可能已经注意到代码中出现了重复出现的模式。在第一行，我们编写元素的名称（称为“选择器”），然后在括号之间定义该元素的外观。

模板的基本结构如下所示：

```css
selector {
  property_name: property:value;
}
```

这种类型的构造是典型的 CSS 规则。该规则包含一个选择器（第一个括号之前的所有内容），后跟一个在括号之间写入的属性列表。

有多种方法可以准确指定我们想要设计的内容。假设我们只想在底层指定窗户的设计。然后怎样呢？我们可以这样写：

```css
ground floor window {
  border: 5px solid brown;
  width: 150px;
}
```

结果是只有选择器发生了变化。而不是“窗口{”我们指定了“底层窗口{”

此代码从左到右读取，如“找到底层，然后找到它的窗口并设置以下值”。如果我们在“底层窗户”下放置一个子选择器，如：

```css
adjacent wall windows {
```

然后我们告诉浏览器：“找到底层窗口，窗口旁边的窗口，并用以下值填充它们”，依此类推。如果你还记得我们讨论过嵌套HTML标签作为子节点和父节点的类比，那么这就是相同的概念，这些元素嵌套在其他元素中。

不幸的是，浏览器无法构建一个房子，但我们的示例告诉我们CSS的工作原理。这个比喻很有用，因为在编码时，我们并不总是能够看到变化。但我们可以将段落（< p >）视为窗口，将门视为标题（< h1 >）等。

它看起来像这样：

```css
p {
}

h1 {
}
```

让我们将我们在这个类比中学到的东西应用到我们的例子中，并使用相同的想法为 Justin Beaver 文章添加一些颜色和生命。

回想一下，我们的代码如下所示：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Justin Beaver fascinated by HTML</title>
  </head>
  <body>
    <article>
      <header>
        <h1>Justin Beaver: Ever since I learned HTML, my life has made a complete 180</h1>
        <p>Posted by: Damian Wielgosik</p>
      </header>
      <p>Justin Beaver confessed something that even his greatest fans would have never expected of the skilled musicians and lyricist. The young rock-and-roller admitted that since he typed his first title tag, his life became easier. It has been reported by those surrounding the Canadian that Beaver's private mentors, Ryan Loseling and Nicolas Crate, often walk around Los Angeles disputing what a great tool the HTML validator is.</p>
      <figure>
        <img src="cat.jpg" alt="Justin Beaver's cat is pleased">
        <figcaption>Justin Beaver's happy cat</figcaption>
      </figure>
      <p>Beaver has already created some websites and does not intend to stop there. <q>I will probably have a song about HTML on my next album,</q> - the artist added.
      </p>
    </article>
  </body>
</html>
```

回想一下建房子的类比。我们不是建造门，窗等，而是处理< article >，< p >，< header >，< body >，< figcaption >等元素。这些标签构建了页面，现在CSS将有助于为它们提供样式。

我已在下一页准备了截图，以便您了解我们的修改将如何更改生成的网站。

![article-final-proposition.png](https://i.loli.net/2018/11/18/5bf0745033f84.png)

如你所见，情况发生了很大变化。我们添加了简单的颜色，背景，改变了字体样式等等。让我们一步一步地完成如何在上面的图像中完成效果。

第一步是将整个 HTML 代码保存到单独的文件中。对我而言，它被称为 article.html。然后创建一个单独的文件，我们保留 CSS 规则。让它成为main.css。

我的计算机上的文件如下所示：

![article-file-system.png](https://i.loli.net/2018/11/18/5bf07447b2981.png)

我们现在可以尝试在浏览器中打开 article.html，使用文本编辑器打开 main.css 文件。我推荐[Sublime Text Editor](http://sublimetext.com/)或[TextMate](http://macromates.com/)。在 main.css 中进行每次更改后，我们可以刷新浏览器页面以更新其外观。

我们现在需要在浏览器中打开 article.html，并从 main.css 文件加载代码。这是通过 HTML 代码中 < head > 中的标记  < link > 完成的。只需在头部添加这样的标签：

```html
<link rel="stylesheet" href="main.css">
```

“href” 属性指示文件的位置。“样式表”告诉我们它是一个CSS样式表。

好的，要开始在 CSS 中更改视觉外观，让我们尝试为标题找到正确的选择器，类似于窗口和墙壁的代码。

```css
h1 { 
}
```

我们到了！在这里，我们可以告诉浏览器“对于 < h1 > 中的所有元素，应用以下外观。” 请注意，大括号目前是空的。让我们试着告诉它我们希望标题文本是绿色的。我们将应用属性 “color” 并将其设置为 “green”。

```css
h1 {
  color: green; 
}
```

此规则的操作在下图中说明：

![selector-explanation.png](https://i.loli.net/2018/11/18/5bf074474e81e.png)

让我们来看看我们的页面如何看待变化！

![article-green-header.png](https://i.loli.net/2018/11/18/5bf075ee5d965.png)

是! 标题以绿色表示。 

现在我们想要了解有关作者的信息的下一部分。假设我们希望文本为白色，背景为红色，如前几页所示。这是当前的 HTML 代码：

```markup
<article>
  <header>
    <h1>Justin Beaver: Ever since I learned HTML, my life has made a complete 180.</h1>
    <p>Posted by: Damian Wielgosik</p>
  </header>
```

让我们使用CSS，找到合适的选择器（“ p { ”）并尝试给它一个背景红色和一个白色文本：

```css
p {
    background-color: red;
    color: white;
}
```

我们的main.css代码目前应如下所示：

```css
h1 {
  color: green; 
}

p {
    background-color: red;
    color: white;
}
```

如您所见，我们在另一个下添加规则。是时候看看我们的网站现在看起来如何......

![article-red-paras.png](https://i.loli.net/2018/11/18/5bf0744782cc1.png)

糟糕，这不太对劲。似乎所有其他段落也已更改为具有新的背景和文本颜色。这是我们代码的问题，因为我们使用了以下内容：

```css
p {
    background-color: red;
    color: white;
}
```

我们实际告诉浏览器的是“找到 ** 所有 ** < p > 元素并应用更改。” 但是，我们只想更改文章标题行中的段落。

我们现在需要修改代码，使上述选择器只适用于 < P > 在 < title >，这是一个对的“孩子”  < article >。代码应该反映这种层次结构：

```css
article header p {
    background-color: red;
    color: white;
}
```

让我们看看这些变化的影响。

![article-better-selector.png](https://i.loli.net/2018/11/18/5bf07446ac471.png)

好多了！看来我们能够定位正确的段落。但是这是怎么发生的？好吧，我们使用上面的代码告诉浏览器知道 CSS 选择器应该定位哪些标签。我们通过检查HTML代码并找到应该与选择器匹配的所有标记来完成此操作。在我们的例子中，我们有 < article >，< heade r>和 < p >的嵌套标签，因此CSS 选择器 “article header p” 让我们确切地指定应用更改的位置。

让我们继续阅读文章中的图像。

比方说，本文的尺寸应为600像素宽。请记住，我们对应的图像HTML标签是< figure >。让我们指定我们的 CSS 代码来反映这一点：

```css
article figure  {
    width: 600px;
}
```

使用此代码，< article > 标记中的每个 < figure > 都将具有 600 像素的宽度。请注意，如果我们在博客文章中有多个图像并希望为每个图像指定不同的标准，那么“文章”区别将会有所帮助。但由于我们只有一个图像，让我们转到边界代码：

```css
article figure  {
    width: 600px;
    border: 3px solid black;
}
```

在这里，我们添加了一个名为 “border” 的属性。冒号后，我们指定边框的宽度（3 个像素），边框的样式为 “solid”，颜色为 “black”。

让我们看看它的样子：

![article-border-overflow.png](https://i.loli.net/2018/11/18/5bf07450c8ec3.png)

看起来我们遇到了问题。当边框以正确的样式和颜色显示时，图像显示超出600像素。这是因为我们建立了元素 < figure > 的宽度，但 < img > 标签没有任何固定宽度，因此保持其原始大小。如果图像占据其父 < figure >宽度的100％，那将是很好的。编码非常简单：

```css
article figure img {
    width: 100%;
}
```

它现在看起来像这样：

![article-good-border.png](https://i.loli.net/2018/11/18/5bf0744e9d1ff.png)

在边框和图像之间添加一些“填充”或空格会很不错。我们通过添加属性“padding”来做到这一点。我们可以修改代码如下：

```css
article figure  {
    width: 600px;
    border: 3px solid black;
    padding: 5px;
}
```

结果：

![article-border-padding.png](https://i.loli.net/2018/11/18/5bf0744d726b9.png)

您可以尝试自己修改“填充”的值，并查看图片和边框之间的白色间隙如何变化。

我们的页面现在看起来不错，但我们尚未完成。当前段落文本几乎扩展了浏览器窗口的整个宽度，这是不可读的。也许以某种方式减少文本的宽度是合适的？也许将它限制在 800 像素？

让我们为此选择一个特殊的CSS选择器：

```css
article {
    width: 800px;
}
```

那更好。

那么字体怎么样？如果您查看我们网站的原始图像，我们的字体略有不同。就像您可以在 Microsoft Word 中编辑字体样式一样，您也可以在 CSS 中编辑它们。要指定字体，您需要将此属性添加到最高标记，以便它适用于该标记内的所有文本。例如，我们将设置字体作为属性的 < body > ，以使下面的每一个元素的 < body > 将具有此设置。在图片中，我使用了一种名为 Verdana 的字体。

让我们尝试应用它：

```css
body {
    font-family: Verdana;
}
```

您可以通过删除此行或将 font-family 更改为其他样式来查看差异。对于标题，段落等，浏览器将显示 Verdana 中的所有内容。

最后，我们在main.css文件中的代码应如下所示：

```css
body {
    font-family: Verdana;
}

article {
    width: 800px;
}

article header h1 {
    color: green;
}

article header p {
    background-color: red;
    color: white;
}

article figure  {
    width: 600px;
    border: 3px solid black;
    padding: 5px;
}

article figure img {
    width: 100%;
}
```

通常，使用最常用的选择器启动代码并进入更复杂的选择器是一种很好的做法。我从身体开始，然后是文章，依此类推，从上到下。细节越高，它在列表中的位置就越低。

