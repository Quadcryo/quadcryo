---
layout: page
title: Notes VII
description: Hermitian operators (pt. 1) 
img: assets/img/bra ket.png
importance: 8
category: quantum mechanics research project (P)
---

In these next several notes, we will be going over one of the most important topics in linear algebra and begin our approach toward understanding quantum mechanics. We will first be talking about Hermitian operators, and will describe and prove several properties. We will then introduce the spectral decomposition theorem, alongside the spectral theorem, which is slightly less related, but is still incredibly important for verifying the existence of diagonalisable matrices under certain conditions. Furthermore, we will begin using "Hilbert space" and "inner product space" interchangeably from now on. 
<br>
<br>
Let $$A$$ be a linear operator on $$V$$ a Hilbert space. There exists a unique linear operator $$A^{\dagger}$$ on $$V$$ such that for $$|v\rangle, |w\rangle \in V$$, 
<br>

$$
(|v\rangle, A|w\rangle) = (A^{\dagger}|v\rangle, |w\rangle).
$$

<br>
We define $$A^{\dagger}=(A^{*})^{T}$$. Some properties that can quickly be proven from this definition are that for two linear operators $$A$$ and $$B$$, $$(AB)^{\dagger} = A^{\dagger}B^{\dagger}$$. If $$|v\rangle $$ is a vector, then $$|v\rangle^{\dagger} = \langle v|$$. We then have
<br>

$$
(A|v\rangle)^{\dagger} = A^{\dagger}|v\rangle^{\dagger} = \langle v| A^{\dagger}.
$$

<br>
<b> Lemma </b>  
<br>

$$
\begin{array}{ll}
    \text{(i)} & (|w\rangle \langle v|)^{\dagger} = |v\rangle \langle w|, \\
    \text{(ii)} & \bigg( \sum_{i}a_{i}A_{i} \bigg)^{\dagger} = \sum_{i}a_{i}^{*}A_{i}^{\dagger} \ \text{(anti-linearity)}, \\
    \text{(iii)} & (A^{\dagger})^{\dagger} = A.
\end{array}
$$

<br>
<i> Proofs. </i> To prove (i), we have
<br>

$$
\begin{align*}
(|w\rangle \langle v|)^{\dagger} & 
= |w\rangle^{\dagger} \langle v|^{\dagger} \\ & 
= |w\rangle^{\dagger} (|v\rangle^{\dagger})^{\dagger} \\ & 
= |v\rangle \langle w|.
\end{align*}
$$

<br>
To prove (ii), we have
<br>

$$
\begin{align*}
\bigg( \sum_{i}a_{i}A_{i} \bigg)^{\dagger} & 
= \bigg(\bigg( \sum_{i}a_{i}A_{i} \bigg)^{*}\bigg)^{T} \\ &
= \bigg( \sum_{i}a_{i}^{*}A_{i}^{*} \bigg)^{T} \\ &
= \sum_{i}a_{i}^{*}A_{i}^{\dagger}. 
\end{align*}
$$

<br>
And finally, to prove (iii), we have
<br>

$$
\begin{align*}
(A^{\dagger})^{\dagger} &
= (((A^{*})^{T})^{*})^{T} \\ & 
= (((A^{*})^{*})^{T})^{T} \\ & 
= (A^{T})^{T} = A. 
\end{align*}
$$

■

<br>
A linear operator $$A$$ such that $$A^{\dagger}=A$$ is known as a <b> self-adjoint </b>, or a <b> Hermitian operator </b>. This will be incredibly useful later. We will now introduce a certain class of Hermitian operators known as <b> projectors </b>. Notice that the term "projector" seems familiar, as in elementary linear algebra it means to find the projection of one vector onto another vector. The projector operators perform a similar task, and we can determine a scalar (expressed in terms of the inner product however) that scales the vector. Let $$W$$ be a $$k$$-dimensional vector subspace of the $$d$$-dimensional vector space $$V$$. It is possible to construct the orthonormal basis $$|1\rangle,|2\rangle,\ldots,|d\rangle$$ for $$V$$ by the Gram-Schmidt process, and it follows that we can construct an orthonormal basis $$|1\rangle,|2\rangle,\ldots,|k\rangle$$ for $$W$$. We thus define the projector
<br>

