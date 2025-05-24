---
title: LaTeX数学语法学习
tags:
  - 开源分享
---
{% raw %}
# LaTeX数学语法学习

## 基础语法
### 行内公式与块公式
```latex
这是行内公式 $E=mc^2$ 示例
使用括号的写法 \( \frac{1}{2} \) 也是行内公式

单独成行的块公式：
$$ \sum_{i=1}^n i = \frac{n(n+1)}{2} $$
或者使用方括号：
\[ \int_a^b f(x)dx \]
```

这是行内公式 $E=mc^2$ 示例

使用括号的写法 \( \frac{1}{2} \) 也是行内公式

单独成行的块公式：
$$ \sum_{i=1}^n i = \frac{n(n+1)}{2} $$
或者使用方括号：
\\[ \int_a^b f(x)dx \\]

### 注释与空格
```latex
$E=mc^2% 这是单行注释（不会出现在渲染结果中）$

公式中的空格需要特殊符号：
$a\,b$（小空格）  
$a\quad b$（大空格）  
$a\!b$（负空格）
```

$E=mc^2% 这是单行注释$

公式中的空格需要特殊符号：
$a\,b$（小空格）  
$a\quad b$（大空格）  
$a\!b$（负空格）

### 关于换行
```latex
可以通过在公式末尾添加\\表示换行，但该特性并不会被所有编辑器支持。
另外一种换行的办法是引入gather环境(多行公式居中对齐)：
\begin{gather}
a^2,a_1\\
x^{y+z},p_{ij},p_ij\\
x_i,x_{\text i}\\
\end{gather}
单行公式换行:
\begin{multline} 1 + 2 + 3 + 4 + 5 + 6 \
+ 7 + 8 + 9 + 10 = 55 \end{multline}
```

\begin{gather}
a^2,a_1\\
x^{y+z},p_{ij},p_ij\\
x_i,x_{\text i}\\
\end{gather}

\begin{multline} 1 + 2 + 3 + 4 + 5 + 6 \
+ 7 + 8 + 9 + 10 = 55 \end{multline}

### 常用环境
```latex
$$
\begin{equation}
    e^{i\pi} + 1 = 0
\end{equation}
$$

$$
\begin{align}
    (a+b)^2 &= a^2 + 2ab + b^2 \\
    (a-b)^2 &= a^2 - 2ab + b^2
\end{align}
$$

$$
f(x) = 
\begin{cases}
    x^2 & x \geq 0 \\
    -x  & x < 0
\end{cases}
$$
```
> Tips：
> 
> 1. equation 环境：用于单个带自动编号（需要编辑器支持）的公式，适合独立方程的场景
> 
> 2. align 环境：用于多行对齐公式（用 & 指定对齐位置），每行默认带编号
> 
> 3. cases 环境：用于分段函数（需搭配 amsmath 宏包），用大括号包裹多个条件分支

$$
\begin{equation}
    e^{i\pi} + 1 = 0
\end{equation}
$$

$$
\begin{align}
    (a+b)^2 &= a^2 + 2ab + b^2 \\
    (a-b)^2 &= a^2 - 2ab + b^2
\end{align}
$$

$$
f(x) = 
\begin{cases}
    x^2 & x \geq 0 \\
    -x  & x < 0
\end{cases}
$$

### 数学字体
```latex
$$ \begin{gather} 
\mathbb{ABCD} \quad \text{黑板粗体} \\ 
\mathcal{ABCD} \quad \text{花体} \\ 
\mathscr{ABCD} \quad \text{手写体} \\ 
\mathbf{ABCD} \quad \text{粗体} \\ 
\mathsf{ABCD} \quad \text{无衬线体} 
\end{gather} 
$$
```

$$ \begin{gather} 
\mathbb{ABCD} \quad \text{黑板粗体} \\ 
\mathcal{ABCD} \quad \text{花体} \\ 
\mathscr{ABCD} \quad \text{手写体} \\
\mathbf{ABCD} \quad \text{粗体} \\ 
\mathsf{ABCD} \quad \text{无衬线体} 
\end{gather} 
$$

