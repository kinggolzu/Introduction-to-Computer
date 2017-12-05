附录一：Markdown 使用教程
---
>作者:[李雪](mailto:www.565284368@qq.com)

## 写在前面

Markdown是为那些经常需要码字，文字排版，对文字排版，和排版有要求的人员设计的，甚至从头到尾都不需要使用鼠标。

## Markdown的基本语法

###### **1.分级标题**

输入相应的“#”个数代表几级标题，依次有不同的字体大小，其中“#”后面最好有一个空格。
```
# 一级标题

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题
```

###### **2.加粗，斜体**

双"\*"包围表示加粗，单“\*”包围表示斜体。
```
**加粗**

*斜体*
```

###### **3.层次**

当我们在写读书笔记，论文的时候，内容结构有层次感很重要。

例如：

1. 第一节（1.后面最好有一个“空格”，会有一个格式的统一）

2. 第二节（你不用敲“2”，自动就有了）

1). 第一小节（这里的缩进可以使用空格，可以使用Tab键）

2). 第二小节



###### **4.插入图片**

点击菜单栏->插入图片(在[]里面添加图片的描述，在()里面添加图片的绝对路径，或者将图片保存在.MD文件所在文件夹中)

`![fig](\img\Figure 0.11.png)`

![fig](/assets/images/appendix/A/Figure 0.png)

###### **5.插入无序列表**

使用 *，+，- 表示无序列表。
```
- 无序列表项1

- 无序列表项2

    - 无序列表项2-1
```
- 无序列表项1

- 无序列表项2

    - 无序列表项2-1

###### **6.插入有序列表**

使用数字和点表示有序列表。

1. 有序列表项

2. 有序列表项

  2.1 有序列表项

  2.2 有序列表项

###### **7.插入文字引用**

用“>”表示文字引用
```
>好好学习，天天向上
```
>好好学习，天天向上

###### **8. 行内代码块**

使用 \`代码\` 表示行内代码块。
```
eg.让我们聊聊`Hello World`
```
eg.让我们聊聊`Hello World`

###### **9. 代码块**

使用 四个缩进空格或 \`\`\` 包围表示代码块。

```

#include<stdio.h>

int main()

{

	printf("hello world!\n");

	return 1;

}

```

## Markdown的高阶语法

###### 1.标签

在编辑区任意行的列首位置输入以下代码给文稿标签：

标签：Markdown

###### 2.删除线

使用 ~~ 包围表示删除线。

`` ~~这是一段错误的文本~~ ``

~~这是一段错误的文本~~

###### 3.注脚

使用 [^keyword] 表示注脚。

###### 4.行内公式

\$数学公式\$，或是最原始的\$\$\$数学公式\$\$\$

**例子：**

行内公式：

` $ \Gamma(n) = (n-1)!\quad\forall n\in\mathbb N $ `

$$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$$


###### 5.行间公式

`$$数学公式$$`

**例子：**

`$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$`

$$x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$



###### 6.上标和下标

^表示上标，\_表示下标。如果上下标的内容多于一个字符，要用{}把这些内容括起来当成一个整体。上下标是**可以嵌套的**，也可以同时使用。

例子：

`$$x^{y^z}=(1+e^x)^{-2xy^w}$$`

$$x^{y^z}=(1+e^x)^{-2xy^w}$$



###### 7.分数表示

###### 方法1：\frac{分子}{分母}

`$$\frac{a+b}{c+d}$$`

$$\frac{a+b}{c+d}$$

###### 方法2：分子 \over 分母

`$$1 \over 3$$`

$$1 \over 3$$

###### 8.插入表格

按照如下格式输入，可以生成表格。
```
| 项目        | 价格   |  数量  |

| --------   | -----:  | :----:  |

| 计算机     | \$1600 |   5     |

| 手机        |   \$12   |   12   |

