# Markdown公式、符号总结
- [Markdown公式、符号总结](#markdown公式符号总结)
  - [常见公式](#常见公式)
    - [1、向量公式](#1向量公式)
    - [2、分段函数](#2分段函数)
    - [3、多行表达公式](#3多行表达公式)
  - [常见公式环境](#常见公式环境)
  - [公式编辑的编号设置](#公式编辑的编号设置)
  - [矩阵](#矩阵)
    - [1、不带括号的矩阵](#1不带括号的矩阵)
    - [2、带小括号的矩阵](#2带小括号的矩阵)
    - [3、带中括号的矩阵](#3带中括号的矩阵)
    - [4、带大括号的矩阵](#4带大括号的矩阵)
    - [5、带省略号的矩阵](#5带省略号的矩阵)
    - [6、带横线/竖线分割的矩阵：](#6带横线竖线分割的矩阵)
  - [上下标符号](#上下标符号)
  - [括号](#括号)
  - [分式与根式](#分式与根式)
  - [开方](#开方)
  - [累加/累乘](#累加累乘)
  - [三角函数](#三角函数)
  - [对数函数](#对数函数)


## <a id="t1"></a><a id="_1"></a>常见公式

一般公式分为两种形式，行内公式和行间公式。==行内公式==是在公式代码块的前后均添加一个`$` ；==行间公式==则是在公式代码块的前后均添加两个`$$` 。

**数学算式：**  
（1）行内公式：$\Gamma(z)=\int_0^\infty t^{z-1}e^{-t}dt\,.$
（2）行间公式：  
$$\Gamma(z)=\int_0^\infty t^{z-1}e^{-t}dt\,.$$
.  
**Markdown公式：**

```
$ \Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,. $ 
$$\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.$$
```

**公式排列：一般使用`\binom{a}{b}`或者`{a \choose b}`实现对 a , b两个公式的排列。**

**数学算式**  
$$\binom{n+1}{2k} $$
**Markdown公式：**

```
$$\binom{n+1}{2k} $$
```

**数学算式：**  
$${n+1 \choose 2k} $$
**Markdown公式：**

```
$${n+1 \choose 2k} $$
```

### <a id="t2"></a><a id="1_35"></a>1、向量公式

**向量表示：** 使用`\mathbf{x}`来表示向量 $\mathbf{x}$ 

**数学算式：**  
$$f(\mathbf{x})=\mathbf{w}^T\mathbf{x}$$
**Markdown公式：**

```
$$f(\mathbf{x})=\mathbf{w}^T\mathbf{x}$$
```

### <a id="t3"></a><a id="2_46"></a>2、分段函数

定义函数的时候经常需要分情况给出表达式，使用 `{…`。其中：  
（1）使用`\` 来==分隔分组==；  
（2）使用`&` 来==指示需要对齐的位置==；  
（3）使用`\ + 空格`来表示==空格==；  
（4）如果要使==分类之间的垂直间隔变大==，可以使用`\[2ex]` 代替`\` 来分隔不同的情况。(`3ex,4ex` 也可以用，`1ex` 相当于原始距离）。

**数学算式：**

分段函数  

$$ y= \begin{cases} -x,\quad x\leq 0\\ x, \quad x>0 \end{cases} \tag{1} 
$$

(1)

**Markdown公式：**

```
#分段函数 
$$
y= 
\begin{cases}
-x,\quad x\leq 0\\ 
x, \quad x>0
\end{cases}
\tag{1}
$$
```

方程组  
$$ \left\{  \begin{array}{c}     a_1x+b_1y+c_1z=d_1 \\      a_2x+b_2y+c_2z=d_2 \\      a_3x+b_3y+c_3z=d_3 \end{array} \right.  $$
```
# 方程组 
$$ 
\left\{  
\begin{array}{c}     
a_1x+b_1y+c_1z=d_1 \\      a_2x+b_2y+c_2z=d_2 \\      a_3x+b_3y+c_3z=d_3 
\end{array} 
\right.  
$$
```

$$
u(x)=
\begin{cases}
\exp x &\quad \text{if}	\ x\geq 0\\
1 		  & \quad \text{if x < 0}&
\end{cases}
$$

  
均方误差  

 $$ J(\theta) = \frac{1}{2m}\sum_{i = 0} ^m(y^i - h_\theta (x^i))^2 $$
```
# 均方误差 
$$ 
J(\theta) = \frac{1}{2m}\sum_{i = 0} ^m(y^i - h_\theta (x^i))^2 
$$
```

批量梯度下降  
$$ \frac{\partial J(\theta)}{\partial\theta_j}=-\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i))x^i_j  $$

```
# 批量梯度下降
$$ 
\frac{\partial J(\theta)}{\partial\theta_j}=-\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i))x^i_j  
$$
```

推导过程  

$$
\begin{aligned} \frac{\partial J(\theta)}{\partial\theta_j} & = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(y^i-h_\theta(x^i)) \\ & = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(\sum_{j=0}^n\theta_jx_j^i-y^i) \\ & = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i))x^i_j \end{aligned}
$$ 

```
# 推导过程 
$$ \begin{aligned} 
\frac{\partial J(\theta)}{\partial\theta_j} 
& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(y^i-h_\theta(x^i)) \\ 
& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(\sum_{j=0}^n\theta_jx_j^i-y^i) \\ 
& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i))x^i_j 
\end{aligned} $$
```

case环境的使用  
$$ a =    \begin{cases}      \int x\, \mathrm{d} x\\      b^2    \end{cases} $$

```
# case环境的使用 
$$
a =    
	\begin{cases}      
		\int x\, \mathrm{d} x\\
		b^2    
	\end{cases} 
$$
```

带方框的等式  
$$
\begin{aligned} \boxed{x^2+y^2 = z^2} \end{aligned}
$$ 
```
# 带方框的等式 
$$ 
\begin{aligned}  
	\boxed{x^2+y^2 = z^2} 
\end{aligned}
$$
```

最大（最小）操作符  
$$
\begin{gathered} \operatorname{arg\,max}_a f(a) = \operatorname*{arg\,max}_b f(b) \\ \operatorname{arg\,min}_c f(c) = \operatorname*{arg\,min}_d f(d) \end{gathered}
$$ 

```
$$ 
\begin{gathered} 
\operatorname{arg\,max}_a f(a)   
= \operatorname*{arg\,max}_b f(b) \\ 
\operatorname{arg\,min}_c f(c) 
= \operatorname*{arg\,min}_d f(d) 
\end{gathered} 
$$
```

求极限  
$$ \begin{aligned}   \lim_{a\to \infty} \tfrac{1}{a} \end{aligned} $$ 

$$ \begin{aligned}    \lim\nolimits_{a\to \infty} \tfrac{1}{a} \end{aligned} $$

```
$$ 
\begin{aligned}   
	\lim_{a\to \infty} \tfrac{1}{a} \end{aligned} 
$$ 
$$ 
\begin{aligned}    
	\lim\nolimits_{a\to \infty} \tfrac{1}{a} 
\end{aligned} 
$$
```

求积分  
$$
\begin{aligned} \int_a^b x^2 \mathrm{d} x \end{aligned}
$$ 
$$
\begin{aligned} \int\limits_a^b x^2 \mathrm{d} x \end{aligned}
$$ 

```
$$
\begin{aligned}    
	\int_a^b x^2  \mathrm{d} x \end{aligned}
$$
$$
\begin{aligned} 
	\int\limits_a^b x^2  \mathrm{d} x \end{aligned} 
$$
```

使用`\[2ex]` 代替`\` 使分组的垂直间隔增大。

**数学算式：**  

$$ y= \begin{cases} -x,\quad x\leq 0 \\[2ex] x, \quad x>0 \end{cases} \tag{1} $$
**Markdown公式：**

```
$$ y= 
\begin{cases} 
-x,\quad x\leq 0 \\[2ex] 
x, \quad x>0 
\end{cases} 
\tag{1} 
$$
```

### <a id="t4"></a><a id="3_280"></a>3、多行表达公式

有时候需要将一行公式分多行进行显示，其中`\begin{aligned}` 表示==开始方程==，`\end{equation}` 表示==方程结束==；使用`\\`表示==公式换行==。\\begin{gather}表示环境设置。，`&` 表示==对齐的位置==。

**数学算式：**  
$$
\begin{aligned} J(\mathbf{w})&=\frac{1}{2m}\sum_{i=1}^m(f(\mathbf{x_i})-y_i)^2\\ &=\frac{1}{2m}\sum_{i=1}^m [f(\mathbf{x_i})]^2-2f(\mathbf{x_i)}y_i+y_i^2 \end{aligned}
$$ 
**Markdown公式：**

```
$$
\begin{aligned} 
J(\mathbf{w})&=\frac{1}{2m}\sum_{i=1}^m(f(\mathbf{x_i})-y_i)^2\\ 
&=\frac{1}{2m}\sum_{i=1}^m [f(\mathbf{x_i})]^2-2f(\mathbf{x_i)}y_i+y_i^2 
\end{aligned} 
$$
```

## <a id="t5"></a><a id="_302"></a>常见公式环境

| 环境名称 | 释义  |
| --- | --- |
| align | 最基本的对齐环境 |
| multline | 非对齐环境 |
| gather | 无对齐的连续方程 |

> gathered 允许多行（多组）方程式在彼此之下设置并分配单个方程式编号  
> split 与align \*类似，但在另一个显示的数学环境中使用  
> aligned 与align类似，可以在其他数学环境中使用。  
> alignedat 与alignat类似，同样需要一个额外的参数来指定要设置的方程列数。

**备注：** 如果各个方程需要==在某个字符处对齐（如等号对齐），只需在所有要对齐的字符前加上 `&` 符号==。

**数学算式：**  
$$
\begin{aligned}  
	\left.\begin{aligned}         
		B'&=-\partial \times E,\\       
		E'&=\partial \times B - 4\pi j,       
		\end{aligned}  
	\right\}								
	\qquad \text{Maxwell's equations} \end{aligned}
$$ 
$$ 
\begin{aligned}  \sigma_1 &= x + y  &\quad \sigma_2 &= \frac{x}{y} \\	  \sigma_1' &= \frac{\partial x + y}{\partial x} & \sigma_2'      &= \frac{\partial \frac{x}{y}}{\partial x} \end{aligned}
$$  
$$
\begin{aligned} a_n&=\frac{1}{\pi}\int\limits_{-\pi}^{\pi}f(x)\cos nx\,\mathrm{d}x\\ &=\frac{1}{\pi}\int\limits_{-\pi}^{\pi}x^2\cos nx\,\mathrm{d}x\\[6pt] \end{aligned} 
$$
$$
\begin{aligned} 
J(\mathbf{θ})=-\frac{1}{m}∑_{i=1}^{m}y_ilogh_θ(x_i)+(1−y_i)log(1−h_θ(x_i)) 
\end{aligned} 
$$
```
$$
\begin{aligned} 
J(\mathbf{θ})=-\frac{1}{m}∑_{i=1}^{m}y_ilogh_θ(x_i)+(1−y_i)log(1−h_θ(x_i)) 
\end{aligned} 
$$
```
**Markdown公式：**
```
$$ 
\begin{aligned}  
	\left.\begin{aligned}         
		B'&=-\partial \times E,\\         
		E'&=\partial \times B - 4\pi j, 
		\end{aligned}  
	\right\}							
	\qquad \text{Maxwell's equations}
\end{aligned} 
$$

$$ 
\begin{aligned}
	\sigma_1 &= x + y  &\quad \sigma_2 &= \frac{x}{y} \\	  
	\sigma_1' &= \frac{\partial x + y}{\partial x} & \sigma_2' 
		&= \frac{\partial \frac{x}{y}}{\partial x}
\end{aligned}
$$

$$
\begin{aligned}
a_n&=\frac{1}{\pi}\int\limits_{-\pi}^{\pi}f(x)\cos nx\,\mathrm{d}x\\ &=\frac{1}{\pi}\int\limits_{-\pi}^{\pi}x^2\cos nx\,\mathrm{d}x\\[6pt] 
\end{aligned}
$$
```

## <a id="t6"></a><a id="_385"></a>公式编辑的编号设置

| 符号  | 功能  |
| --- | --- |
| \\tag{标号} | 公式宏包序号设置命令，可用于带星号公式环境中的公式行 |
| \\tag\*{标号} | 作用与\\tag相同，只是标号两侧没有圆括号 |

**数学算式：**  
$$
x^2+y^2=z^2 \tag{1$'$} 
$$
$$ 
x^4+y^4=z^4 \tag{*}  
$$
$$ 
x^5+y^5=z^5 \tag*{*}
$$
$$ 
x^6+y^6=z^6 \tag{1-1}  
$$

**Markdown公式：**

```
$$
x^2+y^2=z^2 \tag{1$'$} 
$$
$$ 
x^4+y^4=z^4 \tag{*}  
$$
$$ 
x^5+y^5=z^5 \tag*{*}
$$
$$ 
x^6+y^6=z^6 \tag{1-1}  
$$
```

## <a id="t7"></a><a id="_420"></a>矩阵

**常见矩阵表现形式：**

**数学算式：**  
$$\begin{pmatrix}1 & 2 \\ 3 &4\\ \end{pmatrix}$$ 
$$\begin{bmatrix}1 & 2 \\ 3 & 4\\ \end{bmatrix}$$ 
$$\begin{Bmatrix}1 &2 \\ 3 & 4\\ \end{Bmatrix}$$ 
$$\begin{vmatrix}1 &2 \\ 3 &4\\ \end{vmatrix}$$ 
$$\begin{Vmatrix}1 &  2 \\ 3 &  4\\ \end{Vmatrix}$$ 
==元素省略==可以使用`\cdots` 表示⋯，`\ddots`表示⋱ ，`\vdots`表示⋮ ，从而省略矩阵中的元素，如：  
$$\begin{pmatrix}1&a_1&a_1^2&\cdots&a_1^n\\1&a_2&a_2^2&\cdots&a_2^n\\\vdots&\vdots&\vdots&\ddots&\vdots\\1&a_m&a_m^2&\cdots&a_m^n\\\end{pmatrix} $$

**Markdown公式：**

```
$$\begin{pmatrix}1 & 2 \\ 3 &4\\ \end{pmatrix}$$ 
$$\begin{bmatrix}1 & 2 \\ 3 & 4\\ \end{bmatrix}$$ 
$$\begin{Bmatrix}1 &2 \\ 3 & 4\\ \end{Bmatrix}$$
$$\begin{vmatrix}1 &2 \\ 3 &4\\ \end{vmatrix}$$
$$\begin{Vmatrix}1 &  2 \\ 3 &  4\\ \end{Vmatrix}$$ 
$$\begin{pmatrix}
1&a_1&a_1^2&\cdots&a_1^n\\
1&a_2&a_2^2&\cdots&a_2^n\\
\vdots&\vdots&\vdots&\ddots&\vdots\\
1&a_m&a_m^2&\cdots&a_m^n\\
\end{pmatrix} 
$$
```

**为公式添加脚注编号使用：`\tag{n}`,其中 n
表示第 n 个公式。**

### <a id="t8"></a><a id="1_448"></a>1、不带括号的矩阵

**数学算式：**  
$$
\begin{matrix} 
	1 & 2 & 3\\
	4 & 5 & 6 \\ 
	7 & 8 & 9 
\end{matrix} 
\tag{1} 
$$
**Markdown公式：**

```
$$
\begin{matrix} 
	1 & 2 & 3\\
	4 & 5 & 6 \\ 
	7 & 8 & 9 
\end{matrix} 
\tag{1} 
$$
```

### <a id="t9"></a><a id="2_470"></a>2、带小括号的矩阵

**数学算式：**  
$$
\left( 
	\begin{matrix} 
		1 & 2 & 3\\ 
		4 & 5 & 6 \\
		7 & 8 & 9 
	\end{matrix} 
\right) 
\tag{2} 
$$

**Markdown公式：**

```
$$
\left( 
	\begin{matrix} 
		1 & 2 & 3\\ 
		4 & 5 & 6 \\
		7 & 8 & 9 
	\end{matrix} 
\right) 
\tag{2} 
$$
```

### <a id="t10"></a><a id="3_494"></a>3、带中括号的矩阵

**数学算式：**  
$$
\left[ 
\begin{matrix}
	1 & 2 & 3\\ 
	4 & 5 & 6 \\
	7 & 8 & 9
\end{matrix} 
\right] 
\tag{3} 
$$
**Markdown公式：**

```
$$
\left[ 
\begin{matrix}
	1 & 2 & 3\\ 
	4 & 5 & 6 \\
	7 & 8 & 9
\end{matrix} 
\right] 
\tag{3} 
$$
```

### <a id="t11"></a><a id="4_518"></a>4、带大括号的矩阵

**数学算式：**  

**Markdown公式：**
$$
\left\{ 
\begin{matrix} 
	1 & 2 & 3\\ 
	4 & 5 & 6 \\ 
	7 & 8 & 9
\end{matrix}
\right\} 
\tag{4} 
$$

```
$$
\left\{ 
\begin{matrix} 
	1 & 2 & 3\\ 
	4 & 5 & 6 \\ 
	7 & 8 & 9
\end{matrix}
\right\} 
\tag{4} 
$$
```

### <a id="t12"></a><a id="5_541"></a>5、带省略号的矩阵

**数学算式：**  
$$ 
\left[ 
\begin{matrix}
	a & b & \cdots & a\\
	b & b & \cdots & b\\ 
	\vdots & \vdots & \ddots & \vdots\\
	c & c & \cdots & c 
\end{matrix}
\right] 
\tag{5} 
$$

**Markdown公式：**

```
$$ 
\left[ 
\begin{matrix}
	a & b & \cdots & a\\
	b & b & \cdots & b\\ 
	\vdots & \vdots & \ddots & \vdots\\
	c & c & \cdots & c 
\end{matrix}
\right] 
\tag{5} 
$$
```

### <a id="t13"></a><a id="6_569"></a>6、带横线/竖线分割的矩阵：

**数学算式：**  
$$
\left[ 
\begin{array}{c|cc} 
	1 & 2 & 3 \\ 
	4 & 5 & 6 \\
	7 & 8 & 9
\end{array}
\right] 
\tag{6}
$$

**Markdown公式：**

```
$$
\left[ 
\begin{array}{c|cc} 
	1 & 2 & 3 \\ 
	4 & 5 & 6 \\
	7 & 8 & 9
\end{array}
\right] 
\tag{6}
$$
```

**横线用 `\hline` 分割，示例如下：**

**数学算式：**  
$$
\left[
\begin{array}{c|cc}
	1 & 2 & 3 \\ 
	\hline 
	4 & 5 & 6 \\ 
	7 & 8 & 9 
\end{array}
\right]
\tag{7} 
$$

**Markdown公式：**

```
$$
\left[
\begin{array}{c|cc}
	1 & 2 & 3 \\ 
	\hline 
	4 & 5 & 6 \\ 
	7 & 8 & 9 
\end{array}
\right]
\tag{7} 
$$
```

## <a id="t14"></a><a id="_623"></a>上下标符号

默认情况下，上、下标符号仅仅对下一个组起作用。一个组即单个字符或者使用`{…}` 包裹起来的内容。

| 数学算式 | Markdown公式 | 核心语法 |
| :-: | :-: | :-: |
| $a_i ,a_{pre}$| a_i , a_{pre} | 下标使用`_` |
| $a^i , a^{pre}$| a^i , a^{pre} | 上标使用`^` |
| $\bar{a}$ | \bar{a} |     |
| $\acute{a}$ | \acute{a} |     |
| $\breve{a}$ | \breve{a} |     |
| $\grave{a}$ | \grave{a} |     |
| $\dot{a}$| \dot{a} |     |
| $\ddot{a}$| \\ddot{a} |     |
| $\dot {\dot x}$| \dot {\dot x} |     |
| $\hat{a}$| \hat{a} |     |
| $\widehat{xy}$| \widehat{xy} | 多字符可以使用 |
| $\check{a}$ | \check{a} |     |
| $\breve{a}$ | \breve{a} |     |
| $\tilde{a}$ | \tilde{a} |     |
| $\vec{a}$| \vec{a} | 矢量使用 `\vec{}` |
| $\overrightarrow {xy}$ | \overrightarrow {xy} | 向量  |
| $\overline{a + b + c + d}$| \overline{a + b + c + d} |     |
| $\underline{a + b + c + d}$| \underline{a + b + c + d} |     |
| $\overbrace{a + b + c + d}$| \overbrace{a + b + c + d} |     |
| $\underbrace{a + b + c + d}$| \underbrace{a + b + c + d} |     |
| $\overbrace{a + \underbrace{b + c}\_{1.0} + d}^{2.0}$| \overbrace{a + \underbrace{b + c}\_{1.0} + d}^{2.0} |     |

## <a id="t15"></a><a id="_650"></a>括号

小括号与方括号  
（1）使用原始的 \( \) ， \[ \] 到的括号大小是固定的，如 \( 2 + 3 \) \[ 4 + 4 \] \( 2 + 3 \) \[ 4 + 4 \] \( 2 + 3 \) \[ 4 + 4 \] \( 2 + 3 \)\[ 4 + 4 \]
（2）使用`\left(或\right)`可使括号大小与邻近的公式相适应（该语句适用于所有括号类型），如 $\left(\frac{x}{y}\right)$ 


| 数学算式 | Markdown公式 | 核心语法 |
| :-: | :-: | :-: |
| $( , )$| ( , ) |     |
| $[ , ]$| \[ , \] |     |
| $\lang,\rang$| \lang,\rang 或 \langle, \rangle |     |
|$\lvert, \rvert$ | \lvert, \rvert |     |
|$\lVert, \rVert$  | \lVert, \rVert |     |
|$\lbrace, \rbrace$| \lbrace, \rbrace 或 {, } |     |

**增大括号的方法：**

| 数学算式 | Markdown公式 | 核心语法 |
| :--:| :-: | :-: |
| $(x)$| (x) |     |
| $\big( x \big)$ | \big( x \big) |     |
| $\Big( x \Big)$| \Big( x \Big) |     |
| $\bigg( x \bigg)$| \bigg( x \bigg) |     |
| $\Bigg( x \Bigg)$| \Bigg( x \Bigg) |     |
| $\Bigg(\bigg(\Big(\big((x)\big)\Big)\bigg)\Bigg)$ | \Bigg(\bigg(\Big(\big((x)\big)\Big)\bigg)\Bigg) |     |
| $\Bigg[\bigg[\Big[\big[[x]\big]\Big]\bigg]\Bigg]$ | \Bigg[\bigg[\Big[\big[[x]\big]\Big]\bigg]\Bigg] |     |
| $\Bigg\langle\bigg\langle\Big\langle\big\langle\langle x \rangle \big\rangle\Big\rangle\bigg\rangle\Bigg\rangle$| \Bigg\langle\bigg\langle\Big\langle\big\langle\langle x \rangle\big\rangle\Big\rangle\bigg\rangle\Bigg\rangle |     |
| $\Bigg\lvert\bigg\lvert\Big\lvert\big\lvert\lvert x \rvert\big\rvert\Big\rvert\bigg\rvert\Bigg\rvert$| \Bigg\lvert\bigg\lvert\Big\lvert\big\lvert\lvert x \rvert\big\rvert\Big\rvert\bigg\rvert\Bigg\rvert |     |
| $\Bigg\lVert\bigg\lVert\Big\lVert\big\lVert\lVert x \rVert\big\rVert\Big\rVert\bigg\rVert\Bigg\rVert$ | \Bigg\lVert\bigg\lVert\Big\lVert\big\lVert\lVert x \rVert\big\rVert\Big\rVert\bigg\rVert\Bigg\rVert |     |

## <a id="t16"></a><a id="_679"></a>分式与根式

**分式的表示方法：**

（1）使用`\frac{a}{b}`表示分式，比如 $\frac {a+c+1}{b+c+2}$ ；

（2）使用`\over`来分隔一个组的前后两部分，如 ${a+1\over b+1}$ ;

（3）==连分数==，使用使用`\cfrac`代替`\frac`或者`\over`，两者效果对比如下：

**`\frac` 表示连分式：**

**数学算式：**  
$$x=a_0 + \frac{1^2}{a_ 1+\frac{2^2}{a_2+\frac{3^2}{a_3+ \frac{4^2}{a_4+...}}}}$$
  
**Markdown公式：**

```
$$x=a_0 + \frac{1^2}{a_ 1+\frac{2^2}{a_2+\frac{3^2}{a_3+ \frac{4^2}{a_4+...}}}}$$
```

**`\cfrac` 表示连分式：**

**数学算式：**  
  $$x=a_0 + \cfrac{1^2}{a_ 1+\cfrac{2^2}{a_2+\cfrac{3^2}{a_3+ \cfrac{4^2}{a_4+...}}}}$$
**Markdown公式：**

```
$$x=a_0 + \cfrac{1^2}{a_ 1+\cfrac{2^2}{a_2+\cfrac{3^2}{a_3+ \cfrac{4^2}{a_4+...}}}}$$
```

**`\cfrac` 表示连分式：**

| 数学算式 | Markdown公式 | 核心语法 |
| --- | --- | --- |
| $\frac{a}{b}$| \frac{a}{b} | 分数使用`\frac{分子}{分母}` |
| $a^i , a^{pre}$| a^i , a^{pre} | 上标使用`^` |

## <a id="t17"></a><a id="_717"></a>开方

| 数学算式 | Markdown公式 | 核心语法 |
| --- | --- | --- |
| $\sqrt{a + b}$| \sqrt{a + b} | 开方使用`\sqrt{}` |
| $\sqrt[n]{a + b}$| \sqrt\[n\]{a + b} | 开n次方使用`\sqrt[n]{}` |

## <a id="t18"></a><a id="_722"></a>累加/累乘

| 数学算式 | Markdown公式 | 核心语法 |
| --- | --- | --- |
|$\sum_{i = 0}^{n} x^2$| \sum_{i = 0}^{n} x^2 | 累加使用`\sum_{下标}^{上标}` |
|$\prod_{i = 0}^{n}\frac{1}{x}$| \prod_{i = 0}^{n}\frac{1}{x} | 累乘使用`\prod_{下标}^{上标}` |

## <a id="t19"></a><a id="_728"></a>三角函数

| 数学算式 | Markdown公式 | 释义  |
| --- | --- | --- |
| $\sin$ | \sin | 正弦  |
| $\cos$ | \cos | 余弦  |
| $\tan$ | \tan | 正切  |
| $\cot$ | \cot | 余切  |
| $\sec$ | \sec | 反正弦 |
| $\csc$ | \csc | 反余弦 |
| $\bot$ | \bot | 垂直  |
| $\angle$ | \angle | 夹角  |
| $40^\circ$ | 40^\circ | 度数  |

## <a id="t20"></a><a id="_741"></a>对数函数

| 数学算式 | Markdown公式 | 核心语法 |
| --- | --- | --- |
| $\ln{a + b}$ | \ln{a + b} | 以e为底，对数函数使用`\ln{}` |
| $\log_{a}^{b}$ | \log_{a}^{b} | 对数函数使用`\log_{a}^{b}` |
| $\lg{a + b}$ | \lg{a + b} | 以10为底，对数函数使用`\ln{}` |