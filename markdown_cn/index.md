# GNU C 语言手册

下一篇: [第一个例子](The-First-Example.md)  

---

# GNU C 手册

本手册阐释了如何使用 GNU 编译器套件（GCC）在 GNU/Linux 系统及其他系统上应用 C 语言。我们将这种方言被称 GNU C 。如果你已经了解 C 了，你可以使用本书当作参考手册。

如果你知道一些基本的编程概念，但对于 C 一无所知的话，你可以按顺序阅读本书，当作 C 语言学习的开端。

如果你是编程领域的初学者，与 C 相比，我们建议你首先去学习一门带垃圾回收及无显式指针的语言。一些良好的选择包括 Lisp、Scheme、Python 和 Java。C 的显示指针意味着程序员必须小心地避免某些类型的错误。

C 是一门古老的语言；它首次被使用是在 1973 年。GNU C 编译器首次发布于 1987 年，随后被扩展为了 GNU 编译器套件。其它一些重要的语言都是基于 C 设计的：一旦你了解 C ，C 就会为你提供一个有益的基础，去学习 C++ 、 C# 、 Java 、 Scala 、Go 等等。

C 特殊的优势在于它是相当简单的，同时他允许接近计算机的硬件——这在之前是需要用汇编语言去描述单独的计算机指令。一些人称呼 C 为“高级汇编语言”，因为它的显式指针和对内存自动管理的缺乏。正如一位专家所说：“C 结合了汇编语言的优势和便利。”但 C 可移植性更高，且比汇编语言更易阅读。

本手册描述了截至 2017 年由 GNU 编译器套件支持的 GNU C 语言。请告知我们如果当前有任何变化内容已无法匹配当前版本的 GNU C 。

当一个构建可能在其他 C 编译器中缺失或以不同方式工作时，我们这样说。当它不是 ISO C 标准的一部分时，我们称呼其为“GNU C 扩展”，因为知道这一点很有用。然而，标准和其他方式是本手册的次要话题。为了简单起见，我们保持笔记的简单，除非有必要多说。

同样，我们几乎很少提及 C++ 或其他 GNU 编译器套件所支持的程序。我们希望本手册能为这些语言编写手册，但语言间有太多不同，以至于我们不能通过一本通用的手册分享他们。

C 程序的一些概念的含义取决于它所依赖的目标平台：我们这么说，就是编译后的代码将会运行在那台计算机上和哪个操作系统上。

C 语言没有提供内建的工具，像是一些如输入输出，内存管理，字符串操作以及诸如此类的共用操作。取而代之，这些工具将会被定义为共享标准库的函数提供，并在每个 C 程序里自动可用。参见 GNU C 库参考手册中的 [GNU C 标准库](https://www.gnu.org/software/libc/manual/html_node/index.md#Top)。

GNU/Linux系统使用 GNU C 库来执行此任务。它本身就是一个 C 程序，因此一旦你了解 C，就可以阅读它的源代码，看看它的库函数如何执行任务。其中一部分函数的实现被称为*系统调用*，这意味着它们包含一些特殊的指令，要求系统内核（Linux）执行特定的任务。要了解这些函数是如何实现的，您需要阅读Linux的源代码。无论库函数是否是系统调用，这都是一个内部实现细节，对于如何调用函数没有任何影响。

本手册整合了最早以前的 GNU C 预处理器手册。它还使用了 Trevis Rothwell 和 James Youngman 撰写的早期 GNU C 手册中的一些文本。

GNU C 有许多晦涩的特性，每个特性都是为了历史兼容性或针对非常特殊的情况而设计的。我们将它们保留到了一个附赠的手册，即 GNU C Obscurities 手册，该手册稍后将以数字形式发布。

请将错误和建议报告给 c-manual\@gnu.org。
