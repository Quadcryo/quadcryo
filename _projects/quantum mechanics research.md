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

<h1> 
NOTES 
</h1> 


<br>
We will assume a knowledge of basic linear algebra, such as vector spaces, eigenvectors, eigenvalues, transpose, trace, and characteristic equations. In order to begin to understand quantum mechanics, one must begin with the absolute basics of linear algebra. A finite-dimensional vector space with $$\text{dim}(V)=n$$ is a vector space $$V$$ for which there exists some finite set of vectors $$U=\{u_{1},u_{2},\ldots,u_{n}\}$$ that spans the vector space, or $$\text{span}(U)=V$$. An important notation to understand in quantum mechanics is the braket notation. With this notation, we denote a vector as a so-called "ket", represented as $$|v_{i}\rangle\in V$$, where $$V$$ is a vector space. The "bra" portion of the braket notation is represented as $$|\langle v_{i}|$$, and we will explain its significance later. 
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
There exists a method for constructing an orthonormal basis from an existing basis, known as the Gram-Schmidt process. If we have a basis $$|w_{1} \rangle, |w_{2}\rangle, \ldots, |w_{d}\rangle$$ in an inner product space $$V$$, then we can construct an orthonormal basis $$|v_{1} \rangle, |v_{2}\rangle, \ldots, |v_{d}\rangle$$ for $$V$$. Let us define 
<br>

$$
\begin{equation*} |v_{1}\rangle = \frac{|w_{1}\rangle}{\left\Vert |w_{1}\rangle \right\Vert } \end{equation*}
$$

<br>
Then for $$k$$ going from $$1$$ to $$d-1$$, we can define inductively
<br>

$$
\begin{equation*} |v_{k+1}\rangle = \frac{|w_{k+1}\rangle - \sum_{i=1}^{k}\langle v_{i}|w_{k+1}\rangle |v_{i}\rangle}{\left\Vert |w_{k+1}\rangle - \sum_{i=1}^{k}\langle v_{i}|w_{k+1}\rangle |v_{i}\rangle \right\Vert}. \end{equation*}
$$

<br>
Using this inductive technique, we can always generate some orthonormal basis $$|v_{1} \rangle, |v_{2}\rangle, \ldots, |v_{d}\rangle$$. Notice that despite it seeming very complex, it uses the same general idea of normalisation by dividing by norm. Also notice that the numerator is a vector because the inner product always yields a number. 
<br>
<br>
<b> Theorem </b> (Gram-Schmidt process)
<br>
<br>
\blacksquare
<br>



