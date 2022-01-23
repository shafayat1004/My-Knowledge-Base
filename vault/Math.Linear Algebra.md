---
id: oLeUJx2Gx7a1Lv465CBKK
title: Linear Algebra
desc: ''
updated: 1642940553768
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