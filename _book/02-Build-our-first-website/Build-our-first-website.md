# 让我们建立我们的第一个网站

>来源：[Let's build our first website](http://howtocodeinhtml.com/chapter2.html)

我们假设我们想要建立一个带有职位发布的网页。它应该看起来像这样：

![job-post-clean.png](https://i.loli.net/2018/11/14/5beb1933daa8f.png)

在创建任何类型的网页之前，最好根据重要性将内容划分为更小的组件。现在让我们尝试识别并突出显示此职位发布的每个元素，就像我们在 The Verge 的示例中所做的那样。

![annotated-job-post.png](https://i.loli.net/2018/11/14/5beb1933ab3e2.png)

简要分析将有助于我们更好地了解文本的哪些方面应该在职位发布中脱颖而出。红色表示标题文字。绿色表示伴随图像。而紫色标志着职位发布的两个段落（或“正文”）。

让我们回过头来看一下文字处理器和文本编辑程序的类比，其中网页可以在常规文本文档中创建。也许 Open，Notepad 或 Word 将包含公告的文本，然后另存为文本文件。它应该工作正常吗？

![job-post-textmate.png](https://i.loli.net/2018/11/14/5beb192f849d3.png)

如果在Web浏览器中进行检查，则会得到以下内容：

![job-post-browser.png](https://i.loli.net/2018/11/14/5beb192fe0899.png)

但是，这看起来不像我们设计的那样，是吗？它只是一大堆文字，不显示图片。现在怎么办？也许我们应该尝试在 Word 或 Photoshop 中创建这个帖子？我们并不想要这样做。我们在这里犯了错误，我们很快就会修复。关键问题是我们创建了一个只有纯文本的网站。

Web浏览器无法理解如何仅使用纯文本正确显示页面 - 它不知道文本的哪个部分应该是标题，哪个部分应该是图片。为了正确显示页面，我们需要通过文本功能定义每个元素，并将此信息传递给浏览器。我们已经部分完成了它。让我们做一些小的定义工作并使用正确的语法，以便浏览器也能理解它：

![job-post-functional-bricks.png](https://i.loli.net/2018/11/14/5beb1933e9f7e.png)

如您所见，文本中有特殊标记。我们稍后会谈到这些。现在，最好只是尝试从上到下完全按原样复制它们，就好像你正在逐块构建块一样。

您应该得到类似以下内容：

![job-post-code.png](https://i.loli.net/2018/11/14/5beb192f00884.png)

接下来，保存HTML文件。顺便说一下：我推荐[Sublime Text Editor](http://sublimetext.com/)，它是最好的代码编辑器之一。

![job-post-save.png](https://i.loli.net/2018/11/14/5beb192eb2b49.png)

现在让我们在 Web 浏览器中尝试新文件。

![job-post-html-browser.png](https://i.loli.net/2018/11/14/5beb1933bcaef.png)

它看起来好一点。现在，文本的每个部分的格式都不同，并且还会显示图片。这不是最终版本。缺乏色彩，粗体文字和风格尚不完全匹配。但在我们开始研究之前，让我们继续关注页面的结构。

首先，让我们比较发布的纯文本文档版本和HTML中显示的版本：

![job-post-code-comparison.png](https://i.loli.net/2018/11/14/5beb192f6998a.png)

由于周围特定文本片段带有特殊标签，我们创建了一个完全不同的文档，浏览器可以理解。路要走！

这称为HTML或超文本标记语言，是用于显示Web浏览器信息的主要标记语言。简单来说，它是一种使用“标签”（如 ` <this>` ）来标记文本的语言，以便您可以向浏览器描述文本。这还包括搜索引擎和我们稍后将介绍的一些其他程序。HTML标签就像语言交流中的语法形式，没有它们，你就无法建立一个连贯的网站，就像你无法形成没有语法的正确句子或段落一样。

在我们的例子中，我们只使用了几个简单的标签，下面是每个标签执行的功能列表：

```html
<h1> - 标题（第一学位）
<img> - 图片元素
<p> - 一段文字
```

因此，如果您的网站包含几段文字，则使用 `<p>` 标记围绕每个段落。如果文本是主标题，则用 `<h1>` 包围文本，依此类推。

所有标记结构都非常简单，如下所示：

```html
<tagname>content</tagname>
```

您可能已经注意到第二个标记不同。这是因为每个标签都必须“关闭”，正如 HTML 行话所说的那样。正斜杠出现在结束标记中，告诉浏览器这标志着元素的结束。例如，所有段落元素都以 `</ p>` 结尾，而页眉1以 `</ h1>` 结尾。

还有一些标签不需要封闭。例如，图像标签 `<img>` ，用于插入图片。在上面的示例中，我们使用如下：

```html
<img src="images/white-cat.jpg">
```

还有几个标签不需要“关闭”，您将在本书的后面部分了解这些标签。

关于HTML标签的一个重要实现是，就像字典包含语言的词汇一样，HTML 也有一种定义标签的字典，并描述了何时何地使用它们。目前我们只覆盖了几个，但还有更多。被称为万维网联盟（ W3C ）的国际组织鼓励在整个网络上采用最佳实践，标准和兼容性。您可以在此处查看 HTML 元素的定义：[http//www.w3.org/TR/html-markup/elements.html](http://www.w3.org/TR/html-markup/elements.html)。

此外，有必要记住，与自然语言一样，HTML 随着时间的推移而发展。今天，我们使用第五版 HTML 语言，即 HTML5。

回到我们的示例，它应该在 HTML 代码中如下所示：

```html
<h1>We're looking for an HTML and CSS developer</h1>

<img src="images/white-cat.jpg">

<p>For our client, The Cat Factory, we need a skilled web developer in HTML and CSS. We offer a competitive salary, a bag of cat food, and toys.</p>

<p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
```

请注意，它包含两段文本，标记在 `<p> </ p>` 标记内：

```html
<p>For our client, The Cat Factory, we need a skilled web developer in HTML and CSS. We offer a competitive salary, a bag of cat food, and toys.</p>

<p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
```

假设我们希望广告的读者特别注意段落中的某个部分。假设我们想要标记“我们需要一个熟练的 HTML 和 CSS 开发人员”的文本部分。 HTML 标签如何让浏览器知道？答案是 `<strong>`  
元素，它将围绕应该代表其内容非常重要的文本部分。

```html
<p>For our client, The Cat Factory, <strong>we need a skilled web developer 
in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food,
and toys.</p>

<p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
```

请注意，`<strong>` 标记围绕文本，也位于 `<p>` 标记内。在编程术语中，我们会说 `<strong>` 标记是 `<p>` 中的“子”元素，因为它嵌套在父元素中。有许多标签可以嵌套在其他标签中，而其他标签则不能。每个标记都有一个可能包含（或包含）的可能HTML元素的特定列表，您需要检查是否允许某个标记。您可以将其视为较小的块组合以构成更大的块（在这种情况下，`<strong>` 块是 `<p>` 的一个组件，而这又是整个文本的一个块。

这是它在网络上的样子。

![job-post-strong-browser.png](https://i.loli.net/2018/11/14/5beb192e651db.png)

请注意，我们上面使用的Web浏览器以粗体显示片段，但这并不总是一个规则。 `<strong>` 使文本变粗，这很常见，但有时会被忽略。在本文中使用此HTML标记的原因是嵌套如何工作的一个很好的例子，但是通过一种称为 CSS 的语言可以更好地实现视觉效果（如粗体），我们将在稍后了解更多信息。
