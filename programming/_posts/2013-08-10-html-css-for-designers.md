---
title: 设计师应该知道的 HTML 和 CSS
layout: post
---

想写这个很久了，我总觉的我的设计师同仁们需要知道一些 HTML 与 CSS，这样大家彼此沟通起来隔阂少些，
最起码诸位设计师同僚们可以知道，当前端工程师谈论填充、边框与边距时都在谈论什么。幸运的是，许多
设计师也是这么想的。

## 故纸堆

开讲之前，先挖点故纸堆。

### NeXT

上世纪80年代，乔布斯被迫离开了他与另一个史蒂夫一并创立的苹果公司，感慨事情荒谬（被自己创立的公司开掉）
之余，开始寻找新的机会，与人联合创立了 Pixar，还创立了 NeXT 公司。前者设计师同学们肯定知道，
这家牛逼公司给我们带来太多精彩动画电影了，从 Toy Story 到 Monsters, Inc. 一时无两。

而后者，NeXT 计算机公司，所出产的产品则成为了世界上第一个网站服务器。WWW 的创始人 Tim
Berners-Lee 在一台 NeXT 工作站上编写了一个叫做 HTTPd 的程序，和相应的客户端浏览器，还在那台
机器上贴了小纸条：这台机器是服务器，不许关机。

从销售上说，NeXT 并不是家厉害的公司。乔布斯给它的定位是高端配置，牛逼界面，正因为后者，它所积累的
软件开发经验被整合到了后来的 OS X，也就是诸位同僚使用的 MacBook Pro 或者 iMac 上所跑着的代码。

### WorldWideWeb

高端机器是科研人士心头爱，在欧洲原子核物理做研究员的 Tim Berners-Lee 自然不例外。1990 年，
他起草了 WorldWideWeb 项目，并在一台 NeXT 机器上完成了整套项目：

- Web 浏览器（它本身也是个 Web 编辑器）
- Web 服务器
- 相应的网页，描述了这个项目本身

他的这个项目，也被简称作 W3。1994 年，Tim 离开欧洲原子核物理研究所，跑到 MIT，得到 DARPA 支持，
创立了 W3C，即 World Wide Web Consortium。如今前端同学们所热衷的 Web 前沿规范，正是 W3C
在讨论、推进的。

### CERN

CERN 的全称是欧洲原子核物理研究所。2008年的时候，CERN 非常出名，因为他们搞了个巨大的强子对撞机，
据说搞不好会制造黑洞，把地球吞掉，大家十分关切，有人还做了网站：

<http://hasthelargehadroncolliderdestroyedtheworldyet.com/>

在喧嚣的 2008 年，CERN 和 LHC，也是个热点词汇。你可能想不到，他们竟然也和互联网有关系。

### DARPA

DARPA 的全称是美国国防先进项目所，是军方的机构。前面我说到，DARPA 支持创立了 W3C，但 DARPA
对互联网的贡献可远不止此。早在 1967 年，DARPA 的前身 ARPA（全称里去掉“防御”一词），
所支持的研究项目，创造了世界上第一个互联网，叫做 ARPANET。

那个年代的互联网，网络传输很慢，75% 的网络流量都是彼此传来传去的电子邮件。第一封电子邮件，正是通过
ARPANET 传输的。

## HTML

讲故事，其实三天三夜都讲不完，何况我这里只讲了 WWW 的创立，都还没说后来的浏览器之争，服务器实现演变，
等等。但重点其实是，Tim 早在 1980 年的时候就写了 WWW 的前身 ENQUIRE，当时是 CERN 的独立承包商，
之后又去做了三年技术老板，积累网络编程经验，直到9年后回到 CERN，才把 WorldWideWeb 给做出来。

当真是念念不忘，必有回想。

HTML 的全称是超文本标记语言。超文本是个历史悠久的概念，最早可以追溯到上世纪40年代，和它一块演进的
是超媒体，后者可以算是前者的富集。不过对设计师来说，这俩都不重要，重要的是，最早的 WorldWideWeb，
目的是用超文本的概念，方便研究者们共享研究资料。直至今日，W3C 制定 HTML 规范的原则仍然是这个，
所以，HTML 的别名是文档，它应该语义化，装饰类的标签应该去除，样式代码应该分离，等等。

