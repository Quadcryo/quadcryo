---
layout: page
title: QM and computation with linalg research
description: linear algebra, quantum mechanics, quantum computation
img: assets/img/bra ket.png
importance: 1
category: ongoing
---

<i> Description </i>
<p>
This has been an ongoing project for many months now. I have worked on it actively and inactively over this time, and have made significant progress in linear algebra and working in Hilbert Space. While I know that many topics here will require significantly more reading and problem-solving, it is healthy to create goals along the way, so that is just what I have done. My research goal right now is to understand the spectral theorem and spectral decomposition. 
</p>

<br>
(NOTE: When we refer to a "number", we are more often than not referring to some complex number from $$\mathbb{C}$$. When we speak of a finite-dimensional vector space, we are largely talking about a finite-dimensional vector space over the field $$\mathbb{C}$$)
<br>

<h1> 
NOTES 
</h1> 

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

<h2> 
Definition of the inner product and other
</h2> 

<br>
Let us define the inner product. An inner product is a number given by $$(\cdot,\cdot)$$ for objects "$$\cdot$$". An inner product is linear in the second argument, 
<br>

$$
\begin{equation*} \big(|v_{i}\rangle,\sum_{i}\lambda_{i}|w_{i}\rangle\big) = \sum_{i}\lambda_{i}(|v\rangle,|w_{i}\rangle). \end{equation*}
$$

<br>
The inner product also satisfies $$(|v\rangle,|w\rangle)=(|w\rangle,|v\rangle)^{*}$$, where "$$*$$" denotes conjugation. Moreover, $$(|v\rangle,|v\rangle)\geq 0$$, and is $$0$$ iff. $$|v\rangle=0$$. Quite beautifully, the inner product is also conjugate linear in the first argument. This follows from
<br>

$$
\begin{align*}
\big(\sum_{i}\lambda_{i}|w_{i}\rangle,|v\rangle\big) & 
= \big(|v\rangle,\sum_{i}\lambda_{i}|w_{i}\rangle\big)^{*} \\ &
= \sum_{i}\lambda_{i}^{*}(|v\rangle,|w_{i}\rangle)^{*} \\ &
= \sum_{i}\lambda_{i}^{*}(|w_{i}\rangle,|v\rangle).
\end{align*}
$$

<br>
<br>
Note that a vector space with an inner product attached to it is known as "inner product space", and in quantum mechanics is known as "Hilbert space". We will be referring to this space as an inner product space for now, but will adopt the term "Hilbert space" eventually. Now that we have defined the inner product, we can begin introducing some more notation and techniques. The inner product is commonly notated as $$\langle v|w\rangle $$ for two vectors $$\langle v|$$ and $$| w\rangle $$, and are orthogonal if $$\langle v|w\rangle = 0$$. We define the norm of a vector $$ v\rangle $$ to be its magnitude, and write it as $$\left\Vert v\rangle \right\Vert = \sqrt{\langle v|v\rangle }$$. A unit vector is a vector $$| v\rangle $$ such that $$\left\Vert| v\rangle \right\Vert = 1$$. A vector is normalised if $$\left\Vert v\rangle \right\Vert $$. To normalise a vector, we divide by its norm, so the normalised form of a vector $$| v\rangle $$ is given as $$ |v\rangle /\left\Vert |v\rangle \right\Vert $$. A set of vectors $$|i\rangle $$ for $$i$$ is orthonormal if every vector in the set is a unit vector, and distinct vectors in the set are orthogonal (no vector except for the $$0$$ vector is orthogonal to itself) so that $$\langle i|j \rangle = \delta_{ij}$$, where $$\delta_{ij}$$ denotes the Kronecker delta. 
<br>

<h2>
The Gram-Schmidt process and proof
</h2>

<br>
There exists a method for constructing an orthonormal basis from an existing basis, known as the Gram-Schmidt process. If we have a basis $$|w_{1} \rangle, |w_{2}\rangle, \ldots, |w_{n}\rangle$$ in an inner product space $$V$$, then we can construct an orthonormal basis $$|v_{1} \rangle, |v_{2}\rangle, \ldots, |v_{n}\rangle$$ for $$V$$. Let us define 
<br>

