## 第一章 GitHub和GitBook How to

本章包含的内容：

【崔玉贵】（cuiyg14@lzu.edu.cn）
1. Git（参考资料：）
    1. Git简介

Git是一款免费、开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。  Git的读音为\/gɪt\/。
Git是一个开源的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理。Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。
Torvalds 开始着手开发 Git 是为了作为一种过渡方案来替代 BitKeeper，后者之前一直是 Linux 内核开发人员在全球使用的主要源代码工具。开放源码社区中的有些人觉得BitKeeper 的许可证并不适合开放源码社区的工作，因此 Torvalds 决定着手研究许可证更为灵活的版本控制系统。尽管最初 Git 的开发是为了辅助 Linux 内核开发的过程，但是我们已经发现在很多其他自由软件项目中也使用了 Git。例如 很多 Freedesktop 的项目迁移到了 Git 上
    

2. 在你的电脑上使用Git（至少包含Windows平台，如果有其他操作系统则可以写上）
   

 3. Git基础（至少讲清楚clone、add、commit、push、pull）

 BLOBS
BLOB代表二进制大对象。为代表 blob文件的每个版本。一个blob保存文件数据，但不包含任何有关文件的元数据。它是一个二进制文件，该文件它被命名为SHA1哈希 Git数据库中。在Git中，文件未提及的名字。一切固定内容寻址。

Tree
树是一个对象，它表示一个目录。它拥有blobs以及其他子目录。一棵树是一个二进制文件，该文件存储Blob树，也被命名为树对象的SHA1哈希的引用。

Commit
提交持有的库的当前状态。COMMIT命令同样由SHA1哈希的名字命名。可以考虑commit对象的链表节点。每个提交的对象有父commit 对象的指针。从给定的承诺可以遍历寻找在父指针，查看历史记录的提交。如果提交多个父承诺，这意味着特定的提交是由两个分支合并。

BRANCHES
分支用来创建另一条线的发展。默认情况下，Git的主分支，这是一样躯干颠覆。平时要工作的新功能创建一个分支。功能完成后，它被合并回master分支，我们删除分支。每个分支所引用HEAD，这点在分支的最新提交。每当做出了一个提交，HEAD更新为最新提交。

TAGS
包括特定版本库中的标签分配一个有意义的名称。标签是非常相似的分支，但不同的是，标签是不可改变的。手段标记的一个分支，没有人打算修改。一旦标签被创建为特定的提交，即使创建一个新的提交，也不会被更新。通常开发人员创建标签的产品发布。

CLONE
克隆操作的库创建实例。克隆操作不仅检出的工作拷贝，但它也反映了完整的信息库。用户可以执行许多操作，这个本地仓库。网络介入是唯一的一次，当正在同步资料库实例。

PULL
Pull操作复制的变化，本地的一个实例来从远程仓库。Pull操作是用于两个存储库实例之间的同步。这是在Subversion更新操作一样。

PUSH
推动从本地存储库实例的远程操作副本的变化。这是用来储存到Git仓库中永久改变。这是在Subversion的提交操作相同。

HEAD
HEAD指针总是指向分支的最新提交。每当你做出了一个提交，HEAD更新为最新提交。HEAD树枝存储在.git\/refs\/heads\/ 目录中。

\[CentOS\]$ ls -1 .git\/refs\/heads\/
master

\[CentOS\]$ cat .git\/refs\/heads\/master
570837e7d58fa4bccd86cb575d884502188b0c49
REVISION
修订版本的源代码。在Git修订代表的提交。这些提交由SHA1安全哈希值确定。

URL
URL代表的Git仓库的位置。 Git 的URL存储在配置文件中。

\[tom@CentOS tom\_repo\]$ pwd
\/home\/tom\/tom\_repo

\[tom@CentOS tom\_repo\]$ cat .git\/config
\[core\]
repositoryformatversion = 0
filemode = true
bare = false
logallrefupdates = true
\[remote "origin"\]
url = gituser@git.server.com:project.git
fetch = +refs\/heads\/\*:refs\/remotes\/origin\/\*




