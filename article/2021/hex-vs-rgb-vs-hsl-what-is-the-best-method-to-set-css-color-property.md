> * 原文地址：[HEX vs RGB vs HSL: What is the Best Method to set CSS Color Property](https://blog.bitsrc.io/hex-vs-rgb-vs-hsl-what-is-the-best-method-to-set-css-color-property-f45d2debeee)
> * 原文作者：[Nethmi Wijesinghe](https://medium.com/@wnethmi96)
> * 译文出自：[掘金翻译计划](https://github.com/xitu/gold-miner)
> * 本文永久链接：[https://github.com/xitu/gold-miner/blob/master/article/2021/hex-vs-rgb-vs-hsl-what-is-the-best-method-to-set-css-color-property.md](https://github.com/xitu/gold-miner/blob/master/article/2021/hex-vs-rgb-vs-hsl-what-is-the-best-method-to-set-css-color-property.md)
> * 译者：[霜羽 Hoarfroster](https://github.com/PassionPenguin)
> * 校对者：[Chorer](https://github.com/Chorer)、[nia3y](https://github.com/nia3y)、[CarlosChenN](https://github.com/CarlosChenN)

# HEX vs RGB vs HSL：设置 CSS 颜色属性的最佳方法是什么

![](https://cdn-images-1.medium.com/max/5760/1*fjzP30im_c--lgsIKqhj0g.jpeg)

不知道你是否了解 HEX、RGB 和 HSL 之间的区别，以及其中任意一种的各种优势？

---

在深入探讨这个问题之前，让我们简要了解每种颜色方法的含义。

## 颜色方法的定义

**Hex** 颜色值是最流行的设置 CSS 颜色属性的方法之一，尤其是在开发人员中。几乎所有浏览器都支持它。

我们可以在十六进制颜色代码中定义紫色，如下所示：

```text
#800080
```

这里的颜色的格式规定是 `#RRGGBB`，其中 `RR`（红色）、`GG`（绿色）和 `BB`（蓝色）是介于 `00` 和 `FF` 之间的**十六进制整数**，表示色彩强度。

## HEX 和 RGB 的区别

**RGB** 或 **Red/Green/Blue**（即红/绿/蓝）也被用于在 CSS 中定义颜色，是另一种广受欢迎的方法。RGB 配色方案是一种三通道格式，其中 r、g、b 三色的数值是 0 到 255 之间的整数。以下是 RGB 颜色的示例：

```text
rgb(128, 0, 128)
```

上述 RGB 颜色代码的实现与上文中 HEX 颜色一致。你可能想知道，明明十六进制颜色代码更容易记住和输入，为什么我们还要使用 RGB 呢？

> 嗯，每种颜色方法都有自己的好处。RGB 的美妙之处在于它允许你为颜色添加不透明度。

这就是 **RGBA** 的强处了 😎。在 CSS3 中，RGB 配色方案新增了一个额外的 **alpha** 通道，以指示颜色的不透明度。

> 译者注：其实嘛，Hex 也支持，比如说 50% 黑色就是 `#00000088`，最后两位数为十六进制的透明度，范围也是 `00` 到 `FF`。

## 新人，HSL！

**HSL** 代表色相 Hue、饱和度 Saturation 和亮度 Lightness，是另一种在 CSS 中声明颜色的方式。紫色的 HSL 颜色值可以指定如下：

```text
hsl(300, 100%, 25.1%)
```

如你所见，第一个参数用于定义色相，它是实际纯色的值，例如红色、黄色、绿色、蓝色、洋红色等。色相是一个颜色轮，取值为 0 到 360 的度数。这里 0 和 360 度代表红色，120 度代表绿色，240 度代表蓝色。

与 RGB 不同，在 HSL 中，颜色的饱和度和亮度都可以改变。

这些颜色可以是暗淡的，也可以是鲜艳的。颜色越少，它变成灰色的阴影就越多。**饱和度**指代混合色中存在多少颜色，它能控制颜色的**鲜艳或暗淡**程度。

![使用 Brandon Mathis 的 [HSL 颜色选择器](https://hslpicker.com/#ff5100)](https://hslpicker.com/#ff5100)](https://cdn-images-1.medium.com/max/2044/1*-eXO8dohWa8I60_Qo-AKyQ.gif)

如你所见，当饱和度值沿线从 100% 变为 0% 时，颜色会从纯色调变为暗色调。

此外，还有第三个参数代表亮度。这玩意也是一个百分比值，数值范围也是 0% 到 100%，用于描述颜色中黑色或白色的占比。

![使用 Brandon Mathis 的 [HSL 颜色选择器](https://hslpicker.com/#ff5100)](https://cdn-images-1.medium.com/max/2000/1*1s0MaASIXSV9vJw6oFvjgg.gif)

这类似于水彩在绘画中的使用。如果你想让颜色更亮，你可以添加白色，如果你想让颜色更深，你可以添加黑色。因此，100% 的亮度表示完全的白色，50% 表示实际色调颜色，0% 表示纯黑色。

**HSLA** 与 RGBA 类似，是 HSL 的扩展。第四个通道表示颜色的不透明度，与 RGBA 和 Hex-alpha 并无二致。不透明度以十进制值指定，就像在 RGBA 中一样，其中 1 表示完全不透明，0 表示完全透明，中间的所有取值都是部分不透明的。

然而，尽管大多数浏览器支持 RGB 和 Hex 颜色代码，HSL 颜色主要还是在基于 HTML5 的浏览器中得到支持。

---

你可能已经在 CSS 中设置颜色属性时使用过所有或部分的这些颜色方法。Hex 是我个人的最爱，但是他们之间究竟有什么区别，各自又有着怎样的优势？话不多说，一起来了解一下吧！

## 在 CSS 中指定颜色的最佳方法是什么？

如果你习惯了 HTML，你可能更习惯使用 Hex 颜色值，因为 Hex 颜色值在 HTML 中被大量使用。但如果你学过设计，你可能会使用 RGB 表示法，因为它是大多数设计软件（如 Photoshop、Corel 和 Illustrator）中最常用的格式。

我的建议是，如果你是一名纯粹的开发人员并且只想完成你的项目，请继续使用你最熟悉的颜色方式。

> 因为浏览器并不真正关心你使用的是哪种颜色格式，即使不同方法之间有细微的性能变化，但性能差异可以忽略不计。

除此之外，如果你担心可用性、决策对开发人员的影响等，让我们看看哪种方法最适合你的情况。

让我们从十六进制表示法开始。由于其简短的符号，十六进制非常有吸引力。许多开发人员发现，与 RGB 和 HSL 相比，Hex 值非常易于阅读，而且更容易复制到他们喜欢的文本编辑器中。

RGB 在较旧版本的 Internet Explorer（9 及更早版本）中广为人知并受支持。

### HSL 旨在让人类更容易理解！

RGB 和 Hex 等格式的机器可读性比人类可读性强。相反，HSL 旨在让人类更好地理解。HSL 是一种更新且自然的颜色处理方式。

> 与在 Hex 和 RGBA 中你必须通过一些数字来获得你想要的颜色不同，在 HSL 中，我们可以使用 Hue 定义颜色并使用第二和第三个参数百分比来获得你想要的饱和度和亮度级别。

如果我告诉你网页标题需要是 `#578557` 或 `rgb(87, 133, 87)`，你能猜出是什么颜色吗？ 😵 不，除非你是电脑。但是，与此同时，如果我给你 HSL 中的颜色：`hsl(120, 21%, 43%)`？现在猜测有点容易了吧？ Hue 值为 120°，表示它是纯绿色。接下来，它的饱和度为 61%，表明它距离暗灰色（一种非常不饱和的绿色）还有 21%。最后，亮度 43% 意味着颜色从纯色到较暗的一面有 7%。

好的，假设你想让按钮颜色在悬停时更亮，单击时更暗。使用 HSL 轻而易举 —— 只需要增加和减少亮度值，仅此而已，是不是非常吃惊！！ 😎 但是在不使用工具或设计师的帮助下用十六进制或 RGB 来做到这一点是不可能的。

> HSL 是一种模仿现实世界的直观颜色符号。

例如，让我们考虑一张浅蓝色的色纸。它的三种格式的颜色值分别是：

| Hex | RGB | HSL |
| --- | --- | --- |
| #ADD8E6 | rgb(173, 216, 230) | hsl(195, 53.3%, 79%) |

好的，现在把你的手握在离表面几英寸的地方。你手的影子让表面变暗了一点，对吧？在不改变颜色本身的情况下，我们是无法使用 RGB 或十六进制表示法表示这种颜色变化的。但是在 HSL 中，我们仅仅需要稍微调整亮度值，然后就 **大功告成 💥** 了！我们根本不需要对原始颜色进行任何更改，是不是真的很酷？

| | Hex | RGB | HSL |
| --- | --- | --- | --- |
| 原值 | #4f2017 | rgb(79, 32, 23) | hsl(195, 53.3%, 79%) |
| 新值 | #2F819D | rgb(47, 129, 157) | hsl(195, 53.3%, 50%) |

如你所见，Hex 和 RGB 值已经被改到面目全非了，而对于 HSL，只有一个值发生了变化。毫无疑问，在构建配色方案时，HSL 是最有用的。以底色为基础，根据需要调整饱和度和亮度，就是这样！有了 HSL，建立一个配色方案，简直就是小菜一碟。 😋

### 最后，这一切都取决于个人喜好！

现在你可能认为 HSL 是最好的颜色表示法。但是，正如我上面提到的，旧版本的 Internet Explorer 不支持 HSL。同样，每种颜色格式都有其优点和缺点。问题是，这并不重要。

> 最重要的是尽可能保持在项目中使用到的类型的一致性，因为它有助于提高生产力。

* <s>和其他两种颜色相比 Hex 有不支持透明度的限制</s>（译者注：Hex 是支持的……）
* 不使用特定工具来调整 RGBA 颜色是很很困难的
* 旧浏览器不支持 HSLA
    * 如果你所服务的浏览器支持 HSLA 那就忽略这条吧！你可以选择使用任何格式！

在选择在项目中设置 CSS 颜色属性的最佳方法时，你可以考虑以下因素。

1. 使用与开发团队其他成员相同的格式来提高可维护性。
2. 如果你已经熟悉 RGB 格式，请使用它。
3. 如果你的目标访问者使用严重过时的浏览器访问你的网站，请使用 Hex，或者使用如下后备代码：

```css
p {
    color: #FF0000;
    color: hsla(0, 100%, 50%, 1);
}
````

4. 如果以上三点还是没能让你决定使用哪一种，请使用 HSLA。HSLA 允许你像 RGBA 一样使用透明度，而且更具备可访问性。

### 有哪些替代方案？

除了上面提到的方法，还有一些其他方法可以用来在 CSS 中设置颜色属性。

* **使用颜色名称**：所有现代浏览器都支持 140 个标准 CSS 颜色名称。颜色名称是代表特定颜色的关键字，如 `coral`。
* `currentcolor` **关键字**：如果需要引用一个元素的颜色，可以使用这个关键字。
* **HWB 值：** HWB 代表色相、白度、黑度。虽然目前 HTML 不支持它，但它被建议作为 CSS4 的新标准。
* **CMYK 值**：CMYK 是青色、洋红色、黄色和黑色的组合。尽管计算机屏幕使用 RGB 值来显示颜色，但打印机通常使用 CMYK 颜色值来显示颜色。与 HWB 类似，CMYK 在 HTML 中尚不支持，不过也是被建议作为 CSS4 中的新标准。

### 最后

颜色在网页中起着至关重要的作用。在 CSS 中，我们能使用 RGB、Hex 和 HSL 等方法来定义颜色。在本文中，我们了解了用于在 CSS 中设置颜色属性的三种主要方法，以及它们的区别和各自的优缺点，还有可用于在 CSS 中定义颜色属性的其他替代方法。

> 尽管 HSLA 由于其人类可读性而比其他两种方法略有优势，但如果不是针对特定情况，则无关紧要。你可以使用任何你觉得舒服的方式。

看看不同的优缺点，每种方法都优于其他方法，总而言之，决定使用哪种方式在 CSS 中设置颜色属性应取决于以下三个因素：

* 偏好
* 可维护性
* 性能与效果

那么，你更喜欢用什么来设置 CSS 中的颜色？Hex、RGBA、HSLA 或其他什么？原因又是什么？在评论区告诉我吧。 😃

---

希望能在另一篇令人兴奋的文章中再次遇见你。祝你编码愉快！ 💻

> 如果发现译文存在错误或其他需要改进的地方，欢迎到 [掘金翻译计划](https://github.com/xitu/gold-miner) 对译文进行修改并 PR，也可获得相应奖励积分。文章开头的 **本文永久链接** 即为本文在 GitHub 上的 MarkDown 链接。

---

> [掘金翻译计划](https://github.com/xitu/gold-miner) 是一个翻译优质互联网技术文章的社区，文章来源为 [掘金](https://juejin.im) 上的英文分享文章。内容覆盖 [Android](https://github.com/xitu/gold-miner#android)、[iOS](https://github.com/xitu/gold-miner#ios)、[前端](https://github.com/xitu/gold-miner#前端)、[后端](https://github.com/xitu/gold-miner#后端)、[区块链](https://github.com/xitu/gold-miner#区块链)、[产品](https://github.com/xitu/gold-miner#产品)、[设计](https://github.com/xitu/gold-miner#设计)、[人工智能](https://github.com/xitu/gold-miner#人工智能)等领域，想要查看更多优质译文请持续关注 [掘金翻译计划](https://github.com/xitu/gold-miner)、[官方微博](http://weibo.com/juejinfanyi)、[知乎专栏](https://zhuanlan.zhihu.com/juejinfanyi)。