$$
\begin{equation*} |v_{1}\rangle = \frac{|w_{1}\rangle}{\left\Vert |w_{1}\rangle \right\Vert } \end{equation*}
$$

<br>
Then for $$k$$ going from $$1$$ to $$n-1$$, we can define inductively
<br>

$$
\begin{equation*} |v_{k+1}\rangle = \frac{|w_{k+1}\rangle - \sum_{i=1}^{k}\langle v_{i}|w_{k+1}\rangle |v_{i}\rangle}{\left\Vert |w_{k+1}\rangle - \sum_{i=1}^{k}\langle v_{i}|w_{k+1}\rangle |v_{i}\rangle \right\Vert}. \end{equation*}
$$

<br>
Using this technique, we can always generate some orthonormal basis $$|v_{1} \rangle, |v_{2}\rangle, \ldots, |v_{n}\rangle$$. Notice that despite it seeming very complex, it uses the same general idea of normalisation by dividing by norm. Also notice that the numerator is a vector because the inner product always yields a number. We will now prove that this process in fact gives us an orthonormal basis. 
<br>
<br>
<b> Theorem </b> (Gram-Schmidt process)
<br>
<br>
Let $$V$$ be an inner product space, and let $$S = \{|w_{1}\rangle, |w_{2}\rangle,\ldots,|w_{n}\rangle \}$$ be a linearly independent set of vectors from $$V$$. Then the set $$\overline S = \{|v_{1}\rangle, |v_{2}\rangle,\ldots,|v_{n}\rangle \}$$ forms an orthonormal basis for $$V$$ such that 
<br>

$$
\begin{equation*} \text{span}\{|w_{1}\rangle, |w_{2}\rangle,\ldots,|w_{k}\rangle \}=\text{span}\{|v_{1}\rangle, |v_{2}\rangle,\ldots,|v_{k}\rangle \}, \forall k\in [1,n]. \end{equation*}
$$

<br>
<i> Proof. </i> We will be using a constructive proof. Since $$S$$ is a linearly independent set, $$|w_{k}\rangle \neq 0 \forall k$$. Let us define $$|v_{1}\rangle=\frac{|w_{1}\rangle}{\left\Vert |w_{1}\rangle \right\Vert}$$. Clearly, $$|v_{1}\rangle $$ is a normalised vector, and thus $$\text{span}\{|w_{1}\rangle\}=\text{span}\{|v_{1}\rangle\}$$, satisfying the theorem for $$k=1$$. Now let us define
<br>

$$
\begin{equation*} |v_{2}\rangle = \frac{|w_{2}\rangle - \langle w_{2}|v_{1} \rangle |v_{1}\rangle}{\left\Vert |w_{2}\rangle - \langle w_{2}|v_{1} \rangle |v_{1}\rangle \right\Vert}. \end{equation*}
$$

<br>
Note that this is the normalised form of the orthogonal decomposition given by $$|w_{2}\rangle - \langle w_{2}|v_{1}\rangle|v_{1}\rangle$$. From this we can see that $$\left\Vert |v_{2}\rangle \right\Vert = 1$$, and that indeed $$\text{span}\{|w_{1}\rangle,|w_{2}\rangle\}=\text{span}\{|v_{1}\rangle,|v_{2}\rangle\}$$. 
<br>
<br>
After continuing like this, suppose that we have constructed the orthonormal basis $$\{|v_{1}\rangle, |v_{2}\rangle,\ldots,|v_{k-1}\rangle \}$$ with $$\text{span}\{|w_{1}\rangle, |w_{2}\rangle,\ldots,|w_{k-1}\rangle \}=\text{span}\{|v_{1}\rangle, |v_{2}\rangle,\ldots,|v_{k-1}\rangle \}$$. We define

$$
\begin{equation} |v_{k}\rangle = \frac{|w_{k}\rangle - \langle w_{k}|v_{1}\rangle|v_{1}\rangle - \langle w_{k}|v_{2}\rangle|v_{2}\rangle - \cdots - \langle w_{k}|v_{k-1}\rangle|v_{k-1}\rangle}{\left\Vert |w_{k}\rangle - \langle w_{k}|v_{1}\rangle|v_{1}\rangle - \langle w_{k}|v_{2}\rangle|v_{2}\rangle - \cdots - \langle w_{k}|v_{k-1}\rangle|v_{k-1}\rangle \right\Vert} \end{equation} \label{eq:1}
$$

