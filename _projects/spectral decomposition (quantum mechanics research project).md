---
layout: page
title: Notes VIII
description: The spectral theorem and spectral decomposition
img: assets/img/bra ket.png
importance: 9
category: quantum mechanics research project (P)
---

In the previous set of notes, we briefly introduced the notion of normality. In quantum mechanics, determining the eigendecomposition of a matrix and determining the diagonal matrix are extremely important, as they allow us to represent certain operators in terms of their eigenvalues and eigenvectors. The act of writing a diagonisable matrix in terms of its eigenvalues and eigenvectors with respect to an orthonormal basis is known as spectral decomposition. The spectral theorem, which we will introduce and prove here, proves several facts about certain types of operators, and guarantees the existence of the spectral decomposition. The proof of the spectral theorem uses many more ideas from linear algebra. 
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
    \text{(ii)} &  \text{there is an orthonormal basis of} \ \mathbb{R}^{n} \ \text{such that it has the eigenvectors of} \ A. 
\end{array}
$$

<br>
The second property is what allows us to determine the spectral decomposition. If there exists a basis with eigenvectors of $$A$$, then we can represent a diagonalised matrix in terms of its eigenvalues, eigenvectors, all with respect to some orthonormal basis. 
<br>
<br>
<br>
<i> Proof of the Spectral Theorem. </i> We will begin by proving (i). Suppose that $$\lambda\in \mathbb{C}$$ is an eigenvalue. Note that $$\mathbb{R}\subseteq\mathbb{C}$$. If the eigenvalues are real, then we must have that $$\lambda = \lambda^{*}$$, so we will prove this. Let $$|v\rangle$$ be a vector. Recall the eigenvalue-eigenvector equation $$A|v\rangle = \lambda|v\rangle$$. If we take the conjugate of both sides, we have $$A^{*}|v\rangle^{*} = \lambda^{*}|v\rangle^{*}$$. However, since $$A\in M_{n\times n}(\mathbb{R})$$, $$A^{*}=A$$, so $$A|v\rangle^{*} = \lambda^{*}|v\rangle^{*}$$. We will take the tranpose of the expression in two different ways. First, if we take the transpose but substitute $$\lambda|v\rangle$$ for $$A|v\rangle$$, we have
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
We now proceed to prove (ii). It is in fact true that (ii) is equivalent to the statement: for a symmetric matrix $$A$$, there exists an orthogonal matrix $$R^{-1}AR$$ that is diagonal. 
<br>
<br>
To begin, let $$\lambda_{1}$$ be an eigenvalue of $$A$$. Since $$A$$ is symmetric, by (i), $$\lambda_{1}$$ and all other eigenvalues of $$A$$ must be real. Thus, $$A$$ will also have a corresponding eigenvector $$|v_{1}\rangle$$. Let us normalise $$|v_{1}\rangle$$ so that $$\left\Vert |v_{1}\rangle \right\Vert = 1$$. We now can extend $$|v_{1}\rangle$$ to a basis such that we have the spanning list $$|v_{1}\rangle, |u_{1}\rangle, \ldots, |u_{n}\rangle$$ for our original inner product space. The Gram-Schmidt process guarantees that it is possible to transform this basis into an orthonormal basis, so we rewrite this list as the orthomormal basis $$|v_{1}\rangle, |v_{2}\rangle, \ldots, |v_{n}\rangle$$. 
<br>
<br>
Define the matrix $$P = \begin{bmatrix} |v_{1}\rangle & |v_{2}\rangle & \cdots & |v_{n}\rangle \end{bmatrix}$$. We can see that $$P$$ is orthogonal because its entries are orthonormal. Let us define some matrix $$B=P^{-1}AP$$. We want to show that $$B$$ is diagonal. To do this, we first need to show that is is symmetric. Recall that an orthogonal matrix satisfies the property that its inverse and transpose are equivalent. Then
<br>