【崔玉贵】（cuiyg14@lzu.edu.cn）

2. GitHub（参考资料：[https:\/\/help.github.com](https://help.github.com)）
    1. GitHub注册

搜索github进入官网\/填写昵称（用户名）、注册邮箱和密码\/昵称一栏，每次在你输入昵称之后，都会检查是否已经被注册。如果被注册了，那么会提示Username is already taken。此时请换另一个昵称进行注册。\/这时会弹出一个界面，让你选择你的私人计划（personal plan），即选择免费用户还是付费用户。付费用户可以拥有私人代码仓库（repos），即别人不能查看你的代码。免费用户的仓库都是公开的，任何人都能查看。
这里我们选择免费用户就可以了。默认的FREE后面Chosen按钮已经是选中状态了。如果你想成为付费用户，那么点击上面的Chosen按钮。
第二个红箭头前面的单选框是可选的，打不打勾都可以，最后我们点击右下角的绿色按钮Finish sign up来完成注册
    

2. GitHub的使用（建立仓库，clone仓库，同步仓库）

登陆你的Github账户，点击上方导航栏的“+”按钮，在下方选择“New  repository”\/
    3. 什么是Fork和，如何使用

Forking工作流 这种工作流不是使用单个服务端仓库作为『中央』代码基线，而让各个开发者都有一个服务端仓库。 这意味着各个代码贡献者有2个Git仓库而不是1个：一个本地私有的，另一个服务端公开的。
Forking工作流的一个主要优势是，贡献的代码可以被集成，而不需要所有人都能push代码到仅有的中央仓库中。 开发者push到自己的服务端仓库，而只有项目维护者才能push到正式仓库。 这样项目维护者可以接受任何开发者的提交，但无需给他正式代码库的写权限。
效果就是一个分布式的工作流，能为大型、自发性的团队（包括了不受信的第三方）提供灵活的方式来安全的协作。 也让这个工作流成为开源项目的理想工作流。

Pull requests let you tell others about changes you've pushed to a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before the changes are merged into the repository.


3. GitBook（参考资料：[https:\/\/help.gitbook.com\/](https://help.gitbook.com/)）
    1. 什么是GitBook

GitBook 是一个基于 Node.js 的命令行工具，可使用 Github\/Git 和 Markdown 来制作精美的电子书，GitBook 并非关于 Git 的教程。
    2. GitBook注册

下载并安装GitBook客户端然后输入邮箱用户名，设置密码，验证邮箱后即可

    3. 如何创建一本书

创建一个新的仓库![](/assets/1.png)

创建一个新文件，名为SUMMARY.md，里面填入：

\# Summary
\* \[前言\]\(README.md\)

![](/assets/2.png)
    

4. 如何使用GitBook编辑器
    5. 以不同的形式阅读一本书（网页、PDF等）
    6. 什么是Markdown

Markdown 是一种轻量级标记语言，创始人为约翰·格鲁伯（John Gruber）和亚伦·斯沃茨（Aaron Swartz）。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML\(或者HTML\)文档”。这种语言吸收了很多在电子邮件中已有的纯文本标记的特性。
Markdown同时还是一个由Gruber编写的Perl脚本：Markdown.pl。它把用markdown语法编写的内容转换成有效的、结构良好的XHTML或HTML内容，并将左尖括号\('&lt;'\)和&号替换成它们各自的字符实体引用。它可以用作单独的脚本，Blosxom和Movable Type的插件又或者BBEdit的文本过滤器.
Markdown也已经被其他人用Perl和别的编程语言重新实现，其中一个Perl模块放在了CPAN\(Text::Markdown\)上。它基于一个BSD风格的许可证分发并可以作为几个内容管理系统的插件。
    7. Markdown基础语法

1. 标题设置（让字体变大，和word的标题意思一样）
在Markdown当中设置标题，有两种方式：
第一种：通过在文字下方添加“=”和“-”，他们分别表示一级标题和二级标题。
第二种：在文字开头加上 “\#”，通过“\#”数量表示几级标题。（一共只有1~6级标题，1级标题字体最大）

2. 块注释（blockquote）
通过在文字开头添加“&gt;”表示块注释。（当&gt;和文字之间添加五个blank时，块注释的文字会有变化。）

3. 斜体
将需要设置为斜体的文字两端使用1个“\*”或者“\_”夹起来

4. 粗体
将需要设置为斜体的文字两端使用2个“\*”或者“\_”夹起来

5. 无序列表
在文字开头添加\(\*, +, and -\)实现无序列表。但是要注意在\(\*, +, and -\)和文字之间需要添加空格。（建议：一个文档中只是用一种无序列表的表示方式）

6. 有序列表
使用数字后面跟上句号。（还要有空格）

7. 链接（Links）
Markdown中有两种方式，实现链接，分别为内联方式和引用方式。
内联方式：This is an \[example link\]\(http:\/\/example.com\/\).
引用方式：
I get 10 times more traffic from \[Google\]\[1\] than from \[Yahoo\]\[2\] or \[MSN\]\[3\].  

\[1\]: http:\/\/google.com\/        "Google" 
\[2\]: http:\/\/search.yahoo.com\/  "Yahoo Search" 
\[3\]: http:\/\/search.msn.com\/    "MSN Search"
 

8. 图片（Images）
图片的处理方式和链接的处理方式，非常的类似。
内联方式：!\[alt text\]\(\/path\/to\/img.jpg "Title"\)
引用方式：
!\[alt text\]\[id\] 

\[id\]: \/path\/to\/img.jpg "Title"

9. 代码（HTML中所谓的Code）
实现方式有两种：
第一种：简单文字出现一个代码框。使用\`&lt;blockquote&gt;\`。（\`不是单引号而是左上角的ESC下面~中的\`）
第二种：大片文字需要实现代码框。使用Tab和四个空格。

10. 脚注（footnote）
实现方式如下：
hello\[^hello\]


\[^hello\]: hi

11. 下划线
在空白行下方添加三条“-”横线。（前面讲过在文字下方添加“-”，实现的2级标题）


4. Git、GitHub和GitBook三者的关系与异同

git是一个版本控制工具
github是一个用git做版本控制的项目托管平台。

git是一种版本控制系统。跟svn、cvs是同级的概念。
github是一个网站，给用户提供git服务。这样你就不用自己部署git系统，直接用注册个账号，用他们提供的git服务就可以。

GitBook 是一个基于 Node.js 的命令行工具，可使用 Github\/Git 和 Markdown 来制作精美的电子书，GitBook 并非关于 Git 的教程。

通俗点来说，就是一个项目或者说工程有多个人一起干，这个项目里每个人都有可能都拿同一文件了来编辑，但是这就产生了问题，到底怎么协同项目里面的人的所编辑的文件，怎么更新项目呢？这时就有了像git（版本控制工具）这样的东西了来做这种事情，github就相当于项目放置的平台（不过它里面有很多的不同的开源项目（往往是很多人协同开发的）罢了， 借助git来管理，相对于git本地仓库来说，它是一个远程仓库）。

作者：周国成
链接：https:\/\/www.zhihu.com\/question\/21907548\/answer\/32239242
来源：知乎
著作权归作者所有，转载请联系作者获得授权。


![](/assets/4.jpg)

可以使用搜索引擎等任何方式查找相关资料，实践、总结并完成相关内容

**在每一节开头注明本节起草人和审阅人并附上其邮箱，如：**

```
起草人：[张三](mailto:example@mail.com)
审阅人：[李四](mailto:example@mail.com)
```

格式参考[https:\/\/www.gitbook.com\/book\/kinggolzu\/introduction-to-computer\/details](https://www.gitbook.com/book/kinggolzu/introduction-to-computer/details)