<br>
Since $$S$$ is a linearly independent set, $$|v_{k}\rangle \not\in \text{span}\{|w_{1}\rangle, |w_{2}\rangle,\ldots,|w_{k}\rangle\}$$. This is obvious because a vector cannot be contained within a span of vectors not containing itself. From this it also follows that $$|v_{k}\rangle \not\in \text{span}\{|v_{1}\rangle, |v_{2}\rangle,\ldots,|v_{k}\rangle\}$$. Although the denominator of equation $$(1)$$ consists of a possible linear combination of vectors that could result in an indeterminate form, the previous fact mitigates that, so we know that the expression is valid. Note also that $$\left\Vert |v_{k}\rangle \right\Vert =1 $$. To show that $$\overline S$$ is orthonormal, note that 
<br>

$$
\begin{align*} 
\langle v_{k}|v_{i} \rangle & = \bigg\langle \frac{|w_{k}\rangle - \langle w_{k}|v_{1}\rangle|v_{1}\rangle - \langle w_{k}|v_{2}\rangle|v_{2}\rangle - \cdots - \langle w_{k}|v_{k-1}\rangle|v_{k-1}\rangle}{\left\Vert |w_{k}\rangle - \langle w_{k}|v_{1}\rangle|v_{1}\rangle - \langle w_{k}|v_{2}\rangle|v_{2}\rangle - \cdots - \langle w_{k}|v_{k-1}\rangle|v_{k-1}\rangle \right\Vert} \bigg\rvert v_{i} \bigg\rangle \\ &
=\frac{\langle w_{k}|v_{i}\rangle - \langle w_{k}|v_{i}\rangle}{\left\Vert |w_{k}\rangle - \langle w_{k}|v_{1}\rangle|v_{1}\rangle - \langle w_{k}|v_{2}\rangle|v_{2}\rangle - \cdots - \langle w_{k}|v_{k-1}\rangle|v_{k-1}\rangle \right\Vert}
=0
\end{align*}
$$

<br>
for $$i\in [1,k-1]$$. Since this implies that the two vectors are orthogonal, we know that $$\overline S$$ is an orthonormal basis of $$V$$. To prove the final statement, notice in equation $$(1)$$ that $$|w_{k}\rangle \in \text{span}\{|v_{1}\rangle, |v_{2}\rangle,\ldots,|v_{k}\rangle \}$$. From this we know that $$\text{span}\{|w_{1}\rangle, |w_{2}\rangle,\ldots,|w_{k}\rangle \} \subset \text{span}\{|v_{1}\rangle, |v_{2}\rangle,\ldots,|v_{k}\rangle \}$$. Since the span of one set is a subset of the other, and both sets are linearly independent, they must span subspaces of $$V$$ with equal dimension. This implies that $$\text{span}(S) = \text{span}(\overline S)$$, and we are done. 
<br>
■
<br>
<br>
(1 June, 2023)
<br>
<br>

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

<h2>
The Cauchy-Schwarz Inequality and proofs
</h2>

<br>
The Cauchy-Schwarz Inequality is a very significant result, and takes numerous forms in a number of areas. Over the real numbers and with the dot product (a special case of the inner product), it states that 
<br>

$$
\bigg( \sum_{i=1}^{n}a_{i}b_{i} \bigg)^{2} \leq \bigg( \sum_{i=1}^{n}a_{i}^{2} \bigg)^{2}\bigg( \sum_{i=1}^{n}b_{i}^{2} \bigg)^{2}.
$$

<br>
If we use the inner product, the Cauchy-Schwarz Inequality is as follows:
<br>
<br>
<b>Theorem </b> (Cauchy-Schwarz Inequality)
<br>
<br>
Let $$|v\rangle$$ and $$|w\rangle$$ be vectors. Then
<br>

$$
\begin{equation*} |\langle v | w \rangle|^{2} \leq \langle v | v \rangle \langle w | w \rangle. \end{equation*}
$$

