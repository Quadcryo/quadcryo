---
layout: page
title: Notes I 
description: linear operators
img: assets/img/bra ket.png
importance: 2
category: quantum mechanics research project
---

<h2>
Linear operators
</h2>

<br>
We will assume a knowledge of basic linear algebra, such as vector spaces, eigenvectors, eigenvalues, transpose, trace, and characteristic equations. In order to begin to understand quantum mechanics, one must begin with the absolute basics of linear algebra. A finite-dimensional vector space with $$\text{dim}(V)=n$$ is a vector space $$V$$ for which there exists some finite set of vectors $$U=\{u_{1},u_{2},\ldots,u_{n}\}$$ that spans the vector space, or $$\text{span}(U)=V$$. An important notation to understand in quantum mechanics is the braket notation. With this notation, we denote a vector as a so-called "ket", represented as $$|v_{i}\rangle\in V$$, where $$V$$ is a vector space. The "bra" portion of the braket notation is represented as $$\langle v_{i}|$$, and we will explain its significance later. 
<br>
<br>
In quantum mechanics, we commonly refer to matrices as "linear operators". A linear operator is a function $$A: V \rightarrow W$$ from a vector space $$V$$ to a vector space $$W$$ that is linear in its inputs, namely 
<br>

$$
\begin{equation*} A\big(\sum_{i}a_{i}|v_{i}\rangle \big) = \sum_{i}a_{i}A(|v_{i}\rangle) \end{equation*},
$$

<br>
where $$A$$ is a linear operator. However, to simplify notation, instead of tediously representing an action of some linear operator $$A$$ on a vector with $$A(|v_{i}\rangle)$$, we can write it as $$A|v_{i}\rangle$$. There are two trivial linear operators. For some vector space $$V$$, $$I_{V}$$ is the identity linear operator, and $$I_{V}|v_{i}\rangle=|v_{i}\rangle$$ for all vectors $$|v_{i}\rangle\in V$$. Also, $$0$$ is the zero vector, and $$0|v_{i}\rangle=0$$ for all vectors $$|v_{i}\rangle\in V$$. A linear operator $$A$$ is equivalent to a matrix representation. To see how this fits into the bigger picture, if we have some vector space $$V_{m}$$ and another vector space $$V_{n}$$, then the $$m\times n$$ linear operator $$A$$ with entries $$A_{ij}$$ takes a vector from $$V_{m}$$ and maps it to a vector in $$V_{n}$$. In other words,  
<br>

$$
\begin{equation*} A\sum_{i}a_{i}|v_{i}\rangle  = \sum_{i}a_{i}A|v_{i}\rangle .\end{equation*}
$$