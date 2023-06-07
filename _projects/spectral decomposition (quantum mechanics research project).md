---
layout: page
title: Notes VIII
description: The spectral theorem and spectral decomposition
img: assets/img/bra ket.png
importance: 9
category: quantum mechanics research project (P)
---

In the previous set of notes, we briefly introduced the notion of normality. In quantum mechanics, determining the eigendecomposition of a matrix and determining the diagonal matrix are extremely important, as they allow us to represent certain operators in terms of their eigenvalues and eigenvectors. The act of writing a diagonisable matrix in terms of its eigenvalues and eigenvectors with respect to an orthonormal basis is known as spectral decomposition. The spectral theorem, which we will introduce and prove here, proves several facts about certain types of operators, and guarantees the existence of the spectral decomposition. 
<br>

<br>
<b> Theorem </b> (Spectral Theorem)
<br>
<br>
Let $$A$$ be a symmetric linear operator with real entries. Then
<br>

$$
\begin{array}{ll}
    \text{(i)} & A \ \text{has real eigenvalues}, \\ 
    \text{(ii)} &  \text{there is a basis of} \ \mathbb{R}^{n} \ \text{such that it has the eigenvectors of} \ A. 
\end{array}
$$

<br>
The second property is what allows us to determine the spectral decomposition. If there exists a basis with eigenvectors of $$A$$, then we can represent a diagonalised matrix in terms of its eigenvalues, eigenvectors, all with respect to some orthonormal basis. 
<br>
<br>
<br>
<i> Proof of the Spectral Theorem. </i> We will begin by proving (i). Suppose that $$\lambda\in \mathbb{C}$$ is an eigenvalue. Note that $$\mathbb{R}\subseteq\mathbb{C}$$. If the eigenvalues are real, then we must have that $$\lambda = \lambda^{*}$$, so we will prove this. Let $$|v\rangle$$ be a vector. Recall the eigenvalue-eigenvector equation $$A|v\rangle = \lambda|v\rangle$$. If we take the conjugate of both sides, we have $$A^{*}|v\rangle^{*} = \lambda^{*}|v\rangle^{*}$$. However, since $$A\in M_{\mathbb{R}}$$, $$A^{*}=A$$, so $$A|v\rangle^{*} = \lambda^{*}|v\rangle^{*}$$. We will take the tranpose of the expression in two different ways. First, if we take the transpose but substitute $$\lambda|v\rangle$$ for $$A|v\rangle$$, we have
<br> 

$$
\begin{align*}
(A|v\rangle)^{T}|v\rangle^{*} &
= (\lambda|v\rangle)^{T}|v\rangle^{*} \\ &
= \lambda|v\rangle^{T}|v\rangle^{*}.
\end{align*}
$$

<br>
Alternatively, we can evaluate the transpose as follows:
<br>

$$
\begin{align*}
(A|v\rangle)^{T}|v\rangle^{*} &
= |v\rangle^{T}A^{T}|v\rangle^{*}, \ \text{and since} \ A \ \text{is symmetric}, \\ &
= |v\rangle^{T}A|v\rangle^{*} \\ &
= |v\rangle^{T}\lambda^{*}|v\rangle^{*}. 
\end{align*}
$$

<br>
These evaluations are equivalent, so $$\lambda|v\rangle^{T}|v\rangle^{*} = |v\rangle^{T}\lambda^{*}|v\rangle^{*}$$. Since the eigenvectors are not the zero vector $$|0\rangle$$, we can divide both sides by $$|v\rangle^{T}|v\rangle$$ to obtain $$\lambda = \lambda^{*}$$, and we are done. 
<br>















