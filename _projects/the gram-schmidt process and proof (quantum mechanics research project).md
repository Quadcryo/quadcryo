---
layout: page
title: Notes III
description: The Gram-Schmidt process and proof
img: assets/img/bra ket.png
importance: 4
category: Linear Algebra of Quantum Mechanics (P)
---

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