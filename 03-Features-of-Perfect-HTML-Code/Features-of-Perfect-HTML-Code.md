# 完美HTML代码的功能

>来源：[Features of Perfect HTML Code](http://howtocodeinhtml.com/chapter3.html)

此时我们已经建立了我们的第一个网站。不幸的是，根据目前良好网页的标准，我们尚未完成。正如工程师遵守严格的设计准则，或者餐馆有健康和安全法规一样，Web 开发人员也有一套最重要的规则来定义完成的工作。

让我们从目前为止的代码开始，包含我们所学到的所有元素：

```html
<h1>We're looking for an HTML and CSS developer.</h1>
<img src="images/white-cat.jpg">
<p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
<p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
```

在任何自尊的 HTML 页面的最顶端，应该有文档类型的指示。这是 doctype：

```html
<!DOCTYPE html>
<h1>We're looking for an HTML and CSS developer.</h1>
<img src="images/white-cat.jpg">
<p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
<p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
```

上面突出显示的部分“告诉”浏览器该页面是 HTML 文档，并且应该根据已建立的语言标准来处理页面的代码。这会向浏览器通知几条规则，这些规则将指导我们如何查看我们的网站。除此之外，它还有助于浏览器知道允许或不允许哪些标签。它有助于浏览器更好地解释我们的代码。

在 doctype 下面，我们要放置标记 < html>：

```html
<!DOCTYPE html>
<html>
  <h1>We're looking for an HTML and CSS developer.</h1>
  <img src="images/white-cat.jpg">
  <p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
  <p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
</html>
```

请注意，此标记需要关闭，因此我们希望确保在结尾处添加 < /html> ：

```html
<!DOCTYPE html>
<html>
  code
</html>
```

因此，属于我们网站的所有内容都包含在 < html> 标记下。在编写 HTML 时，只有通过 < /html> 包含代码才有意义。

但是，< html> 标签尚未完成。我们想要添加有关我们网站语言的更多信息。由于这是一个英文示例，我们将其指定为：

```html
<!DOCTYPE html>
<html lang="en">
  <h1>We're looking for an HTML and CSS developer.</h1>
  <img src="images/white-cat.jpg">
  <p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
  <p>Don't wait, apply now! Our crazy team is waiting for you right  meow!</p>
</html>
```

请注意突出显示的部分已修改 < html> 标记。这被称为“属性”。属性是 HTML 中的修饰符，始终写在 < > 附件之间的标记旁边。编写代码时，属性具有以下模板。

```html
tag attribute="value"
```

随着 HTML 开发人员的成长，他/她将遇到许多不同的属性。除了 "lang" 之外，还有很多种。这里只是几个例子。

- < div id =“sidebar”> < /div> - 属性名称为“id”，值为“sidebar”
- < p class =“landscape”> < /p> - 属性名称为“class”，值为“landscape”
- < input type =“text”> - 属性名称为“type”，值为“text”

我们使用属性，因为在许多 HTML 标记（例如 < html> ）中不包含所有必要的信息。使用属性，我们可以修改我们使用的标签，并为它们添加更多有用的信息。在这种情况下，我们让浏览器知道我们的 HTML 文档是用英语编写的，所以我们用属性 "lang" 修改了 < html> 标签，并给它一个 "en" （英语）的值。

多个属性甚至可以出现在单个标记中。这里有一些例子：

```html
<input type="text" value="enter text here">
<a href="http://functionite.com" title="We Train Developers">HTML Training</a>
```

值得注意的是，属性也是 HTML 标准的一部分，就像嵌套标记一样，这些属性的列表以及它们可以修改的标记可以在网上找到。

事实上，我们在第一次构建网页时已经使用过属性！还记得图片代码吗？您将其放在 HTML 文档中，其中包含以下行：

```html
<img src="images/white-cat.jpg">
```

在这种情况下，< img> 标签使用属性 src 修改，其值为 images/white-cat.jpg 。

标签本身只是 < img> ，所以如果我们只是将它单独留下，浏览器将无法检索要显示的信息源。当我们定义 'src" 时，我们告诉浏览器“嘿，从这个来源加载信息”。然后浏览器知道应该查找文件夹 "images" 和文件 "white-cat.jpg"。我们还可以传递链接到网络上的任何资源（如果它不受限制），例如[http://4.bp.blogspot.com/-z4sMggeD4dg/UO2TB9INuFI/AAAAAAAAdwc/Kg5dqlKKHrQ/s1600/funny-cat-pictures-032-025.jpg](http://4.bp.blogspot.com/-z4sMggeD4dg/UO2TB9INuFI/AAAAAAAAdwc/Kg5dqlKKHrQ/s1600/funny-cat-pictures-032-025.jpg)。

这是属性如何工作的要点。由于属性，我们可以添加有助于 HTML标记的丰富有价值的信息。

现在让我们回到我们的文档并添加更多必要的组件。我们将查看标记 < head>，其中包含对页面内容不一定有用的元素，但对于搜索引擎，浏览器选项卡等非常重要。例如，网页上的标题可以帮助搜索引擎找到您的内容。

```html
<!DOCTYPE html>
<html lang="en">
  <head>
  </head>
  <h1>We're looking for an HTML and CSS developer.</h1>
  <img src="images/white-cat.jpg">
  <p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
  <p>Don't wait, apply now! Our crazy team is waiting for you right  meow!</p>
</html>
```

目前，我们的 head 标签是空的，但通常这是您要放置所有元信息的位置，例如整个文档的标题。当我们用我们的工作机会创建页面时，假设我们决定标题为“工作机会：HTML 和 CSS 开发人员”。让我们继续添加吧！

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Job Offer: HTML and CSS Developer</title>
  </head>
  <h1>We're looking for an HTML and CSS developer.</h1>
  <img src="images/white-cat.jpg">
  <p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
  <p>Don't wait, apply now! Our crazy team is waiting for you right  meow!</p>
</html>
```

您可能已经注意到，我们在标签 < title> 之间添加了标题。有什么区别，为什么我们这样做呢？下图说明了我们没有 < title> 标签（左）和我们的页面有 < title> 标签（右）的情况。使用标题，我们的网站更适用于浏览器用户，并且在许多标签之间导航更容易。

![img](http://howtocodeinhtml.com/img/chapter3/job-post-title-comparison.png)

另一个例子可能是我的公司网站。我使用“功能 - JavaScript 研讨会团队”作为标题内的文本标签。因此，它在 Google 搜索结果中显示为：

![img](http://howtocodeinhtml.com/img/chapter3/functionite-title-google.png)

如您所见，在对网站进行编码时，这一点非常重要。没有它，该网站将没有名称，这将给访问者留下不好的印象。就个人而言，我不相信一个甚至没有标题的页面。

添加头后我们还需要做一件事，那就是添加 < body> 标签。这将整个页面的内容与头部分开。您网页上显示的所有内容都将放在 < body> 中。

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Job Offer: HTML and CSS Developer</title>
  </head>
  <body>
    <h1>We're looking for an HTML and CSS developer.</h1>
    <img src="images/white-cat.jpg">
    <p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
    <p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
  </body>
</html>
```

万岁！看起来我们努力的结束似乎一切都是正确的。作为新手编码器，检查一切是否正常（例如嵌套标签，良好属性等）可能是个好主意。但并不是每个人都有高级 HTML 开发人员的朋友，他们可能会被要求咨询。幸运的是，我们可以使用一种特殊的工具来检查我们的代码是否正确。 W3C 组织，即定义标准并维护 HTML 文档最佳实践的同一组织，已经成为检查代码的工具。该工具简称为 HTML 验证器，可在[http://validator.w3.org上找到](http://validator.w3.org/)。

该页面应如下所示：

![img](http://howtocodeinhtml.com/img/chapter3/w3c-validator.png)

让我们使用该工具并检查我们的代码是否正确。

![img](http://howtocodeinhtml.com/img/chapter3/w3c-validator-error.png)

... Woops！我们有一个错误和3个警告。我们来看看它们。

验证器报告的单个错误与我们的图像有关。我们来看看错误的内容：

> img 元素必须具有 alt 属性，但在某些条件下除外。有关详细信息，请参阅有关为图像提供替代文本的指导

事实证明，文档中的 < img> 标记必须始终具有 "alt" 属性，以便在浏览器无法加载图像时使用该属性。然后它将显示此备用属性的值（它比空格更好，对吧？）。

在我们选择属性 "alt" 的值之前，让我们看看 HTML 规范，以确保我们正确地执行此操作：

这是我们可以查看它的页面：[W3C](http://www.w3.org/wiki/HTML/Elements/img)：

> 提供图像的后备内容。alt 属性值的要求将在下一节中介绍。

然后，它进一步区分了几种情况，以及何时以及如何使用 alt 属性。在我们的例子中，我们正在处理一个用于装饰帖子的图像，并且不包含任何内容，情节或其他信息给读者。在这种情况下，我们应该将备用属性留空，说明规范：

> 然而，可以使用 img 元素在页面中包括未被周围文本讨论但仍具有一些相关性的装饰图像。这些图像是装饰性的，但仍然是内容的一部分。在这些情况下，alt 属性必须存在，但其值必须为空字符串。

在其他情况下，我们希望选择可能替换图片上的内容的文本字符串。有关几个杰出案例的详细指南可以在 < img> 标签的规范中找到：[http://www.w3.org/wiki/HTML/Elements/img](http://www.w3.org/wiki/HTML/Elements/img)。

好的，所以我们知道我们希望将 "alt" 属性设置为空。

我们加上吧......

```html
<img src="images/white-cat.jpg" alt="">
```

...然后再次针对验证器检查我们的文档。

![img](http://howtocodeinhtml.com/img/chapter3/w3c-validator-valid.png)

它通过没有错误！

但我们仍然有3个警告。其中最重要的如下：

> 在HTML元元素或 XML 声明中，未在文档中找到字符编码信息。通常建议在文档中声明字符编码，特别是如果有可能从磁盘，CD 等读取或保存文档。

但不要担心，这是一个简单的警告。在我们尝试理解它之前，让我们检查以下示例，这将使我们能够更好地理解该问题。

重要的是要意识到您的网站可能会被来自西班牙，中国或瑞典等不同国家的人们访问，更不用说其他人了。如果您允许，他们可以留下您的文章旁边可能会显示的评论或消息。值得注意的是，不同国家使用不同的语言并使用自己的变音符号。在瑞典语中它可以是 ä 或 ö，而中文为您提供一系列的汉语拼音方案。在全球网络中，让不同语言在同一页面上正确显示至关重要。如果我们在帖子中使用中文，我们来看看会发生什么：

```html
<p>PS 再见</p>
```

让我们在浏览器中检查效果：

![img](http://howtocodeinhtml.com/img/chapter3/utf-problem.png)

请注意最后一行，而不是一个正确的中文句子，我们可以看到一些在任何现代语言中根本没有意义的奇怪标志。不要惊慌，它与我们在 HTML 验证器中收到的警告有关。事实证明，我们没有插入特殊的行，这将允许其他语言正确显示。在计算机世界中，它被称为[字符编码](http://en.wikipedia.org/wiki/Character_encoding)。如果我们将此信息传递给 HTML 页面，它将“告诉”浏览器它已准备好显示各种字符，包括所有不同的变音标记。

我们开工吧！

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Job Offer: HTML and CSS Developer</title>
    <meta charset="utf-8"> 
  </head>
  <body>
    <h1>We're looking for an HTML and CSS developer.</h1>
    <img src="images/white-cat.jpg">
    <p>For our client, The Cat Factory, <strong>we need a skilled web developer in HTML and CSS</strong>. We offer a competitive salary, a bag of cat food, and toys.</p>
    <p>Don't wait, apply now! Our crazy team is waiting for you right meow!</p>
  </body>
</html>
```

这次我们不得不使用带有属性 charset 的特殊标签 < meta >，并为其赋予“utf-8”的值。 utf-8  是指一种特殊的字符集，它包含来自世界上大多数语言的字符集，如果不是全部的话。

就是这样！你刚刚建立了你的第一个网站！恭喜！