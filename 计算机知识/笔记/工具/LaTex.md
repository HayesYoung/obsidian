# 1. 基本了解和设置
#### Latex 是什么
LaTeX是一种排版系统，用于创建高质量的科技文档、学术论文、书籍、报告以及其他文档型，由Donald Knuth于1980开发

核心功能：
- 

#### 注释
- 单行注释
```latex
% hello world！
```

- 多行注释
使用 \iffalse 和 \fi 命令或者调用包
```latex
\iffalse
hello world！
\fi

% --------------------------

\usepackage{verbatim}
\begin{comment}
hello world！
\end{comment}
```


#### 汉化
LaTex 常用的实现中文方式
- ctex 宏包
```laTex
% 直接使用ctexart，ctexrep，ctexbook，ctexbeamer
\documentclass{ctexart}

%-----------------------------------------------
% 导入ctex宏包
\documentclass{article} 
\usepackage[UTF8]{ctex}
```



#### 源代码结构
LaTex的源代码分为两个部分：导言区 和 正文区

- 导言区，设置全局命令 

```LaTex
\documentclass{article} % 定义文档的类型（article、report、book等） 
\usepackage[UTF8]{ctex} % 引入宏包

%设置文档的标题、作者和日期
\title{My LaTex note} 
\author{Hayes Young} 
\date{\today} %当前日期
\date{2023 7 23} %也自定义日期

\newcommand{\hello}{Hello, World!}  % 自定义新命令 

\begin{document} % 正文开始
```


- 正文区，文档显示的内容

在 \begin{document} 和  \end{document} 之间，一个文档只能有一个 document 坏境 ，\end{document}  后面的代码会直接忽略

```LaTex
\begin{document}

\maketitle % 显示文档信息，上面的标题作者时间等


正文显示区域

\hello  % 上面的设置的自定义，会输出 hello, World!


\end{document}

%--------------------------------

\begin{document}
这里的会直接忽略
\end{document}
```


![[class1.pdf]]



#### documentclass{} 命令 
`\documentclass{}` 命令用于指定文档的类型或类别。

语法格式
```laTex
\documentclass[option1, option2, ...]{class}
```

- `options` ：可选参数，指定文档样式，例如字号、纸张大小等。

```laTex
% A4 纸张大小，12号字体
\documentclass[12pt, a4paper]{article}
```

- `class` ：必选参数：只有五种，其他宏包的也是基于这五种
```laTex
1. `article`: 用于写短文稿、期刊论文、简单的报告等。
2. `report`: 适用于较长的报告、学位论文等。
3. `book`: 用于书籍、综合性的长篇文档。
4. `letter`: 用于写信。
5. `beamer`: 用于制作演示文稿（幻灯片）。
```



# 2. 字体样式



字体类型：
- `\rmfamily`  `\textrm{}`：罗马字体（默认字体）。
- `\sffamily` `\textsf{}`：无衬线字体。
- `\ttfamily` `\texttt{}`：打字机字体。
- `\songti` 
- `\fangsong`
- `\heiti`
- `\kaishu`

字体粗细
- `\mdseries`  `\textmd`{}： 正常字体大小 (默认粗细)
- `\bfseries` `\textbf{}` ：加粗字体  

字体型状:
- `upshhape` `\textup{}`：直立体 (默认字体型状)
- `\itshape` `\textit{}`：意大利斜体
- `\slshape` `\textsl{}`：斜体
- `\scshape` `\textsc{}`：小型大写字母

字体大小:
- `\tiny`：最小的字号。
- `\scriptsize`：较小的字号。
- `\footnotesize`：脚注字号。
- `\small`：小号字体。
- `\normalsize`：默认字号（通常为12pt）。
- `\large`：大号字体。
- `\Large`：更大号字体。
- `\LARGE`：更大号字体。
- `\huge`：巨大号字体。
- `\Huge`：最大的字号。

特殊字符：
- `\textbackslash`：用于显示反斜线 `\`
- `\textdollar`：用于显示美元符号 `$`
- `\&`：用于显示 `&`
- `\#` #
- 


# 文章

文章结构：
- `\section{}`：一级标题。
- `\subsection{}`：二级标题。
- `\subsubsection{}`：三级标题。

- `\paragraph{}`：段落标题。
- `\subparagraph{}`：子段落标题。

- `\par`：换行


# 数学公式
数学公式排版有两种形式
- 行内排版
公式会和正文混合在一起
```latex
$y=x^2$
$y=x^{99}$

```

- 行间排版
公式单独占用一行
```latex
$$y=x^6$$
$$y=x^{88}$$
```