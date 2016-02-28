# ModernPhysicsExperiment_PKU

A latex template for modern physics experiment at school of physics, Peking University

请用 xelatex 编译

请用 UTF-8 编码文件

不需要下载 evtex4-1

Edited and pushed to github by Liang Hao (mail: haoliang@pku.edu.cn), 2016.02.28

Remove documentclass "revtex4.1", using "article"

Change "CJK" to "xeCJK"

And change a lot of things that relate to it.

Test with texlive 2015 in windows 10 and Ubuntu 15.10

$xelatex XX.tex






----------2014年Readme----------

由于一年中，各种收到使用win7+winEdt7+ctex用户的报错反馈，这里应荀坤老师要求，重发一份Readme.
由于大家的报错太多，而且杂乱无章，几乎全部我当场就解决了，于是就没有留下报错备案. 今天看来，这对重写Readme是件不利的事情.
但是我也是有win7的，我可以重新模拟大家面临的处境，于是这里就重发一份在我的模拟上编译成功的东西：

mpltx_win7.tex

编码：unicode (notepad菜单>文件>另存为>文件编码:unicode,文件类型:所有文件*.*)
EOL码：0x0D 0x0A (dos,windows)
使用编译命令：xelatex （顶菜单>Tex>Pdf>XeLaTeX）
去掉水印：见69-71行注释

Q:revtex4-1下载后怎么办？
A:看revtex4-1的Readme，按指导做就好.

Q:\maketitle 报错
A:pdflatex对这里使用的中文编码未兼容（我当时就是遇到这个问题才使用xelatex的），所以用xelatex吧

Q:哪个哪个包声明时出错
A:包冲突，这个在tex家族是家常便饭了，毕竟tex是宏替换机制，而各个包又是不同人写的，没有一个统一的规范，有冲突很正常.
但正常归正常，用户需要一个无冲突的结果. 这时候就要调试了，试试去掉新加的包与旧的包，或者通过换换前后顺序看报错的区分，就可以定位出是哪两个包出了问题，然后可能有交换顺序后就可以使用了的可能，如果还不行，使用RequirePackage的做法.
如果自己的尝试归于无果，且如果这个包还很受欢迎，那么网上一定有人遇到同样的问题的，搜索一下，就能知道解决方案.

为了向大家说明在实际使用中，这个模板是完美的，我就用了去年的两个报告作例子。这两个报告(STM,SiHall的tex文件)有图，有minipage，有表格，所以一般需求没有问题了.
不过大家在实验中还是要独立思考，往年的报告会有错误是很正常的. 科研中还经常看到同一期刊发片Re:什么什么的文章批评以前什么什么文章的内容是错的呢.

孙思白于北大写
2014年03月06日

----------2013年Readme----------

此模板来自APS Journals, 由曹传午同学分享至人人网，经孙思白同学修改完善传至近代物理实验教学组，供同学们参考。

文件说明：
  mpltx.tex 核心文件，替换里面的中文内容来书写自己的报告。
  mpltx_dos.tex 给Windows用户看的。用notepad(记事本)打开。
  Gax.png|Gax.eps 两幅图，编译示例文件时有用到。
  mpltx.pdf 示例编译结果，测试环境：Ubuntu 12.04, TeXLive 2012

孙思白:
“考虑到实验数据现今大多以数字形式读出和处理，转化为Word时往往受到Microsoft公司产品的种种限制。
  为了方便熟悉LaTeX的同学的报告写作，同时也是为我自己写作方便，我于2013年03月06日写下了这个模板：
  MpLtX --- a LaTeX Template for Modern Physics Lab. 
  这个模板依赖于APS Journals的revtex4-1包，由曹传午同学将原始草稿传至人人网，
  我将其修改完善并debug形成了这个模板。希望能被教学组采纳并公布到tcep网站上。

  关于revtex4-1由http://publish.aps.org/revtex/revtex-faq下载。
  编译这个tex文件需要ctex包，可以从http://www.ctex.org/HomePage下载，然后用xelatex命令编译。
  这个文件开头注释声明了文件的信息，若老师们觉得哪有不妥的可以任意修改。
  我很希望这个文件能被大家认可，也很欢迎其他同学和老师对这个模板进行再次修改。”

Q&A:

Q: 我用CTeX附带的WinEdit打开模板，结果里面的中文都成了乱码。
A: 这个是由于文本编码不匹配造成的。WinEdit默认是国标码GB系列，而我传上来的是UTF8国际编码，所以只要用notepad打开，另存为，编码选项选GB系列任一种(如GBK)就可以了。（我的WinEdt很奇怪，要选Unicode才行，选ANSI不行）
   此外，Windows/Dos的换行符是0x0D 0x0A，而linux/Unix的换行符是0x0A，于是在notepad中显示不出换行，这点不用担心。

Q: 对于linux用户，安装TeXLive后应该是包含ctex宏包的。但是经xelatex编译后，CJK环境中仍没有中文显示。
A: 这个往往是由于字体未设置造成的。TeXLive不默认安装中易字体。关于如何安装中易字体并修补TeXLive的CTeX宏包，请移步http://blog.csdn.net/ustc_dylan/article/details/6196129

Q: 为什么\\的换行不会缩进两格？
A: 要缩进两格的换行请用\par，这个是CTeX的用法。