### 公式编号与引用
```latex
\begin{equation}\label{eq:1}
e^{i\pi} + 1 = 0
\end{equation}
在文本中引用：见公式 \eqref{eq:1}
```

\begin{equation}\label{eq:1}
e^{i\pi} + 1 = 0
\end{equation}

在文本中引用：见公式 (1)

> Tips：没有找到能在Mkdocs中显示编号的方法。

### 特殊符号输入
```latex
角度符号：90^\circ  
微分符号：\mathrm{d}（直立体）  
存在号：\exists\, x \in \mathbb{R}  
梯度：\nabla f
```

$$
\begin{gather}
角度符号：90^\circ\\
微分符号：\mathrm{d}（直立体）\\
存在号：\exists\, x \in \mathbb{R}\\
梯度：\nabla f
\end{gather}
$$

## 常用符号
### 希腊字母
??? latex
    ```latex
    $$
    \begin{gather}
    \delta,\lambda\\
    \Delta,\Lambda\\
    A B\\
    \phi,\varphi\\
    \epsilon,\varepsilon\\
    π
    \end{gather}
    $$
    ```

$$
\begin{gather}
\delta,\lambda\\
\Delta,\Lambda\\
A B\\
\phi,\varphi\\
\epsilon,\varepsilon\\
π
\end{gather}
$$

### 上下标
??? latex
    ```latex
    $$
    \begin{gather}
    a^2,a_1\\
    x^{y+z},p_{ij},p_ij\\
    x_i,x_{\text i}\\
    \text{A B},\rm{A B}\\
    \text A B,\rm A B\\
    {\rm A} B\\
    \text{e},\text{i}
    \end{gather}
    $$
    ```

$$
\begin{gather}
a^2,a_1\\
x^{y+z},p_{ij},p_ij\\
x_i,x_{\text i}\\
\text{A B},\rm{A B}\\
\text A B,\rm A B\\
{\rm A} B\\
\text{e},\text{i}
\end{gather}
$$

### 分式与根式
??? latex
    ```latex
    $$
    \frac{1}{2},\frac 1 2,\\
    \frac 1 {x+y}\\
    \frac {\dfrac 1 x + 1}{y + 1}
    $$

    $$
    \sqrt 2,\sqrt{x+y},\sqrt[3]x
    $$
    ```

$$
\frac{1}{2},\frac 1 2,\\
\frac 1 {x+y}\\
\frac {\dfrac 1 x + 1}{y + 1}
$$

$$
\sqrt 2,\sqrt{x+y},\sqrt[3]x
$$

### 普通运算符
??? latex
    ```latex
    $$
    \begin{gather}
    +-\\
    \times,\cdot,\div\\
    \pm,\mp\\
    ><,\ge,\le,\gg,\ll,\ne,\approx,\equiv\\
    \cap,\cup,\in,\notin,\subseteq,\subsetneqq,\varnothing\\
    \forall,\exists,\nexists\\
    \because,\therefore\\
    \mathbb R,R,Q,N,Z_+\\
    \mathcal F,\mathscr F
    \end{gather}
    $$

    $$
    \cdots,\vdots,\ddots
    $$

    $$
    \infty,\partial,∂,\nabla,\propto,^{\circ}
    $$

    $$
    \begin{gather}
    \sin x,\sec x,\cosh x\\
    \log_2 x, \ln x,\lg x\\
    \lim\limits_{x \to 0} \frac { x}{\sin x}\\
    \max x
    \end{gather}
    $$

    $$
    \text{MSE}(x)
    $$
    ```

$$
\begin{gather}
+-\\
\times,\cdot,\div\\
\pm,\mp\\
><,\ge,\le,\gg,\ll,\ne,\approx,\equiv\\
\cap,\cup,\in,\notin,\subseteq,\subsetneqq,\varnothing\\
\forall,\exists,\nexists\\
\because,\therefore\\
\mathbb R,R,Q,N,Z_+\\
\mathcal F,\mathscr F
\end{gather}
$$

