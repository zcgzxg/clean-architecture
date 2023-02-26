# 设计原则

好的软件系统始于干净的代码。一方面，如果砖头不做好，建筑的结构就不那么重要。另一方面，你可以用做得好的砖头造成实质性的混乱。这就是 SOLID 原则的用处所在。

SOLID 原则告诉我们如何将我们的函数和数据结构排列成类，以及这些类应该如何相互连接。使用“类”这个词并不意味着这些原则仅适用于面向对象的软件。类只是函数和数据的一种耦合分组。每个软件系统都有这样的分组，无论它们是否被称为类。SOLID 原则适用于这些分组。
这些原则的目标是创建中层软件结构，以实现以下目标：

- 容忍变化，
- 并且，易于理解
- 是可以用于许多软件系统的组件的基础。

术语“中层”指的是在模块级工作的程序员应用这些原则。它们应用于代码级别之上，并帮助定义模块和组件中使用的软件结构类型。

就像可以用做好的砖头造成实质性的混乱一样，用精心设计的中层组件也可能造成系统范围的混乱。因此，一旦我们涵盖了 SOLID 原则，我们将继续探讨它们在组件世界中的对应原则，然后是高层架构的原则。

SOLID 原则的历史悠久。在 20 世纪 80 年代后期，我与其他人在 USENET（一种早期的 Facebook）上辩论软件设计原则时开始汇编它们。多年来，这些原则已经不断变化。有些被删除，有些合并，有些增加。最终的分组在 21 世纪初稳定下来，尽管我按不同的顺序呈现了它们。

在 2004 年左右，迈克尔·菲瑟斯（Michael Feathers）给我发了一封电子邮件，说如果我重新排列这些原则，它们的第一个单词会拼出单词“SOLID”，因此 SOLID 原则诞生了。

接下来的章节将更详细地描述每个原则。以下是摘要：

- SRP：单一职责原则

  作为康威定律的一个积极推论，它表明一个软件系统的最佳结构受到使用它的组织的社会结构的严重影响，以便每个软件模块都有一个且仅有一个更改原因。

- OCP：开闭原则

  Bertrand Meyer 在 20 世纪 80 年代使这个原则变得著名。其要点是为了使软件系统易于更改，必须设计使这些系统的行为可以通过添加新代码而不是更改现有代码来改变。

- LSP：里氏替换原则

  Barbara Liskov 在 1988 年提出了子类型的著名定义。简而言之，该原则表明，为了从可互换的部件构建软件系统，这些部件必须遵守一个允许这些部件相互替换的契约。

- ISP：接口隔离原则

  该原则建议软件设计师避免依赖于他们不使用的东西。

- DIP：依赖反转原则

  实现高级策略的代码不应依赖于实现低级细节的代码。相反，细节应该依赖于策略。

> 这些原则多年来已经在许多不同的出版物中详细描述过。接下来的章节将重点关注这些原则的架构影响，而不是重复这些详细讨论。如果您还不熟悉这些原则，下面的内容无法详细理解它们，您最好研究脚注文档中的内容。例如，《敏捷软件开发，原则、模式和实践》，Robert C. Martin，Prentice Hall，2002 年，http://www.butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod，和https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)（或者只是谷歌SOLID）。