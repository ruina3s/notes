---
title: Latex学习
date: 2022-6-20 14:28:00
tab: 
---

Latex学习
==



[toc]



# 0.tex下载安装与vscode配置

参考该[视频](https://www.bilibili.com/video/BV11h41127FD)了解tex与latex，并有对应环境的下载与安装，也可下清华或者中科院的镜像

其中一份文档教程可下载：[一份不太简短的LaTeX介绍](https://github.com/CTeX-org/lshort-zh-cn)，需要在GitHub上下载，本文将摘抄其中内容为笔记。



**vscode上的配置**：

安装插件“latex workshop”

接着配置vscode，单击F1，输入json，选择“setting.json” （注意不要选成默认default的了）

![image-20220620144607320](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20220620144607320.png)

粘贴以下内容：

```json

// LaTeX
    "latex-workshop.latex.autoBuild.run": "never",
    "latex-workshop.showContextMenu": true,
    "latex-workshop.intellisense.package.enabled": true,
    "latex-workshop.message.error.show": false,
    "latex-workshop.message.warning.show": false,
    "latex-workshop.latex.tools": [
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOCFILE%"
            ]
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOCFILE%"
            ]
        },
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "-outdir=%OUTDIR%",
                "%DOCFILE%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ]
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "XeLaTeX",
            "tools": [
                "xelatex"
            ]
        },
        {
            "name": "PDFLaTeX",
            "tools": [
                "pdflatex"
            ]
        },
        {
            "name": "BibTeX",
            "tools": [
                "bibtex"
            ]
        },
        {
            "name": "LaTeXmk",
            "tools": [
                "latexmk"
            ]
        },
        {
            "name": "xelatex -> bibtex -> xelatex*2",
            "tools": [
                "xelatex",
                "bibtex",
                "xelatex",
                "xelatex"
            ]
        },
        {
            "name": "pdflatex -> bibtex -> pdflatex*2",
            "tools": [
                "pdflatex",
                "bibtex",
                "pdflatex",
                "pdflatex"
            ]
        },
    ],
    "latex-workshop.latex.clean.fileTypes": [
        "*.aux",
        "*.bbl",
        "*.blg",
        "*.idx",
        "*.ind",
        "*.lof",
        "*.lot",
        "*.out",
        "*.toc",
        "*.acn",
        "*.acr",
        "*.alg",
        "*.glg",
        "*.glo",
        "*.gls",
        "*.ist",
        "*.fls",
        "*.log",
        "*.fdb_latexmk"
    ],
    "latex-workshop.latex.autoClean.run": "onFailed",
    "latex-workshop.latex.recipe.default": "lastUsed",
    "latex-workshop.view.pdf.internal.synctex.keybinding": "double-click",
    "latex-workshop.view.pdf.viewer": "tab"

```

tex文件的编译：

编写好的tex文件后，在该文件所在位置启动命令行输入

```
pdflatex 文件名
```

即可完成编译并可查看文件位置中对应pdf文件

在vscode中则直接选择文件右上角的绿色三角按钮即可进行编译

![image-20220620145551468](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20220620145551468.png)

按下<kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>p</kbd>后输入“view latex”或按快捷键<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>v</kbd>可打开tex文件的pdf文件查看

![image-20220620145912619](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20220620145912619.png)

![image-20220620150032827](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20220620150032827.png)



# 1.基本概念

## 1.1.编译命令

在命令行或终端中，通过`pdflatex filename`或者`xelatex filename`来对tex文件进行编译，可生成包括同名的pdf文件在内的多个文件

## 1.2.语法

Latex以反斜杠`\`开头，称其为命令，有两种形式：

+ 反斜杠后跟一串字母，以非字母为界限（数字、空格、标点）
+ 反斜杠和一个非字母符号

Latex对大小写是**敏感**的



命令是可以接受参数的，参数分为可选参数（可填可不填）和必选参数：

+ 可选参数用`[]`来包裹
+ 必选参数用`{}`来包裹

有些命令可以带一个星号 *，带星号和不带星号的命令效果有一定差异。初次接触这些概念时，可以粗略地把星号看作一种特殊的可选参数。



**环境**：用以令一些效果在局部生效，或是生成特殊的文档元素。

```tex
\begin{⟨environment name⟩}[⟨optional arguments⟩]{⟨mandatory arguments⟩}
...
 ⟨environment name⟩ 为环境名，begin和end中的应一致
\end{⟨environment name⟩}
```

环境的可选和必选参数不限，也可以没有，可嵌套

有些命令使用后会对之后内容起作用，为限定作用范围可使用`{}`来限制



## 1.3.结构

```tex
\documentclass{...} % ... 为某文档类，指定文档类型
% 导言区 导言区中常会使用\usepackage 命令调用宏包，还会进行文档的全局设置
\begin{document}
% 正文内容
\end{document}
% 此后内容会被忽略
```



## 1.4.文档类

```tex
\documentclass[⟨options⟩]{⟨class-name⟩}
%LATEX 源代码的开头须用\documentclass 指定文档类
```

⟨class-name⟩指定文档的类型

![image-20230217145609931](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20230217145609931.png)

其基础上派生的一些文档类如支持中文排版的 ctexart / ctexrep / ctexbook，或者有其它功能的一些文档类，如 moderncv / beamer 等。

⟨options⟩为可选参数，**全局**指定排版的参数，如字号、纸张大小、单双面等。比如：

```tex
\documentclass[11pt,twoside,a4paper]{article}
%纸张为 A4 大小，基本字号为 11pt，双面排版
```

LATEX 的三个标准文档类可指定的选项包括：

+ 10pt, 11pt, 12pt 指定文档的基本字号。默认为 10pt。
+ twoside, oneside 指定单面/双面排版。双面排版时，奇偶页的页眉页脚、页边距不同。article和 report 默认为 oneside，book 默认为 twoside。
+ onecolumn, twocolumn 指定单栏/双栏排版。默认为 onecolumn。
+ openright, openany 指定新的一章 \chapter 是在奇数页（右侧）开始，还是直接紧跟着上一页开始。report 默认为 openany，book 默认为 openright。对 article 无效。
+ landscape 指定横向排版。默认为纵向。
+ titlepage, notitlepage 指定标题命令 \maketitle 是否生成单独的标题页。article 默认为notitlepage，report 和 book 默认为 titlepage。
+ fleqn 令行间公式左对齐。默认为居中对齐。
+ leqno 将公式编号放在左边。默认为右边。
+ draft, final 指定草稿/终稿模式。草稿模式下，断行不良（溢出）的地方会在行尾添加一个
  黑色方块；插图、超链接等功能也会受这一组选项影响，具体见后文。默认为 final。



## 1.5.宏包

类似于java中的jar包，作为latex的功能扩展。调用宏包的语法如下：

```tex
\usepackage[⟨options⟩]{⟨package-name⟩}
%可以一次性调用多个宏包，在 ⟨package-name⟩ 中用逗号隔开
```

如：

```tex
\usepackage{tabularx, makecell, multirow}
```

使用宏包和文档类之前，一定要首先确认它们是否安装在你的计算机中，否则 \usepackage 等命令会报错误



宏包在使用后可能会更改latex的命令与环境，需要查看宏包的使用说明，用以下命令：

```shell
texdoc ⟨pkg-name⟩
@⟨pkg-name⟩ 是宏包或者文档类的名称
```



## 1.6.Latex常用文件类型

LATEX 在编译过程中

| 文件类型  | 说明                                                         |
| --------- | ------------------------------------------------------------ |
| .pdf .dvi | 编译后用于**阅读**、传播用的文档                             |
| .log      | 排版引擎生成的**日志**文件，供排查错误使用                   |
| .aux      | LATEX 生成的主辅助文件，记录交叉引用、目录、参考文献的**引用**等 |
| .toc      | LATEX 生成的**目录**记录文件                                 |
| .lof      | LATEX 生成的**图片**目录记录文件                             |
| .lot      | LATEX 生成的**表格**目录记录文件                             |
| .bbl      | BIBTEX 生成的参考文献记录文件                                |
| .blg      | BIBTEX 生成的日志文件                                        |
| .idx      | LATEX 生成的供 makeindex 处理的索引记录文件                  |
| .ind      | makeindex 处理 .idx 生成的用于排版的格式化索引文件           |
| .ilg      | makeindex 生成的日志文件                                     |
| .out      | hyperref 宏包生成的 PDF 书签记录文件                         |



宏包和文档类

| 文件类型 | 说明                               |
| -------- | ---------------------------------- |
| .sty     | 宏包文件。宏包的名称与文件名一致   |
| .cls     | 文档类文件。文档类名称与文件名一致 |
| .bib     | BIBTEX 参考文献数据库文件          |
| .bst     | BIBTEX 用到的参考文献格式模板      |

 

## 1.7.文件的组织方式

编写长篇文档时，可将源文件分割成若干个文件，例如将每章内容单独写在一个文件中。

在源代码里插入文件：

```tex
\include{⟨filename⟩}
```

⟨filename⟩ 为文件名（不带 .tex 扩展名)，较新版可带。和要编译的主文件不在一个目录中，则要加上相对或绝对路径

 \include 在读入 ⟨filename⟩ 之前会另起一页。有的时候我们并不需要这样，而是用 \input 命令，它纯粹是把文件里的内容插入：

```tex
\input{<filename>}
```

\include 和 \input 命令载入的文件名最好不要加空格和特殊字符，也尽量避免使用中文名

LATEX 还提供了一个 \includeonly 命令来组织文件，用于**导言区**，指定只载入某些文件。导言区使用了 \includeonly 后，正文中不在其列表范围的 \include 命令不会起效:

```tex
\includeonly{⟨filename1⟩,⟨filename2⟩,...}
```



工具宏包 syntonly。加载这个宏包后，在导言区使用 \syntaxonly 命令，可令 LATEX 编译后不生成 DVI 或者 PDF 文档，只排查错误，编译速度会快不少：

```tex
\usepackage{syntonly}
\syntaxonly
```



## 1.8.LATEX 和 TEX 相关的术语和概念

**引擎**：全称为排版引擎，是编译源代码并生成文档的程序，如 pdfTEX、XƎTEX 等。有时也称为编译器。
**格式**：是定义了一组命令的代码集。LATEX 就是最广泛应用的一个格式。
**编译命令**：是实际调用的、结合了引擎和格式的命令。如 xelatex 命令是结合 XETEX 引擎和LATEX 格式的一个编译命令。



# 2.排版

## 2.1.编码

现行的latex使用utf-8编码，但任然需要调用宏包才可编译中文。ctex宏包



## 2.2.字符

空格键和 Tab 键输入的空白字符视为“空格”。连续的若干个空白字符视为一个空格。一行开头的空格忽略不计。

行末的换行符视为一个空格；但连续两个换行符，也就是空行，会将文字分段。多个空行被视为一个空行。也可以在行末使用 \par 命令分段。

使用`%`来作为注释符

其它特殊字符如：$、^、_等用于其它排版，若要在文档中显示出来则要如其它编程语言一样前面甲`\`进行转义



## 2.3.标点符号

中文的标点符号（绝大多数为非 ASCII 字符）使用中文输入法输入即可，一般不需要过多留意。而输入西文标点符号时，有不少地方需要留意。

**引号**：单引号用 ` 和 ‘ 来输入，双引号用 `` 和 ’‘ 来表示

**连字**和**破折号**：

```tex
- % 连字符
-- % 短破折
--- % 长破折号
```

**省略号**：`\ldots`

**波浪号**：`\~`



## 2.4.拉丁文扩展与重音

![image-20230218190130198](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20230218190130198.png)



## 2.5.其它特殊符号

参考[The Comprehensive LaTeX Symbol List (tsinghua.edu.cn)](https://mirrors.tuna.tsinghua.edu.cn/CTAN/info/symbols/comprehensive/symbols-a4.pdf)



## 2.6.latex标志

```tex
\TeX
\LaTeX
\LaTeXe
```



## 2.7.断行与断页

```tex
文本~文本 % ~ 会输入一个不会断行的空格
```

断行：

```tex
\\[<length>] % 用于在断行处向下增加垂直间距
\\*[⟨length⟩] % 带*表示禁止在断行处分页
\newline % 不带参数断行，仅用在文本段落中
\\ % 也表示表格、公式换行
```

断页：

```tex
\newpage
\clearpage
% 在双栏排版模式中 \newpage起到另起一栏的作用，\clearpage 则能够另起一页，会在断行/断页位置填充适当的间距
\linebreak[⟨n⟩]  % 断行
\nolinebreak[⟨n⟩] % 不断行
\pagebreak[⟨n⟩]  % 断页
\nopagebreak[⟨n⟩] % 不断页
% 数字 ⟨n⟩ 代表适合/不适合的程度取值范围为 0–4，不带可选参数时，缺省为 4
```

断词：很长的英文单词，仅在单词之间的“空格”处断行无法生成疏密程度匀称的段落时，就会考虑从单词中间断开

使用 `\ -` 命令指定断词的位置



# 3.文档元素

## 3.1.章节与目录

```tex
\chapter{⟨title⟩} % 只在 report 和 book 文档类有定义
\section{⟨title⟩} % 有其它变体
\subsection{⟨title⟩}
\subsubsection{⟨title⟩} 
\paragraph{⟨title⟩} % 有其它变体
\subparagraph{⟨title⟩}
% 这些命令生成章节标题，并能够自动编号
\part %\part 命令，用来将整个文档分割为大的分块，但不影响 \chapter 或 \section 等的编号
```

article 文档类带编号的层级为 \section \subsection \subsubsection 三级；
report / book 文档类带编号的层级为 \chapter \section \subsection 三级

```tex
\tableofcontents % 目录
\addcontentsline{toc}{⟨level⟩}{⟨title⟩} %使用了不生成目录项的章节标题命令，而又想手动生成该章节的目录项，可以在标题命令后面使用
```

所有标准文档类都提供了一个 \appendix 命令将正文和附录分开

book 文档类还提供了前言、正文、后记结构的划分命令：

```tex
\frontmatter % 前言部分，页码使用小写罗马数字；其后的 \chapter 不编号。
\mainmatter % 正文部分，页码使用阿拉伯数字，从 1 开始计数；其后的章节编号正常。
\backmatter % 后记部分，页码格式不变，继续正常计数；其后的 \chapter 不编号。
```



## 3.2.标题页

\maketitle生成简单的标题页。首先需要给定标题和作者等信息：

```tex
\title{⟨title⟩} 
\author{⟨author⟩} 
\date{⟨date⟩}
% 前两个命令是必须
% \today 命令自动生成当前日期，\date 默认使用 \today
\thanks % 生成标题页的脚注,用 \and 隔开多个人名
% article 文档类的标题默认不单独成页，而 report 和 book 默认单独成页。
```

![image-20230219143655258](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20230219143655258.png)

![image-20230219143758610](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20230219143758610.png)



## 3.3.交叉引用

能够被交叉引用的地方，如章节、公v式、图表、定理等位置使用 \label{⟨label-name⟩} 命令

之后可以在别处使用 \ref{⟨label-name⟩} 或 \pageref{⟨label-name⟩} 命令，分别生成交叉引用的编号和页码

\label 命令可用于记录各种类型的交叉引用，使用位置分别为：
**章节标题** 在章节标题命令 \section 等之后紧接着使用。
**行间公式** 单行公式在公式内任意位置使用；多行公式在每一行公式的任意位置使用。
**有序列表** 在 enumerate 环境的每个 \item 命令之后、下一个 \item 命令之前任意位置使用。
**图表标题** 在图表标题命令 \caption 之后紧接着使用。
**定理环境** 在定理环境内部任意位置使用。



## 3.4.脚注与边注

```tex
\footnote{⟨footnote⟩} % ⟨footnote⟩里面为脚注显示的文本
\marginpar[⟨left-margin⟩]{⟨right-margin⟩} % 如果只给定了 ⟨right-margin⟩，那么边注在奇偶数页文字相同；如果同时给定了 ⟨left-margin⟩，则偶数页使用 ⟨left-margin⟩ 的文字
```



## 3.5.列表

```tex
\begin{enumerate} % 有序列表
\item ...
\end{enumerate}
% \item 可带一个可选参数，将有序列表的计数或者无序列表的符号替换成自定义的符号
\begin{itemize} % 无序列表
\item ...
\end{itemize}
```

```tex
\begin{description}
\item[⟨item title⟩] ...
\end{description}
% \item 后的可选参数用来写关键字，以粗体显示，一般是必填的
```

```tex
% 各级无序列表的符号由命令 \labelitemi 到 \labelitemiv 定义，可以简单地重新定义它们
\renewcommand{\labelitemi}{\ddag}
\renewcommand{\labelitemii}{\dag}
% 有序列表的符号由命令 \labelenumi 到 \labelenumiv 定义，重新定义这些命令需要用到计数器相关命令
\renewcommand{\labelenumi}%
{\Alph{enumi}>}
```



## 3.6.对齐

```tex
\begin{center} ... \end{center} % 居中
\begin{flushleft} ... \end{flushleft} % 左对齐
\begin{flushright} ... \end{flushright} % 右对齐
% 还可以用以下命令直接改变文字的对齐方式
\centering 
\raggedright 
\raggedleft
```



## 3.7.引用

```tex
% quote 用于引用较短的文字，首行不缩进
\begin{quote}
...
\end{quote}
% quotation 用于引用若干段文字，首行缩进
\begin{quotation}
...
\end{quotation}
% verse 用于排版诗歌，verse 是首行悬挂缩进的
\begin{verse}
...
\end{verse}
```



## 3.8.摘要

摘要环境 abstract 默认只在标准文档类中的 article 和 report 文档类可用，一般用于紧跟\maketitle 命令之后介绍文档的摘要。如果文档类指定了 titlepage 选项，则单独成页；反之，单栏排版时相当于一个居中的小标题加一个 quotation 环境，双栏排版时相当于 \section* 定义的一节



## 3.9.代码

```tex
\begin{verbatim}
... % 放代码
\end{verbatim}
% 带 * 号的空格显示成“␣”
\begin{verbatim*}
...
\end{verbatim*}
```

```tex
% 排版简短的代码或关键字，可使用 \verb
\verb⟨delim⟩⟨code⟩⟨delim⟩
% ⟨delim⟩ 标明代码的分界位置，前后必须一致，除字母、空格或星号外，可任意选择使得不与代码本身冲突，习惯上使用 | 符号
% \verb 后也可以带一个星号，以显示空格
```

verbatim 宏包优化了 verbatim 环境的内部命令，并提供了 \verbatiminput 命令用来直接读入文件生成代码环境。

fancyvrb 宏包提供了可定制格式的 Verbatim 环境；

listings 宏包更进一步，可生成关键字高亮的代码环境，支持各种程序设计语言的语法和关键字。详情请参考各自的帮助文档



## 3.10.表格



## 3.11.图片



## 3.12.盒子



## 3.13.浮动体







# 4.数学公式排版



# 5.排版样式设定



# 6.特色工具与功能



# 7.绘图



# 8.其它







# ？.latex公式排版功能与在word中的使用

为了方便word的公式排版故优先学习这部分，并且优先排版，具体的代码性质在之后补充

在word中使用插入公式（<kbd>alt</kbd>+<kbd>=</kbd>）后输入对应排版代码按<kbd>ctrl</kbd>+<kbd>=</kbd>便可切换为公式，再按<kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>=</kbd>切回代码模式

注：快捷键不管用时可选择公式右侧的三角按钮选择“专用”，需再编辑时选择“线性”

![image-20220621155627901](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20220621155627901.png)

## 1.1行内公式与行间公式

**行内公式**：与文字混合排列；**行间公式**：单独一行

行内使用一对<kbd>$</kbd>符号包裹

```
$a^2 + b^2 = c^2$
```

行间使用<kbd>equation</kbd>环境包裹，且latex中会自动为公式生成编号

```
\begin{equation}
a^2+b^2=c^2
\end{equation}
```

注：在word中均只用输入排版代码即可

编辑公式时进入**数学模式**空格无视由运算符决定