$$
\cdots,\vdots,\ddots
$$

$$
\infty,\partial,∂,\nabla,\propto,^{\circ}
$$

$$
\begin{gather}
\sin x,\sec x,\cosh x\\
\log_2 x, \ln x,\lg x\\
\lim\limits_{x \to 0} \frac { x}{\sin x}\\
\max x
\end{gather}
$$

$$
\text{MSE}(x)
$$

### 大型运算符
??? latex
    ```latex
    $$
    \sum,\prod\\
    \sum_i,\sum_{i=0}^N\\
    \frac{\sum\limits_{i=1}^n x_i}{\prod\limits_{i=1}^n x_i}
    $$

    $$
    \int,\iint,\iiint,\oint,\\
    \int_{-\infty}^0 f(x)\,\text d x
    $$

    $$
    \begin{gather}
    a\, a\\
    a\ a\\
    a\quad a\\
    a\qquad a
    \end{gather}
    $$
    ```

$$
\sum,\prod\\
\sum_i,\sum_{i=0}^N\\
\frac{\sum\limits_{i=1}^n x_i}{\prod\limits_{i=1}^n x_i}
$$

$$
\int,\iint,\iiint,\oint,\\
\int_{-\infty}^0 f(x)\,\text d x
$$

$$
\begin{gather}
a\, a\\
a\ a\\
a\quad a\\
a\qquad a
\end{gather}
$$

### 标注符号
??? latex
    ```latex
    $$
    \vec x,\overrightarrow {AB},\\
    \bar x,\overline{AB}
    $$
    ```

$$
\vec x,\overrightarrow {AB},\\
\bar x,\overline{AB}
$$

### 箭头
??? latex
    ```latex
    $$
    \leftarrow,\Rightarrow,\Leftrightarrow,\longleftarrow
    $$
    ```

$$
\leftarrow,\Rightarrow,\Leftrightarrow,\longleftarrow
$$

### 括号与定界符
??? latex
    ```latex
    $$
    \begin{gather}
    ([])\{ \}\\
    \lceil,\rceil,\lfloor,\rfloor,||\\
    \left(0,\frac 1 a\right]\\
    \left.\frac {∂f}{∂x}\right|_{x=0}
    \end{gather}
    $$
    ```

$$
\begin{gather}
([])\{ \}\\
\lceil,\rceil,\lfloor,\rfloor,||\\
\left(0,\frac 1 a\right]\\
\left.\frac {∂f}{∂x}\right|_{x=0}
\end{gather}
$$

### 多行公式
??? latex
    ```latex
    $$
    \begin{align}
    a&=b+c+d\\
    &=e+f
    \end{align}
    $$
    ```

$$
\begin{align}
a&=b+c+d\\
&=e+f
\end{align}
$$

### 大括号
??? latex
    ```latex
    $$
    f(x)=
    \begin{cases}
    \sin x, & -π\le x \le π\\
    0,& \text{其他}
    \end{cases}
    $$
    ```

$$
f(x)=
\begin{cases}
\sin x, & -π\le x \le π\\
0,& \text{其他}
\end{cases}
$$

### 矩阵
??? latex
    ```latex
    $$
    \begin{matrix}
    a & b & \cdots & c \\
    \vdots& \vdots & \ddots & \vdots \\
    e & f& \cdots & g
    \end{matrix}
    $$

    $$
    \begin{bmatrix}
    a & b & \cdots & c \\
    \vdots& \vdots & \ddots & \vdots \\
    e & f& \cdots & g
    \end{bmatrix}
    $$

    $$
    \begin{pmatrix}
    a & b & \cdots & c \\
    \vdots& \vdots & \ddots & \vdots \\
    e & f& \cdots & g
    \end{pmatrix}
    $$

    $$
    \begin{vmatrix}
    a & b & \cdots & c \\
    \vdots& \vdots & \ddots & \vdots \\
    e & f& \cdots & g
    \end{vmatrix}
    $$

    $$
    \bf A,\bf B^{\rm T}
    $$
    ```

