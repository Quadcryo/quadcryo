---
layout: page
title: notes IV
description: intuition for outer products and their uses
img: assets/img/bra ket.png
importance: 5
category: quantum mechanics research project
---

<h2>
Intuition for outer products and their uses
</h2>

Now that we have proven that the Gram-Schmidt process is valid, we can use it in proving later statements. While we have defined linear operators to essentially matrices, we formally state that here. Let there exist vectors $$|v\rangle = \sum_{i}w_{i}|i\rangle$$ and $$|w\rangle = \sum_{j}v_{j}|i\rangle$$, where $$|i\rangle$$ and $$|j\rangle$$ are orthonormal bases. We stated earlier that if $$|i\rangle$$ and $$|j\rangle$$ are orthonormal bases, then $$\langle i|j\rangle = 1$$. Then
<br>

$$
\begin{align*}
\langle i|j\rangle & 
= \bigg(\sum_{i}v_{i}|i\rangle,\sum_{j}w_{j}|i\rangle\bigg), \text{and by linearity} \\ &
= \sum_{ij}v_{i}^{*}w_{j}\bigg(\sum_{i}|i\rangle,\sum_{j}|i\rangle\bigg) \\ &
= \sum_{ij}v_{i}^{*}w_{j}\delta_{ij} \\ &
= \sum_{ii}v_{i}^{*}w_{i}(1) \\ &
= \begin{bmatrix} 
    v_{1}^{*} & v_{2}^{*} & \cdots & v_{n}^{*} 
  \end{bmatrix}
  \begin{bmatrix}
    w_{1} \\
    w_{2} \\
    \vdots \\
    w_{n}
  \end{bmatrix}.
\end{align*}
$$

<br>
In other words, we may view a "bra" as a conjugated row vector, and a "ket" as a column vector. Of course, when we multiply these two vectors, the resulting product is a number, reinforcing the idea that we are in fact computing an inner product. We now proceed to introduce the outer product. Suppose that $$|v\rangle\in V$$ and $$|w\rangle\in W$$, where $$V$$ and $$W$$ are inner product spaces, and let $$|u\rangle$$ be a vector. We define $$|v\rangle \langle w|$$ to be the linear operator from $$V$$ to $$W$$ defined by $$(|v\rangle \langle w|)(|u\rangle) = \langle w|u\rangle |v\rangle$$. We can interpret this in two equivalent ways: $$|v\rangle \langle w|$$ acting on a vector $$|u\rangle$$, or the number $$\langle w|u\rangle$$ acting as a scalar on the vector $$|w\rangle$$. Either way, it is the same. If we want to express a linear combination of the outer product, we naturally do so as follows:
<br>

$$
\begin{equation*} \sum_{i}a_{i}|w_{i}\rangle \langle v_{i}|(|u\rangle) = \sum_{i}a_{i}|w_{i}\rangle \langle v_{i}|u\rangle. \end{equation*}
$$

<br>
To ensure that the outer product is a valid linear operator, we must define the identity linear operator. Let $$|i\rangle$$ be an orthonormal basis for a vector space $$V$$, so that we may express every vector $$|v\rangle \in V$$ as $$\sum_{i}v_{i}|i\rangle$$, for $$v_{i}$$ a set of numbers. Notice that $$\langle i|v \rangle = v_{i}$$ because the $$i$$th number is $$1$$ in the orthonormal basis, so when taking the inner product we simply have $$v_{i}$$. Then
<br>

$$
\begin{align*} 
\bigg(\sum_{i}|i\rangle \langle i|\bigg)|v\rangle &
= \sum_{i}|i\rangle \langle i|v\rangle \\ &
= \sum_{i}v_{i}|i\rangle 
= |v\rangle.
\end{align*}
$$

<br>
Since this statement is true $$\forall |v\rangle\in V$$, we must have that $$\sum_{i}|i\rangle \langle i|=I$$, or the identity. Now we have established there exists an identity $$I$$ for the outer product. With this, we can now express any linear operator in the outer product form. This is a useful form of both notation and has many uses when dealing with inner products. Let $$A: V \rightarrow W$$ be a linear operator and let $$v_{i}\in V$$ and $$w_{j}\in W$$ be orthonormal bases. Let's find the outer product representation of $$A$$:
<br>

$$
\begin{align*}
A & 
= I_{V}AI_{W} \\ &
= \sum_{j}|w_{j}\rangle \langle w_{j}| A \sum_{i}|v_{i}\rangle \langle v_{i}| \\ &
= \sum_{ij}|w_{j}\rangle \langle w_{j}| A |v_{i}\rangle \langle v_{i}| \\ &
= \sum_{ij} \langle w_{j}| A |v_{i}\rangle |w_{j}\rangle \langle v_{i}|, 
\end{align*}
$$

<br>
and we are done. 
<br>