| 管线        |    \$1    |  234  |
```


| 项目        | 价格   |  数量  |

| --------   | -----:  | :----:  |

| 计算机     | \$1600 |   5     |

| 手机        |   \$12   |   12   |

| 管线        |    \$1    |  234  |

###### 9.括号

()、[]和|可以直接表示自己，而{}本来用于分组，因此需要用{}来表示自身，也可以使用\lbrace 和\rbrace来表示。

**例子：**

按照如下格式输入，可以生成相应的式子。

`$$\{[z-(1+\frac23x)y]\div 4\}$$`

$$\{[z-(1+\frac23x)y]\div 4\}$$



**注意：**原始符号并不会随着公式大小缩放。有时候我们想要括号和分隔符显示的大点，比如上面例子中希望括号能把整个分数都包住，那么可以用\left和\right标记，实现自适应调整。



**例子：**

按照如下格式输入，可以生成相应的式子。

`$$\left(1+\frac23x\right)$$`

$$\left(1+\frac23x\right)$$



**其他例子：**



方括号

按照如下格式输入，可以生成相应的式子。

`$$\left[\frac12\right]$$`

$$\left[\frac12\right]$$



大括号

按照如下格式输入，可以生成相应的式子。

`$$\left\{\frac12\right\}$$`

$$\left\{\frac12\right\}$$



尖括号

按照如下格式输入，可以生成相应的式子。

`$$\left\langle\frac12\right\rangle$$`

$$\left\langle\frac12\right\rangle$$

向上取整

按照如下格式输入，可以生成相应的式子。

`$$\left\lceil\frac12\right\rceil$$`

$$\left\lceil\frac12\right\rceil$$



向下取整

按照如下格式输入，可以生成相应的式子。

`$$\left\lfloor\frac12\right\rfloor$$`

$$\left\lfloor\frac12\right\rfloor$$


**注意：**\left和\right标记必须是成对出现的，但有时候我们只用到其中一个，比如只用一个|当作分割线，这时候可以通过.来表示空的那一方，即用\left.表达左边空的情况，用\right.表达右边空的情况。


**例子：**

按照如下格式输入，可以生成相应的式子。

`$$\left. \frac{du}{dx} \right| _{x=0}$$`

$$\left. \frac{du}{dx} \right| _{x=0}$$

###### 10 根号表示

根号开方使用\sqrt标记，语法格式如下：

`\sqrt[开方次数，默认为2]{开方因子}`

**例子：**

按照如下格式输入，可以生成相应的式子。

`$$\sqrt{x^3}$$　和　$$\sqrt[3]{\frac xy}$$`

$$\sqrt{x^3}$$　和　$$\sqrt[3]{\frac xy}$$



按照如下格式输入，可以生成相应的式子。

```
$$

\sqrt{3x-1}+(1+x)^2

$$
```

$$

\sqrt{3x-1}+(1+x)^2

$$

###### 11 Diagram

以3个“~”+mermaid开头，以3个“~”结束，其中TD表示从上向下绘制,LR表示从上向下绘制。

```
~~~mermaid

graph TD;

	A-->B;

	A-->C;

	B-->D;

	C-->D;

~~~
```

~~~mermaid

graph TD;

	A-->B;

	A-->C;

	B-->D;

	C-->D;

~~~


###### 12.链接

Markdown中有两种方式，实现链接，分别为内联方式和引用方式。

```
内联方式：This is an [example link](http://example.com/).

引用方式：
I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
```

内联方式：This is an [example link](http://example.com/).

引用方式：

I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].



###### 13.插入视频

目前Markdown只支持HTML的video标签。

```html
<video id="video" controls="" preload="none" poster="http://media.w3.org/2010/05/sintel/poster.png">

      <source id="mp4" src="http://media.w3.org/2010/05/sintel/trailer.mp4" type="video/mp4">

      <source id="webm" src="http://media.w3.org/2010/05/sintel/trailer.webm" type="video/webm">

      <source id="ogv" src="http://media.w3.org/2010/05/sintel/trailer.ogv" type="video/ogg">

      <p>Your user agent does not support the HTML5 Video element.</p>

</video>
```

<video id="video" controls="" preload="none" poster="http://media.w3.org/2010/05/sintel/poster.png">

      <source id="mp4" src="http://media.w3.org/2010/05/sintel/trailer.mp4" type="video/mp4">

      <source id="webm" src="http://media.w3.org/2010/05/sintel/trailer.webm" type="video/webm">

      <source id="ogv" src="http://media.w3.org/2010/05/sintel/trailer.ogv" type="video/ogg">

      <p>Your user agent does not support the HTML5 Video element.</p>

</video>



 到这里，Markdown 的基本语法在日常的使用中基本就没什么大问题了，只要多加练习，配合好用的工具，写起东西来肯定会行云流水。
<p style="text-align: right;">联系方式：周庆国,<img src="/assets/biaozhi.png" style="width: 15px;height: 15px;">zhouqg@lzu.edu.cn<p>