所以，不管诸位的设计如何绚丽，那份 PSD，最终都会被前端工程师用语义化的 HTML 写成一份文档，它是个
文本文件，你在 Windows 中用记事本，在 Mac 里用 TextEdit，都能打开它。

### 文本文件

在计算机世界里，文件有好多种，最基本的区分方式就是它的扩展名，但扩展名也有会忽悠人的，系统里某些配置
文件故弄玄虚，甚至还喜欢把扩展名省去。当然大多数时候并非它们故意，使用不同的扩展名，目的是让操作系统
可以更好地区分自己而已。

HTML 文件也是如此，它的扩展名是 .html 或者 .htm，系统一般用默认的 Web 浏览器打开，它是文本文件，
把扩展名改成 .txt，再双击就是用系统默认的文本编辑器打开了。要注意的是，自 Windows XP 起，
操作系统默认是隐藏扩展名的。

与文本文件不同的，是 .psd、.doc 等文件，它们有的是二进制文件，使用自有的数据编码格式，有的是复合的，
可能是个压缩包，可能是个自解压的二进制文件（用过那种可以放在U盘里的所谓绿色版软件吗？）。

不过，我可不想把计算机基础知识在这先重复一遍，大家都是21世纪的人，我们有更好的办法。jsFiddle 和
Github Gist，正是其中两个编写代码演示的好去处。

### HTML 框架

所有的 HTML 页面都大概长这个样子：

```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
  </head>
  <body>
    <h1>设计师该知道的 HTML 与 CSS</h1>
    <p>人在江湖飘，能够多一技傍身，何乐而不为？</p>
  </body>
</html>
```

每个 HTML 文档都有个头部声明，叫做 DOCTYPE，声明方式多年前曾经百花齐放，这么写会如何如何，那么写
又你想怎样，等等。在我们这个示例里头，正是 HTML5 运动起始时变得风靡的写法：

```html
<!doctype html>
```

然后，就是超文本概念的真实演绎了。超文本其实就是标记文本，利用一系列规则，给普通的文本嵌入标记，
这里强调，那里链接到别处，这里有个图片，那里有个引用，诸如此类。HTML自然不能算是只此一家，真正把这
东西规范化的，是 SGML。SGML 是元标记语言，这句话的意思是，SGML 是用来定义标记语言语法的语言。

言归正传，HTML 这门标记语言里要求，所有的文档内容都在 `<html>` 标签之内，文档内容分成 `<head>`
与 `<body>`。这俩英文单词的意思，大家应该都懂的。所以现在你能看明白这张图了：

