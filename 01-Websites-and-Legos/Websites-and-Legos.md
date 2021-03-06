# 网站和乐高积木

> 来源：[网站和乐高积木](http://howtocodeinhtml.com/chapter1.html)

我真的很喜欢[The Verge](http://www.theverge.com/)。这是一个网站，您可以在其中找到有关新技术，科学和文化的有趣文章。在主页上，您可以找到许多相似的故事和文章。它们具有标题，类别，日期和图像条目。它几乎看起来像是用砖砌成的。

让我们来看看其中一个：

![theverge-article.png](https://i.loli.net/2018/11/14/5beb17341a78d.png)

乍一看，没有什么复杂的。让我们有一些乐趣并突出（或阻止）每个元素，就像我们处理乐高部分一样。

![article-theverge-bricks.png](https://i.loli.net/2018/11/14/5beb17370e0b2.png)

总共，我们有五件，一件排在另一件之上。

你可能还记得从童年开始，为了构建特定的东西，你需要很多不同的块来对不同的东西有用。他们每个人都有一定的功能。例如，在建造房屋时，一种类型对墙壁有用，另一种对地板更有用。没有单一的通用块或元素可以让您想到任何想法。见下图？这是多种乐高选择的选择，对吧？

![lego-bricks.jpg](https://i.loli.net/2018/11/14/5beb1732caec6.jpg)

网站也是如此。构建网站时，根据其理想目的地使用不同的元素。在Verge示例中，似乎我们正在处理各种对象（或块），因此对每个块应用相同的颜色或样式这样做会违反直觉。毕竟，标题与日期或段落的内容不同。它们各自执行完全不同的功能。

为了继续，我们需要通过他们在网站上执行的功能来识别文章的元素。让我们通过为每个“块”添加一种独特的颜色来做到这一点。

![article-theverge-functional-bricks.png](https://i.loli.net/2018/11/14/5beb17343c04e.png)

这更有趣。我们现在有几种不同类型的“构建块”。只有两个块是相同类型的，特别是图片下方的两个段。这与组织乐高没什么不同。我们将把属于同一组的类似文本片段放在一起。作为一种形式，我们将根据文章上下文中的功能命名每个部分。

![article-theverge-functional-brickswithlabels.png](https://i.loli.net/2018/11/14/5beb173874694.png)

所以我们根据它们的语义来标记每个元素。这正是我们可以期望从Web浏览器中看到的那种行为和逻辑。我们的工作是以一种可以理解的方式告诉浏览器，这些元素的含义以及它们在语义上如何组合在一起。如果没有这样做，那么我们的网站将显示为单个文本的丛集。

您可能使用Microsoft Word或Pages等文本编辑器程序创建了此类页面或文章。在文本编辑器中，实现“标题样式”等效果只需单击几个按钮即可。换句话说，当我们在单词编辑器中选择文本并按“标题1”时，我们在后台分配了一堆不同的功能，告诉编辑器以特定的方式显示内容。

因此，如果我们想在文字处理器中重新创建一个类似上面例子的页面，那将简单易行，此时你可能会关闭这本书并去做其他事情（Breaking Bad将是一个不错的选择）。问题是我们希望在Web上显示这篇文章，这篇文章必须在浏览器中显示，而不是在文本编辑程序中。

