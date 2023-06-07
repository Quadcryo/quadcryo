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
<br>
[insert proof for (ii)]
<br>

<br>
Now that we have proven the spectral theorem, we can proceed to prove the spectral decomposition theorem. 
<br>
<br>
<b> Theorem </b> (Spectral Decomposition Theorem)
<br>
<br>
Any normal operator $$M$$ on a vector space $$V$$ is diagonal with respect to some orthonormal basis for $$V$$. Conversely, any diagonalisable linear operator is normal. 
<br>
<br>
<i> Proof. </i> We will prove the converse first, because it's easier. Consider some $$n\times n$$ matrix $$A$$. Since we assumed that $$A$$ is diagonalisable, we can determine its eigendecomposition or diagonal form to be
<br>

$$
\begin{align*}
A & 
= \lambda_{1}I + \lambda_{2}I + \cdots + \lambda_{n}I \\ &
= \begin{bmatrix} 
    \lambda_{1} + \lambda_{2} + \cdots + \lambda_{n} & \cdots & 0 \\
    \vdots & \ddots & \vdots \\
    0 & \cdots & \lambda_{1} + \lambda_{2} + \cdots + \lambda_{n}
  \end{bmatrix},
\end{align*}
$$

<br>
where the $$\lambda_{i}$$s are the eigenvalues of $$A$$. We will consider two separate cases: when the $$\lambda_{i}$$s are real and when they are complex. When the $$\lambda_{i}$$s are real, the matrix is Hermitian, and Hermitian operators are normal, so we are done. When the $$\lambda_{i}$$s are complex, we have an equivalent argument, except $$A$$ is no longer Hermitian. Note that $$z^{*}z=zz^{*}$$, or that a complex number commutes with its conjugate. Using this fact, we can see that $$A$$ must be normal because the resulting diagonal entries in $$A^{\dagger}A$$ will be the same as in $$AA^{\dagger}$$, and we are done.
<br>
<br>
Now we will prove the forward direction. Note that since $$M$$ is normal, $$M^{\dagger}M=MM^{\dagger}$$. The proof follows by induction on dim$$(V)=d$$. When $$d=1$$, there is only one element in the vector space, and the operator $$M$$ is a $$1\times 1$$ diagonal matrix (because it can't be anything else), so this case is trivial. Let $$\lambda$$ be an eigenvalue of $$M$$, let $$P$$ be the projector onto the eigenspace for $$\lambda$$, and let $$Q$$ be the projector onto the orthogonal complement of $$P$$. Since $$P + Q = P + (I - P) = I$$, we can write
<br>

$$
\begin{align*}
M & = (P + Q)M(P + Q) \\ & = PMP + QMQ + PMQ + QMQ.
\end{align*}
$$

<br>
We now need to determine several properties of these matrices. If we can show that $$M$$ is diagonal then we will be finished. First, notice that $$PMP=\lambda P$$ because $$PM$$ simply yields a scalar, namely the eigenvalue $$\lambda$$, and we then have $$PMP = \lambda P$$. Notice also that $$QMP = 0$$. This is because the operator $$M$$ maps $$P$$ to itself, so that $$MP\subseteq P$$. Since we said that $$Q$$ was the projector onto the space orthogonal to $$P$$, this must mean that $$QMP=0$$, which is also the zero operator. We will claim that $$PMQ=0$$ as well. To prove this, let $$|v\rangle$$ be an element of the vector subspace $$P$$. Then, since we assumed the normality of $$M$$, we have 
<br>

$$
M^{\dagger}M|v\rangle = MM^{\dagger}|v\rangle = \lambda M^{\dagger}|v\rangle. 
$$

<br>
This implies that $$M^{\dagger}|v\rangle$$ has the eigenvalue $$\lambda$$, so $$M^{\dagger}|v\rangle$$ is an element of the eigenspace for $$\lambda$$ for which $$P$$ is a projector. Thus we have that $$QM^{\dagger}P=0$$. Then we have that 
<br>





























