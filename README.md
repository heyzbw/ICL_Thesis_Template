# 帝国理工学院 LaTex模板
> Imperial College London LaTex Template

> 搭配中文注释，更适合中国宝宝体质

## 使用指南
- `main.tex`为主源文件，使用模板时编译此文件
- `cover.tex`编辑论文封面
- `abstract.tex`编辑论文标题与中英文的摘要
- `body.tex`编辑论文正文（包括结束语）
- `appendix.tex`编辑论文附录
- 文件夹`reference`存放文献数据库`thesis.bib`文件
- 文件夹`picture`存放论文中引用的图片
- 模板编译效果见<a href="main.pdf" target="_blank">main.pdf</a>

## LaTex常见语法记录
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

## 致谢
- 文件整体在[CSU LaTex模板](https://github.com/heyzbw/CSU_Thesis_Template)的基础上修改，做了相应的英文和风格适配。

- 参考文献格式文件`dcu.bst`来源于：[Harvard引用格式](https://ctan.org/tex-archive/macros/latex/contrib/harvard)

- Python引用格式文件`pythonhighlight.sty`来源于GitHub项目：[python-latex-highlighting](https://github.com/olivierverdier/python-latex-highlighting)
