# The mathmatics basics of CN



## Vectors and Functions

### Vectors

| Vector        | 矢量 |
| -------------------------- | -------------- |
| Definition | a list of numbers 数字列表 |
| Eg | (3, 1)、(-10, 8)、(-1, 2, -3, 4) |
| Dimensionality(维数) | the number of elements in the vector. For example: (3, 1) is 2D vectors, it can be draw in x,y system. |

### The operations of vectors(运算)

- Sum: $ \vec{x} $ = ($x_1$, $x_2$, ...., $x_n$) $\rightarrow$ n · D vectors
  - Sum($ \vec{x} $) = $x_1$ + $x_2$ + .... + $x_n$

  1. Input: vectors & output: scalar(标量), which is just a single number.

 - Dot product(or projections, 点积/投影) : $ \vec{x} $​ = ($x_1$​, $x_2$​, ...., $x_n$​) , $ \vec{y} $​ = ($y_1$​, $y_2$​, ...., $y_n$​​)

   - $ \vec{x} $ · $ \vec{y} $ = $x_1$·$y_1$ + $x_2$·$y_2$ + .... + $x_n$·$y_n$

​	1. Input: **Two** vectors & output: **a** scalar(标量).

​	2. _Dot product can show how aligned two vector are.(排列程度)_

​	3. If dot product is 0, that means the two vectors are perpendicular/orthogonal.(垂直的 = 正交的, $\perp$)



### Function(函数)

The operations of function with vectors:

- **Sum** $\rightarrow$ calculus(微积分) $\rightarrow$ integral(积分) $\rightarrow$ the area under the curve $\rightarrow$ $\int_{a}^{b} f(x) \, dx$
1. Input: function & output: number
- **Dot product**  $\rightarrow$ projections  $\rightarrow$  $g(x)$ = $f(x)_1 · f(x)_2$ = $\int_{a}^{b} f(x)_1 · f(x)_2 \, dx$
  1. Sum become integrals.
  2. When dot product = 0, that means these two function are **orthogonal**.(aka, the sum of area under the curve $g(x)$)



## Convolutions and linear systems

### Linear Time Invariant system (aka, linear system, or LTI):

- The element of linear system(use “time” for example): Input = some signal such as a function of time(t), Output = another function.

​	So The linear system can takes in a function x of t and spits out a function y of t.

​	Therefore, It can be used to get the output which is a **filtered version** of the input.

- $y(t)$ = projection of $f(t)$ onto $x(t)$.   $f(t)$ is the filter of t. 

<img src="C:/Users/23112/Downloads/7.png" width="60%">

> You can see the **red** curve is $y=x(t)$, you can move the **blue** filter $f(t)$ as a window to get the $y(t)$.

**Aka**, $y(t)$ = $x(t) · f(t)$ and $f(t)$​ only move in fixed distance = window width.(固定距离, 也被称为窗宽/支撑宽度)



## Representing vectors and matrices in a different basis

如何在不同基底中展示矢量与矩阵: 

​						$\vec{v}$ = $$
\left(
\begin{matrix}
v_1 \\
v_2 
\end{matrix}
\right)
$$

