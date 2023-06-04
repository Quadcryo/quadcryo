---
layout: page
title: Notes II
description: definition of the inner product and other
img: assets/img/bra ket.png
importance: 3
category: quantum mechanics research project (P)
---

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
<br>
(1 June, 2023)