![head body](http://www.likecool.com/Gear/Pic/head%20body%2045399156/head-body.jpg)

### head

HTML 头部，通常内容有：

- 文档的文件编码
- 文档的额外信息
- 文档的标题
- 文档的收藏夹图标
- 文档的外部、内联样式
- 文档的外部、内联脚本

其中涉及到的 HTML 标签有 `<link>`、`<meta>`、`<script>` 和 `<title>`。设计师在此处需要
注意到的是收藏夹图标（favicon）。这货的作用从它的英文名字就能看出来，它是 favorite icon 的缩写，
最初的作用就是，当用户收藏你的网页，能在收藏夹里看到这个网页的图标。因此，它能提高你的网站的辨识度。

如今呢？它的用处更趋广泛，除了收藏夹之外，它还出现在浏览器标签栏，Windows 7 还支持直接拖拽链接到
快速启动栏，从而让用户可以在桌面直达你的网站。

### body

`<body>` 是繁华所在，在最初的 HTML 中，HTML 中只是一些文本内容，加上一些加粗、斜体、外部链接、
标题、段落、引用之类，后来又陆续加上了图片等多媒体的内容，并有 `<object>`、`<embed>` 等标签。

在 HTML5 里，我们又有了 `<video>`、`<audio>`、`<canvas>`、`<svg>` 等等。

这些琳琅满目的标签都用来做什么？答案很简单，它们的存在，就是为了让我们的内容，能够用标记文本描述出来。

好吧，内容很丰富了，样式怎么控制呢？

## CSS

我们用 CSS。不过开讲之前，有得讲个故事。

多年前，在浏览器的战国时代，呃，确切说更像是楚汉争霸时代，楚国 Netscape 公司雄霸一方，靠卖浏览器
赚得盆满钵满，有一票牛人，例如 [jwz](http://www.jwz.org/)，汉 微软 IE 开发小组，刚起步，
和刘邦不同的是 IE 开发小组有个牛逼干爹，最终它靠着干爹带，把楚国给打败了。不过结果不重要，重要的是，
在两方斗争过程中，由于当时谁也不知道 HTML 的规范该如何如何，而谁都想跟用户说用我把我最牛逼，
导致两大浏览器 Netscape、Internet Explorer 各做各的，Netscape 搞了个
[`<blink>`](http://en.wikipedia.org/wiki/Blink_element)，IE 搞了个
[`<marquee>`](http://en.wikipedia.org/wiki/Marquee_element)，更多乱七八糟的细枝末节，
最终把 Web 开发者搞残了，直至今日，可以只为一款浏览器开发网页，都是一种幸福。

<iframe width="100%" height="200" src="http://jsfiddle.net/dotnil/AVzCv/embedded/result/" scrolling="no" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

互拼软件实现度的结果是，最终用户选择了免费的那个。

所以了解用户操蛋的需求是多么重要。如今翻旧账再来揣测，IE 的免费，更像是给免费模式的互联网拉开大幕，
雅虎第一个登场，Google、Facebook、Taobao 们开始割据。

扯远了，乱世之后，是大一统，当时的 Web 从业者们终于意识到，胡搅蛮缠该结束了。W3C 规范指定步入正轨，
Firefox 冒出来扛着规范大旗鞭挞曾经对规范实现度最高的 IE6，没错，那个 IE6，在它发布后的很长一段
时间里，它都是最牛逼的浏览器。但再牛逼的浏览器也抗不过时间，也抗不过 Firefox 的当众调戏、Opera 和
Safari 的偷偷揩油。Web 开发者们开始呼吁内容与形式分离，让 HTML 回归朴素，把效果，放入 CSS。

于是后来冒出一些著名的 CSS 宣传网站，[CSS Zen Garden](http://www.csszengarden.com/)
便是其中之一。它的立意很有趣，同一份 HTML，通过不同的 CSS 得到完全不同的效果。考虑到当时的网络环境、
CSS 规范实现程度，这个网站做得很不赖。

说到这里，本文的立论也就出来了，内容回归 HTML，效果放入 CSS，作为设计网页展现形式的你，懂一点 CSS
真的是大有裨益喔。

### 字体

我们经常会听到设计师或者需求方这样要求，这里给我用微软雅黑，看上去高端洋气一点，啊，能不能所有的都是
微软雅黑，微软雅黑多好看呀。对于用惯了 Windows 系统，一路宋体走过来的同学们来说，Windows
Vista 里开始加入的雅黑、Tahoma 等反锯齿字体无疑是个福音。中文突然也不那么毛毛糙糙了，既然它这么好，
干嘛不全用上呢？

负责任的前端开发可能已经告诉你了，那在那些没有微软雅黑字体的浏览器里怎么办，用什么字体呢？

要回答这个问题，我们得从 Web Safe Fonts 概念说起，在 Internet 如火如荼的日子里，Web 开发者和
浏览器厂商都需要面对的一个问题是，都有那些字体可用。在这里需要表扬的是微软（咦，好奇怪）。1996 年，
它开始了一项叫做 [Core Fonts for the Web](http://en.wikipedia.org/wiki/Core_fonts_for_the_Web)
的项目，为因特网提供可免费使用的私有字体：

- Andale Mono
- Arial
- Arial Black
- Comic Sans MS
- Courier New
- Georgia
- Impact
- Times New Roman
- Trebuchet MS
- Verdana
- Webdings

支持 Windows 和 Mac。因为授权协议，虽然 2002 年项目终止，这些已经发布的字体都能免费使用，使得
开源社区也能得享便利，因此，所谓的 Web Safe Fonts，其实就是指主流计算机平台（Windows、Mac OS、
Unix + X）上[均有支持的字体](http://web.mit.edu/jmorzins/www/fonts.html)：

- <span style="font-family:Arial">Arial</span> / <span style="font-family:Helvetica">Helvetica</span>
- <span style="font-family:Times New Roman">Times New Roman</span> / <span style="font-family:Times">Times</span>
- <span style="font-family:Courier New">Courier New</span> / <span style="font-family:Courier">Courier</span>

注意这里的字体划分方式：

- Arial 和 Helvetica 归为一类，它们是无衬线字体，即 sans-serif。在 CSS 中，这个类别概念叫做
  字族，即 font-family 属性；
- Times New Roman 和 Times 也是一类，它们属于 serif 字族，即有衬线字体；
- Courier New 与 Courier 又是一类，它们是等宽字体，字族叫做 monospace。

当然，随着事件推移，技术演进，能在 Web 中安全使用的字体早已不止这六个，字族也日渐丰富，但通常而言，
字族[分成如下几类](http://en.wikipedia.org/wiki/Web_typography#Generic_font_families)：

- <span style="font-family:sans-serif">sans-serif</span>：无衬线字体，通常认为它们在屏幕上表现更好，更清晰
- <span style="font-family:serif">serif</span>：有衬线字体
- <span style="font-family:monospace">monospace</span>：等宽字体，中文天生等宽，英文则不同
- <span style="font-family:cursive">cursive</span>：草书
- <span style="font-family:fantasy">fantasy</span>：含有符文或者装饰属性，但仍能表示字符的字体

通常在浏览器里，前三者是可配置的，用户可以设置自己在各个字族里偏好的字体。

然后回到微软雅黑，假如要设置标题字体成雅黑，那么正确的 CSS 应该这么写：

```css
h1 {
    font-family: Microsoft Yahei, sans-serif;
}
```

我们设置了最佳字体为微软雅黑，但对于没有雅黑的用户，我们告诉它这里用用户浏览器里设置的无衬线字体即可。
但是要注意的是，浏览器里的设置是会坑人的，浏览器并不阻止用户给等宽字族设置非等宽字体，所以，为了取得
更好的设计体验，假如必须设置字体，则越详细越好：

```css
h1 {
    font-family: Microsoft Yahei, Hiragino Sans GB, Helvetica, Arial, sans-serif;
}
```

在这里我告诉用户，你的电脑如果有微软雅黑，那就用雅黑；如果没有雅黑，那有[冬青黑](http://www.typeisbeautiful.com/2010/01/1894/)
（Mac 下新增的中文字体，显示效果极佳）没？还没有啊，那就用 Helvetica，不行就 Arial。再不行，就
随便哪个无衬线字体把。

### 盒子模型

前端工程师通常都希望设计师帮忙标注设计稿中各个设计元素的尺寸，但在设计师标注完尺寸之后，又会很愤怒地
表示这不是他想要的。这种时候，双方的想法估计都是：

![](/assets/img/2013/are-you-f-kiding-me.jpg)

这里有个期望的差距，也正是本文想要填充的一个沟通的障碍。要标注符合 Web 设计的尺寸，最好先厘清 CSS
中盒子模型的概念。

前面我们说，在 HTML 诞生之初，它就是个文档的概念，是用来给研究者们共享文档、附件用的，但是在后来，
渐渐地假如了 img、embed、video 等多媒体的内容，Web 内容也日趋丰富。于是浏览器犯难了，怎么把一份
文档，渲染出一个层次化的页面呢？

对浏览器而言，HTML 中的一个个标记，就是一个个小节点，`<video>` 标签，散落文档各处的文本，都是节点，
每个节点都有它所属的类型，而每个类型的显示方式都可以归到如下几类：

- block
- inline
- inline-block

即区块、内联、内联区块，我们先从区块开始。

<iframe width="100%" height="300" src="http://jsfiddle.net/dotnil/dBaSs/embedded/result" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

在 CSS 中，每个区块都有三个属性可供设置，按照从外到内的顺序：

- margin：边距
- border：边框
- padding：填充

在我的示例中，按区域颜色从浅至深的顺序设置。点 CSS 标签，可以看到 `.box` 区块的三个属性设置，为了
显示效果，我还设置了背景色：

```css
.box {
    margin: 20px;
    border: 5px solid #ccc;
    padding: 30px;
    background: #999;
}
```

修改 margin 的效果：

![](/assets/img/2013/margin.gif)

修改 border 的效果：

![](/assets/img/2013/border.gif)

修改 padding 的效果：

![](/assets/img/2013/padding.gif)

每一个块级元素都有这三个属性，边距、边框、填充。

### 浮动与定位

TODO

### 布局

TODO

## 跋

给设计师的教程，是不应该像本文这般枯燥乏味的，本文可以算是知识点的预整理，在 2013 下半年，我将整理
本文，将其以 Web 小应用的形式展现。

希望我说到做到，哈哈。
