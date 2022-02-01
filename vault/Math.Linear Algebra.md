---
id: oLeUJx2Gx7a1Lv465CBKK
title: Linear Algebra
desc: ''
updated: 1643689083566
created: 1642014686291
---
### Vectors
Can be represented by,
$
\begin{pmatrix}
a\\b\\.\\.
\end{pmatrix}
$  or a**i**+b**j**+c**k**+ ...

#### Linear Combination
$$
v_1,v_2,v_3,\ ...,v_n | v_n \in \R^n 
$$
of two or more vectors is basically a summation of the vectors where each of them are multiplied with a scalar.
$$
c_1v_1+c_2v_2+c_3v_3+\ ...+c_nv_n | c_n \in \R 
$$
![Linear Combination](https://upload.wikimedia.org/wikipedia/commons/6/6f/Linjcomb.png)

#### Span
The span is the set of all the linear combination of two or more vectors.
e.g If we have two vectors where $\overrightarrow{a}\neq k\overrightarrow{b}$ where $k\in\R$ ($\therefore$ the vectors are **linearly independent**) then the $span(a,b)=\R^2$
>**$span(\overrightarrow{a})$ is a line.**

>$span(v_1,v_2,v_3,\ ...,v_n)=\{c_1v_1+c_2v_2+c_3v_3+\ ...+c_nv_n |c_i\in\R\ for\ 1\leq i\leq n\}$

$$
\begin{aligned}
span\bigg\{\begin{pmatrix}2\\3\end{pmatrix}, \begin{pmatrix}4\\6\end{pmatrix} \bigg\} &= c_1\begin{pmatrix}2\\3\end{pmatrix}+  c_2\begin{pmatrix}4\\6\end{pmatrix}\\
&=c_1\begin{pmatrix}2\\3\end{pmatrix}+  2c_2\begin{pmatrix}2\\3\end{pmatrix}\\
&= (c_1+2c_2)\begin{pmatrix}2\\3\end{pmatrix}\\
&=c_3\begin{pmatrix}2\\3\end{pmatrix} (\therefore a\ line)
\end{aligned}
$$

To check if a set of vectors spans $\R^3$,
$$
c_1
\begin{pmatrix}
x_1\\x_2\\x_3
\end{pmatrix}
+c_2
\begin{pmatrix}
y_1\\y_2\\y_3
\end{pmatrix}
+c_3
\begin{pmatrix}
z_1\\z_2\\z_3
\end{pmatrix}=
\begin{pmatrix}
a\\b\\c
\end{pmatrix}
$$

If $\nexists$ a valid solution of $c_1,\ c_2,\ c_3$ for any given set of a, b and c values, then the set of vectors **do not span** $\R^3$

#### Inner Product
$$
\textbf{a} =\begin{pmatrix}
a_1\\a_2\\a_3
\end{pmatrix}
,
\textbf{b} = \begin{pmatrix}
b_1\\b_2\\b_3
\end{pmatrix}\\
\textbf{a}.\textbf{b}=a_1b_1+a_2b_2+a_3b_3
$$
Using matrix notation can also write it as,
$$
\textbf{a}^T\textbf{b}=a_1b_1+a_2b_2+a_3b_3
$$
where,
$$
\begin{pmatrix}
a_1&a_2&a_3
\end{pmatrix}
\begin{pmatrix}
b_1\\b_2\\b_3
\end{pmatrix}
$$

Knowing all this, we can say,
$$
\textbf{a}^T\textbf{a} = a_1^2+a_2^2+a_3^2\\
\therefore\sqrt{\textbf{a}^T\textbf{a}} = ||\textbf{a}||
$$
Sum of all elements of a vector:
$$
\textbf{1}^T\textbf{a} = a_1+a_2+a_3
$$
Mean of vector:
$$
\left(\frac{1}{n}\right)^T\textbf{a} = \frac{a_1+a_2+a_3}{n}
$$
Inner product with a unit vector:
$$
e_i^T\textbf{a} = a_i
$$

#### Linear Independence
In a set of vectors, If any one vector can be represented as a linear combination of the others, then the set is linearly dependent.    

To check for Linear Independence for a set of vectors,
$$
c_1
\begin{pmatrix}
x_1\\x_2\\x_3
\end{pmatrix}
+c_2
\begin{pmatrix}
y_1\\y_2\\y_3
\end{pmatrix}
+c_3
\begin{pmatrix}
z_1\\z_2\\z_3
\end{pmatrix}=
\begin{pmatrix}
0\\0\\0
\end{pmatrix}
$$
If the only solution to this is **not** $c_1=c_2=c_3=0$, then the set is **not Linearly Independent** 

#### Linear Superposition
If, for a function, $f(\alpha x+\beta y)\to \alpha f(x) + \beta f(y)$ then, the function is linear.

#### Affine Functions
Functions such that, $f(\alpha_1x_1+\alpha_2x_2+...+\alpha_nx_n)=$ is linear, and $\alpha_1 +\alpha_2+...+\alpha_n=1$