# HTML练习：编写一个Blogpost

>来源：[HTML Exercise: Coding a Blogpost](http://howtocodeinhtml.com/chapter4.html)

是时候进行另一项练习，向您展示在 HTML5 中编写更高级网站的理念。我们将尝试将以下示例生成为网站，博客上的文章。

![blogpost-preview.png](https://i.loli.net/2018/11/14/5beb1c063cc35.png)

请注意，这里我们有一篇文章标题。此外，还有关于作者的信息，以及照片和“引用”段落。值得注意的是，作为一名前端 Web 开发人员，您经常会收到图形设计（如上所示），并且必须以 HTML 格式重新创建所有内容。

让我们从始终固定且不变的元素开始。正如我们之前所做的那样，我们需要doctype标签，< html >，< head > 和 < body >。请注意，在我们的 < head > 中，我们要确保我们对“ utf-8 ”进行字符编码，以便我们可以在我们的网站上显示特殊字符。

我们的代码起始模板如下所示：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8"> 
  </head>
  <body>
  </body>
</html>
```

我们现在添加标题：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Justin Beaver fascinated by HTML</title>
  </head>
  <body>
  </body>
</html>
```

此时，我们已经完成了模板，该模板现在将作为文章内容的基础。

如果我们将文件保存为 article.html，然后在浏览器中打开，我们将看不到任何内容，因为 < body > 标记没有内容。

我们通常从最一般的内容开始，随后是随着我们的进展更具体，更详细的内容。让我们分析一下我们的作品：

1. 在文章中，最重要的信息可能是包含标题的标题信息：“ JJustin Beaver: Ever since I learned HTML, my life has made a complete 180. ”
2. 下一个最重要的信息是作者，“ authored by Damian Wielgosik. ”。
3. 接下来是第一段文字，然后是照片及其描述的地方。
4. 最后，最后一段，其中包含一句话，“ I will probably have a song about HTML on my next album ”。

那些是我们的作品。我们在这些分析中查看这些分析有助于我们可视化 HTML 代码的外观。层次结构从最常规元素（父元素）开始，然后继续到父元素包含的元素（子元素），这些元素是更具体的详细元素。

有了对层次结构的理解，我们的信息应该在 HTML 代码中按如下方式组织：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Justin Beaver fascinated by HTML</title>
  </head>
  <body>
    <article>
    </article>
  </body>
</html>
```

您可能已经注意到我们使用了 < body > 父元素中包含的 < article > 元素。文章由标题和内容组成，因此表示标题和段落的所有标记自然都是 < article > 的子标记。

添加到目前为止我们发现的元素列表中，我们现在将使用标记标题的元素 < header > 标记。

我们可以将 < header > 代码添加为 < article > 的子代。当我们在代码中从上到下移动时（在重要性方面），请注意我们还向右移动缩进以显示元素在层次结构上比其上面的组件更低。在下面的示例中，< header >不仅位于< article >下方，还缩进以显示它在层次结构中的位置。

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
      </header>
    </article>
  </body>
</html>
```

我们的标题部分现已准备就绪，但 < header > 中应该包含哪些内容？ 好吧，我们之前讨论过我们有一个标题和作者。我们将使用标记 < h1 > 作为文本标题，并使用 < p > 作为作者。作者没有特定的HTML标记，因此在这种情况下，我们使用 < p > 作为文本的通用容器。

在下面的代码中，我们在 header 元素中添加了 < h1 >  和  < p > 标记：

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
    </article>
  </body>
</html>
```

顺便说一句，你应该注意到除了 < h1 > 之外，还有较低级别的 HTML 标题，如下所示：

- < H2 >
- < H3 >
- < H4 >
- < H5 >
- < H6 >

这些元素有助于映射标题和副标题的逻辑结构。因此，例如，如果我们以书籍格式书写，其标题将包含在元素 < h1 > 之间。然后，章节的名称将用 < h2 > 和子部分 < h3 > 标记。

请注意，您不应该简单地将标题表示为 < h4 > 。标头必须嵌套在更高优先级的标头下，因此如果您有 < h4 >，< h3 > 必须在它之前发生，并且 < h2 > 必须在此之前发生，依此类推。

例如，这本书看起来像这样：

```html
<h1>Simple HTML5</h1>
<h2>My first website</h2>
<h3>W3C Validator</h3>
<h2>Meet CSS</h2>
<h3>Selectors in CSS</h3>
```

让我们继续编写第一段文字。我们希望避免在 < header > 下嵌套段落。该段落应该是 < article > 的一部分是有道理的。因此，我们将在 < article > 中添加第一个 < p >，其优先级与 < header > 相同，但在其下方：

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
    </article>
  </body>
</html>
```

接下来我们将添加照片和说明。对于这种类型的内容，因此所有内容都与整个文档相关，如照片，图表或地图，我们将使用 < figure > 标签。值得注意的是， < figure > 使用条件很重要，因为你可以使用额外的元素 < figcaption >，它将图像的描述放在它下面。

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
    </article>
  </body>
</html>
```

在我们添加了图片之后，我们还有一个段落要添加到文章中。请注意，这一段引用了一句话，“我的下一张专辑中可能会有一首关于HTML的歌曲。” 我们可以对此引用进行注释，以便我们的代码具有更大的语义值。也许在将来，有人会寻找Justin Beaver的引用，这个名称将帮助他们更快地找到报价。否则，搜索引擎总是要处理一大块文本。

为了表明文本的一部分是引用，我们将在新段落中使用 < q > 标记：

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
      <p>Beaver has already created some websites and does not intend to stop there. 
      <q>I will probably have a song about HTML on my next album,</q> - the artist added.
      </p>
    </article>
  </body>
</html>
```

现在，让我们将代码保存到扩展名为 .html 的文件中，并将其显示在浏览器中。

您现在已经完成了第二页。大！这是成为专业 Web 开发人员的又一步。