$$
\begin{matrix}
a & b & \cdots & c \\
\vdots& \vdots & \ddots & \vdots \\
e & f& \cdots & g
\end{matrix}
$$

$$
\begin{bmatrix}
a & b & \cdots & c \\
\vdots& \vdots & \ddots & \vdots \\
e & f& \cdots & g
\end{bmatrix}
$$

$$
\begin{pmatrix}
a & b & \cdots & c \\
\vdots& \vdots & \ddots & \vdots \\
e & f& \cdots & g
\end{pmatrix}
$$

$$
\begin{vmatrix}
a & b & \cdots & c \\
\vdots& \vdots & \ddots & \vdots \\
e & f& \cdots & g
\end{vmatrix}
$$

$$
\bf A,\bf B^{\rm T}
$$



## 实战演练
??? latex
    ```latex
    $$
    f(x) = \frac 1 {\sqrt{2\pi} \sigma} {\rm e} ^ {-\frac {(x-\mu)^2}{2\sigma ^ 2}}\\
    f(x) = \frac 1 {\sqrt{2\pi} \sigma} \exp \left[ {-\frac {(x-\mu)^2}{2\sigma ^ 2}}\right]
    $$

    $$
    \lim\limits_{N\to \infty} P \left\{ \left| \frac {I\left( \alpha_i \right)}{N} - H(s) \right| < \varepsilon  \right\} = 1
    $$

    $$
    x(n) = \frac 1 {2\pi} \int _{-π} ^ π X\left( {\rm e} ^ {{\rm j} \omega } \right) {\rm e} ^ {{\rm j} \omega n} \, {\rm d}\omega\\
    $$

    $$
    \begin{align}
    \vec B \left( \vec r \right) &= \frac {\mu_0}{4\pi}\oint_C \frac {I \, {\rm d} \vec l \times \vec R}{R^3}\\
    &= \frac {\mu_0}{4\pi} \int_V \frac{\vec J_V \times \vec R}{R^3}\, {\rm d} V'
    \end{align}
    $$
    ```

$$
f(x) = \frac 1 {\sqrt{2\pi} \sigma} {\rm e} ^ {-\frac {(x-\mu)^2}{2\sigma ^ 2}}\\
f(x) = \frac 1 {\sqrt{2\pi} \sigma} \exp \left[ {-\frac {(x-\mu)^2}{2\sigma ^ 2}}\right]
$$

$$
\lim\limits_{N\to \infty} P \left\{ \left| \frac {I\left( \alpha_i \right)}{N} - H(s) \right| < \varepsilon  \right\} = 1
$$

$$
x(n) = \frac 1 {2\pi} \int _{-π} ^ π X\left( {\rm e} ^ {{\rm j} \omega } \right) {\rm e} ^ {{\rm j} \omega n} \, {\rm d}\omega\\
$$

$$
\begin{align}
\vec B \left( \vec r \right) &= \frac {\mu_0}{4\pi}\oint_C \frac {I \, {\rm d} \vec l \times \vec R}{R^3}\\
&= \frac {\mu_0}{4\pi} \int_V \frac{\vec J_V \times \vec R}{R^3}\, {\rm d} V'
\end{align}
$$

## 常见错误示例
❌ 错误：x^2 + y^2 = z^2 % 缺少 $ 符号
✅ 正确：$x^2 + y^2 = z^2$

❌ 错误：\sqrt x + 1 （根号范围错误）
✅ 正确：$\sqrt{x + 1}$

❌ 错误：\text{误差} = 0.1%（百分号需要转义）
✅ 正确：$\text{误差} = 0.1\%$

`$x^2 + y^2 = z^2$` `$\sqrt{x + 1}$` `$\text{误差} = 0.1\%$`

{% endraw %}