<br>
<i> Proof I. </i> We can prove this in two ways. The first way is more complex, but utilizes the previously developed outer product. Recalling that $$\left\Vert |w\rangle \right\Vert = \sqrt{\langle w|w\rangle}$$, we can obtain the first member of an orthonormal basis $$|i\rangle$$ to be 
<br>

$$
\begin{equation*} \frac{|w\rangle}{\sqrt{\langle w|w\rangle}}. \end{equation*}
$$

Using the definition of the identity $$I$$ in terms of the outer product, we have

$$
\begin{align*}
\langle v | v \rangle \langle w | w \rangle & 
= \bigg(\sum_{i}|i\rangle \langle i|\bigg)\langle v | v \rangle \langle w | w \rangle \\ & 
= \sum_{i}\langle v | v \rangle |i\rangle \langle i| \langle w | w \rangle \\ &
= \sum_{i}\langle v | i \rangle \langle i | v \rangle  \langle w | w \rangle.
\end{align*}
$$

<br>
Notice that $$\sum_{i}\langle v | i \rangle \langle i | v \rangle \geq \frac{\langle v | w \rangle \langle w | v \rangle}{\langle w | w \rangle}$$. This is somewhat obvious, because we are taking the sum, running through all $$i$$s, which yields a sum of values, whereas the $$RHS$$ is the same but divided by $$\langle w | w \rangle$$. There is, however, an exception when either vector is a multiple of the other, in which case we have equality. Then
<br>

$$
\begin{align*}
\langle v | v \rangle \langle w | w \rangle & 
\geq \frac{\langle v | w \rangle \langle w | v \rangle}{\langle w | w \rangle} \langle w | w \rangle \\ &
= \langle v | w \rangle \langle w | v \rangle \\ &
= \left\Vert \langle v | w \rangle \right\Vert^{2}.
\end{align*}
$$

<br>
If either vector is a multiple of the other, then we have equality. To show this, let $$|w\rangle = z|v\rangle $$ for some number $$z$$. Then 
<br>

$$
\begin{align*}
\langle v | v \rangle \langle w | w \rangle & 
= ( |v\rangle , |v\rangle) ( z|v\rangle , z|v\rangle), \text{and by linearity and conjugate linearity in both arguments} \\ &
= ( |v\rangle , |v\rangle)zz^{*}( |v\rangle, |v\rangle) \\ &
= \left\Vert z \right\Vert^{2}(\langle v | v \rangle)^{2}.
\end{align*}
$$

<br>
Furthermore, 
<br>

$$
\begin{align*}
|\langle v | w \rangle|^{2} & 
= |(|v\rangle, z|v\rangle|^{2} \\ &
= \left\Vert z(|v\rangle, |v\rangle \right\Vert^{2} \\ &
= \left\Vert z \right\Vert^{2}|(\langle v |v\rangle)^{2},
\end{align*}
$$

<br>
which is obviously equivalent to what we just derived, so we have shown when equality holds, and we are done. 
<br>
■
<br>
<br>
<i> Proof II. </i> The second way to prove this is by far simpler, but we will be using the dot product instead of the inner product. Recall that the dot product of two vectors $$v$$ and $$w$$ is given as 
<br>

$$
\begin{equation*} v \cdot w = \left\Vert v \right\Vert \left\Vert w \right\Vert \cos{\theta} \end{equation*},
$$

<br>
where $$\theta = |\arg{v} - \arg{w}|$$. Since we know that $$\cos{\theta}\leq 1$$ for all $$\theta$$, we can write this as the inequality
<br>

$$
\begin{align*}  
v\cdot w & \leq \left\Vert v \right\Vert \left\Vert w \right\Vert \\ 
(v\cdot w)^{2} & \leq \left\Vert v \right\Vert^{2} \left\Vert w \right\Vert^{2} \\
(v\cdot w)^{2} & \leq (v\cdot v)(w\cdot w),
\end{align*}
$$

<br>
which is Cauchy-Schwarz. Equality holds if either vector is a scalar multiple of the other because scaling a vector by a scalar does not change its argument. 
<br>
■

<br>
(3 June, 2023)
<br>

