$$
P = \sum_{i=1}^{k}|i\rangle \langle i|
$$

<br>
to be the projector onto the subspace $$W$$. The projector is a linear operator, and its dimensions are confined by the dimensions of the subspace on which it acts. It can be verified that the operator $$|v\rangle \langle v|$$ is Hermitian for any $$|v\rangle$$ using a lemma above, so this means that the projector operator is indeed Hermitian, so $$P^{\dagger}=P$$. To see how this relates to the projector in elementary linear algebra, let $$|u\rangle$$ be a vector. Then the $$v$$th projector $$P_{v} = |v\rangle \langle v|$$. As $$P_{v}$$ acts on the vector $$|u\rangle$$, we have
<br>

$$
\begin{align*}
P_{v}|u\rangle & 
= |v\rangle \langle v|(|u\rangle) \\ &
= |v\rangle \langle v|u \rangle.
\end{align*}
$$

<br>
Let $$\langle v|u \rangle$$ be some number $$c$$. Then $$P_{v}|v\rangle = c|v\rangle$$. Thus the projector has the effect of scaling the vector by a certain scalar, which is where it derives its name "projector". By convention, instead of saying the vector space onto which $$P$$ is a projector, we will simply say the vector space $$P$$. 
<br>
<br>
We define the <b> orthogonal complement </b> of $$P$$ to be the operator $$Q = I - P$$. We can see that $$Q$$ is a projector onto the vector space spanned by the set of vectors $$|k+1\rangle, |k+2\rangle,\ldots,|d\rangle$$ because
<br>

$$
\begin{align*}
Q &
= I - P \\ & 
= \sum_{i=1}^{d}|i\rangle \langle i| - \sum_{i=1}^{k}|i\rangle \langle i| \\ & 
= \sum_{i=k+1}^{d}|i\rangle \langle i|,
\end{align*}
$$

<br>
which is the projector that spans that list. We will refer to the orthogonal complement of $$P$$ as $$Q$$. 
<br>
<br>
<b> Lemma </b> (Idempotence of the projector operator)
<br>

$$
P^{2} = P. 
$$

<br>
<i> Proof. </i> Let us have some projector $$|v\rangle \langle v|$$ that is orthonormal $$\forall |v\rangle$$ so that $$\langle v|v\rangle = 1$$. Then we have
<br>

$$
\begin{align*}
(|v\rangle \langle v|)^{2} &
= (|v\rangle \langle v|)(|v\rangle \langle v|) \\ &
= |v\rangle \langle v|v\rangle \langle v| \\ &
= |v\rangle \langle v|. 
\end{align*}
$$

■

<br>
We will conclude with several definitions and facts that will be useful later in our proof of spectral decomposition later. An operator $$A$$ is <b> normal </b> if $$AA^{\dagger}=A^{\dagger}A$$. In other words, $$A$$ is normal if it commutes with its self-adjoint. Also, we define a matrix $$U$$ - and thus linear operator $$U$$ - to be <b> unitary </b> if it satisfies the equation $$UU^{\dagger}=1$$. Similarly, an <b> orthogonal matrix </b> is essentially unitary if it is symmetric. In this way, we say that a matrix $$A$$ is orthogonal if $$A^{-1}=A^{T}$$, and that, by multiplying both sides by $$A$$, $$AA^{T}=I$$. All orthogonal matrices are invertible. Finally, one very useful property of transposes is that the transpose of a product of linear operators is equivalent to the transpose of each matrix but swapped from the original order. So $$(AB)^{T}=B^{T}A^{T}$$. This will be used later. 
<br>
<br>
(7 June, 2023)