$$
\begin{align*}
B & 
= P^{-1}AP \\ &
= P^{T}AP \\ 
B^{T} & 
= (P^{T}AP)^T \\ & 
= (AP)^{T}(P^{T})^{T} \\ &
= P^{T}A^{T}P = P^{T}AP,
\end{align*}
$$

<br>
so $$B$$ is symmetric. We now consider the product $$B|e_{1}\rangle$$, where $$|e_{1}\rangle$$ denotes the unit vector of our $$n-$$dimensional vector space with $$1$$ as its first entry. If we compute this, we then have a column vector, which is also the first column of our matrix. We can also write $$P^{T}AP|e_{1}\rangle$$. Since we defined the eigenvalue of our vector $$|v_{1}\rangle$$ to be $$\lambda_{1}$$, we can compute the part $$P|e_{1}\rangle = |v_{1}\rangle$$. Thus we can write
<br>

$$
P^{T}AP|e_{1}\rangle = P^{T}A|v_{1}\rangle,
$$

<br>
but $$A|v_{1}\rangle$$ is equivalent to the $$\lambda_{1}$$ eigenvalue expression, so we have
<br>

$$
\begin{align*}
P^{T}A|v_{1}\rangle & 
= P^{T}\lambda_{1}|v_{1}\rangle \\ &
= \lambda_{1}P^{T}|v_{1}\rangle \\ &
= \lambda_{1} \begin{bmatrix} |v_{1}\rangle \\ |v_{2}\rangle \\ \vdots \\ |v_{n}\rangle \end{bmatrix}|v_{1}\rangle \\ &
= \lambda_{1} \begin{bmatrix} |v_{1}\rangle \cdot |v_{1}\rangle \\ |v_{2}\rangle \cdot |v_{1}\rangle \\ \vdots \\ |v_{n}\rangle 
  \cdot |v_{1}\rangle \end{bmatrix} \\ &
= \begin{bmatrix} \lambda_{1} \\ 0 \\ \vdots \\ 0 \end{bmatrix},
\end{align*}
$$

<br>
since $$|v_{i}\rangle \cdot |v_{j}\rangle = \delta_{ij}$$, or any two nonequivalent vectors in an orthonormal basis must be orthogonal, hence their dot product must be $$0$$. This is the first column of $$B$$. Since $$B$$ is symmetric, we can take the transpose of this expression to obtain the first row of $$B$$, which is $$\begin{bmatrix} \lambda_{1} & 0 & \cdots & 0 \end{bmatrix}$$. Then, using the matrix $$C$$ nested within $$B$$ to represent a continuation of the matrix $$B$$, we can write
<br>

$$
B = 
\begin{bmatrix} 
\lambda_{1} & \cdots & 0 \\
\vdots &   &  \\
0 &   &   C \\
\end{bmatrix}.
$$

<br>
We want to show that $$C$$ is diagonal. If we can do that, then $$B$$ must be diagonal, completing the proof. To prove this, we use induction on the dimension of the matrix $$B$$. In the base case, assume - as can be seen by the above matrix - that the matrix is diagonal up to the dimensions $$n-1 \times n-1$$. Then there must exist some orthogonal matrix $$Q$$ such that $$D = Q^{-1}CQ$$ is diagonal. Define another matrix 
<br>

$$
R = P \begin{bmatrix} 1 & 0 \\ 0 & Q \end{bmatrix}.
$$

<br>
We need to show that $$R$$ is orthogonal and that the expression for $$D = Q^{-1}CQ$$ is diagonal. Note that $$Q$$ is orthogonal, so $$Q^{T}=Q^{-1}$$. To prove orthogonality, compute 
<br>

$$
\begin{align*}
R^{-1} & 
= \bigg(P \begin{bmatrix} 1 & 0 \\ 0 & Q \end{bmatrix}\bigg)^{-1} \\ &
= \begin{bmatrix} 1 & 0 \\ 0 & Q \end{bmatrix}^{-1}P^{-1} \\ &
= \begin{bmatrix} 1 & 0 \\ 0 & Q^{T} \end{bmatrix} P^{T}
\end{align*}
$$

