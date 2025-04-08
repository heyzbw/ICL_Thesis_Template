# 帝国理工学院 LaTex模板
> Imperial College London LaTex Template
> 
> Overleaf & Local Compiler


## 使用指南
- 利用 Overleaf 的`Import from GitHuB`将子仓库`Overleaf_Template`直接导入在线编译使用
- `Local LaTaX Template`在本地编译器直接编译使用


## LaTex常见语法学习记录
- 有编号分点
~~~
\begin{enumerate}
	\item 
	\item 
	\item 
\end{enumerate}

更改编号格式为小写罗马数字：
\begin{enumerate}[label=\roman*)]
	\item 
	\item 
	\item 
\end{enumerate}

[label=\Roman*)] -> 大写罗马数字
[label=\arabic*)] -> 数字
[label=(\alph*)] -> 字母

此外，常见调节参数如下：
[
    itemsep=0pt,      % 项间垂直间距
    parsep=0pt,       % 段落内行间距
    topsep=0pt,       % 列表与上文间距
    partopsep=0pt,    % 单独段落时的额外间距
    leftmargin=*,     % 自动左对齐
    label=\arabic*.,  % 数字编号格式
    font=\bfseries,   % 编号加粗
    before=\vspace{-0.5\baselineskip}, % 列表前间距
    after=\vspace{-\baselineskip}       % 列表后间距
]
更多信息可以参考enumitem包的文档：https://ctan.org/pkg/enumitem
~~~
- 无编号分点
~~~
\begin{itemize}
	\item 
	\item 
	\item 
\end{itemize}
~~~
- 图像引入与引用
~~~
\begin{figure}[!h]
	\centering
	\includegraphics[width=.85\textwidth]{P1}
	\caption{图片示意}
	\label{P1}
\end{figure}

\ref{P1}
~~~
- 有编号公式与引用
~~~
\begin{align}\label{E1}

\end{align}

\ref{E1}
~~~
- 表格表头添加与引用
~~~
\begin{table}[!h]
	\centering
	\caption{说明表}
	\label{T1}
	
\ref{T1}
~~~
- 参考文献
~~~
bibtex格式引用放在.bib文件中
\cite{} 直接引用
\citep{} 间接引用
~~~
- 字体大小
~~~
Command     Nominal Point Size      Exact Point Size
\tiny               5                       5
\scriptsize         7                       7
\footnotesize       8                       8
\small              9                       9
\normalsize        10                      10
\large             12                      12
\Large             14                   14.40
\LARGE             18                   17.28
\huge              20                   20.74
\Huge              24                   24.88
~~~
- 文本字体
~~~
\englishbf{英文加粗} （本模版自设）
\textbf{加粗}
\emph{斜体}
~~~
- 添加斜杠
~~~
\usepackage{diagbox}

~~~
- 引用python语法（提前加入配置文件）
~~~
\begin{python}

\end{python}
~~~
- 脚注
~~~
\footnote{}
~~~
- 插入超链接
~~~
\href{网址}{显示文字}
~~~

模板还有很多不足之处待改进，欢迎大家在issue里提问。
