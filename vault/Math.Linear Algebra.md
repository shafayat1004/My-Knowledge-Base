---
id: oLeUJx2Gx7a1Lv465CBKK
title: Linear Algebra
desc: ''
updated: 1642017528650
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