<br>
and
<br>

$$
\begin{align*}
R^{T} &
= \bigg(P \begin{bmatrix} 1 & 0 \\ 0 & Q \end{bmatrix}\bigg)^{T} \\ &
= \begin{bmatrix} 1 & 0 \\ 0 & Q^{T} \end{bmatrix} P^{T}, 
\end{align*}
$$

<br>
so $$R$$ is orthogonal. To show that $$R^{-1}AR$$ is diagonal, we have 
<br>

$$
\begin{align*}
R^{-1}AR & 
= R^{T}AR \\ &
= \begin{bmatrix} 1 & 0 \\ 0 & Q^{T} \end{bmatrix} A \begin{bmatrix} 1 & 0 \\ 0 & Q \end{bmatrix}. 
\end{align*}
$$

<br>
However, 
<br>

$$
B = P^{-1}AP = P^{T}AP = \begin{bmatrix} 
\lambda_{1} & \cdots & 0 \\
\vdots &   &  \\
0 &   &   C \\
\end{bmatrix}, 
$$

<br>
so ultimately we have 
<br>

$$
\begin{align*}
R^{-1}AR & 
= \begin{bmatrix} 1 & 0 \\ 0 & Q^{T} \end{bmatrix} \begin{bmatrix} \lambda_{1} & \cdots & 0 \\\vdots &   &  \\0 &   &   C \\ \end 
  {bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & Q \end{bmatrix} \\ &
= \begin{bmatrix} \lambda_{1} & 0 \\ 0 & Q^{T}C \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & Q \end{bmatrix} \\ &
= \begin{bmatrix} \lambda_{1} & 0 \\ 0 & Q^{T}CQ \end{bmatrix}. 
\end{align*}
$$

<br>
However - this is where it's really cool - we defined earlier that $$Q^{T}CQ$$ was the diagonal matrix $$D$$, so we simply have 
<br>

$$
\begin{align*}
R^{-1}AR = \begin{bmatrix} \lambda_{1} & 0 \\ 0 & D \end{bmatrix},
\end{align*}
$$

<br>
which is obviously a diagonal matrix. Thus, by induction on the dimension of the matrix $$B$$, we have shown that $$R^{-1}AR$$ is a diagonal matrix, and we are done. 
<br>
■
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
Now we will prove the forward direction. Note that since $$M$$ is normal, $$M^{\dagger}M=MM^{\dagger}$$. The proof follows by induction on $$\text{dim}(V)=d$$. When $$d=1$$, there is only one element in the vector space, and the operator $$M$$ is a $$1\times 1$$ diagonal matrix (because it can't be anything else), so this case is trivial. Let $$\lambda$$ be an eigenvalue of $$M$$, let $$P$$ be the projector onto the eigenspace for $$\lambda$$, and let $$Q$$ be the projector onto the orthogonal complement of $$P$$. Since $$P + Q = P + (I - P) = I$$, we can write
<br>

$$
\begin{align*}
M & = (P + Q)M(P + Q) \\ & = PMP + QMP + PMQ + QMQ.
\end{align*}
$$

<br>
We now need to determine several properties of these matrices. If we can show that $$M$$ is diagonal then we will be finished. First, notice that $$PMP=\lambda P$$ because $$PM$$ simply yields a scalar, namely the eigenvalue $$\lambda$$, and we then have $$PMP = \lambda P$$. Notice also that $$QMP = 0$$. This is because the operator $$M$$ maps $$P$$ to itself, so that $$MP\subseteq P$$. Since we said that $$Q$$ was the projector onto the space orthogonal to $$P$$, this must mean that $$QMP=0$$, which is also the zero operator. We will claim that $$PMQ=0$$ as well. To prove this, let $$|v\rangle$$ be an element of the vector subspace $$P$$. Then, since we assumed the normality of $$M$$, we have 
<br>

$$
M^{\dagger}M|v\rangle = MM^{\dagger}|v\rangle = \lambda M^{\dagger}|v\rangle. 
$$

<br>
This implies that $$M^{\dagger}|v\rangle$$ has the eigenvalue $$\lambda$$, so $$M^{\dagger}|v\rangle$$ is an element of the eigenspace for $$\lambda$$ for which $$P$$ is a projector. Thus we have that $$QM^{\dagger}P=0$$. Taking the adjoint of both sides, and since $$P$$ and $$Q$$ are both Hermitian, we have
<br>

$$
\begin{align*}
(QM^{\dagger}P)^{\dagger} & = 0^{\dagger} \\
Q^{\dagger}(M^{\dagger})^{\dagger}P^{\dagger} & = 0 \\
PMQ & = 0.
\end{align*}
$$

<br>
Since we have proven these two products are in fact equal to the zero operator, we now have that $$M = PMP + QMQ$$. We have to show that $$QMQ$$ is normal in order for us to show that $$M$$ is diagonalisable. Notice that $$QM = QMI = QM(P+Q) = QMP + QMQ = QMQ$$. Also notice that $$QM^{\dagger} = QM^{\dagger}I = QM^{\dagger}(P+Q) = QM^{\dagger}P + QM^{\dagger}Q = QM^{\dagger}Q$$. Then, since we have assumed normality of $$M$$, and due to the idempotence of the projector $$Q$$, we have
<br>

$$
\begin{align*}
QMQQM^{\dagger}Q & 
= QMQ^{2}M^{\dagger}Q \\ &
= QMQM^{\dagger}Q \\ & 
= QMM^{\dagger}Q \\ &
= QM^{\dagger}MQ \\ &
= QM^{\dagger}QQMQ,
\end{align*}
$$

<br>
so $$QMQ$$ is normal. By induction on $$d$$ from our inductive hypothesis, we have that $$QMQ$$ is diagonal with respect to some orthonormal basis for the subspace with the orthogonal complement $$Q$$, and we know that $$PMP$$ is diagonal since it is part of the eigenspace for which $$\lambda$$ is an eigenvalue. Thus it follows that $$QMQ + PMP = M$$ is diagonal with respect to some orthonormal basis for the original vector space $$V$$, and we are done. 
<br>
■
<br>
<br>
To understand the significance of this decomposition in terms of outer products, the spectral decomposition theorem guarantees that we can express some linear operator acting on Hilbert space as 
<br>

$$
M = \sum_{i}\lambda_{i}|i\rangle \langle i|,
$$

<br>
where the $$\lambda_{i}$$s are the eigenvalues of $$M$$, and $$|i\rangle$$ is an orthonormal basis for $$V$$ as well as an eigenvector of $$M$$ with eigenvalue $$\lambda_{i}$$. If we express this in terms of projectors, we have that 
<br>

$$
M = \sum_{i}\lambda_{i}P_{i},
$$

<br>
where $$P_{i}$$ is the projector onto the eigenspace for which $$\lambda_{i}$$ is an eigenvalue with $$M$$ of $$M$$. The projectors $$P_{i}$$ satisfy the completeness relation (existence of an identity operator) so that 
<br>

$$
\sum_{i}P_{i} = I,
$$

<br>
and satisfies the orthonormality relation so that for $$i$$ and $$j$$ not necessarily unique, $$P_{i}P_{j} = \delta_{ij}P_{i}$$, where $$\delta_{ij}$$ is the Kronecker delta. 
<br>
<br>
The reason that these two theorems are so important is that they allow us to easily determine the eigenvalues of a matrix. Since the eigenvalues of a diagonal matrix lie on the diagonal as can be shown through the characteristic equation, the spectral decomposition provides a diagonal representation of some linear operator and allows us to quickly determine the eigenvalues with respect to an orthonormal basis without having to repeat many different steps. 
<br>
<br>
(10 June, 2023)