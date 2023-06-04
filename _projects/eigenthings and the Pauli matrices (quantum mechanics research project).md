---
layout: page
title: Notes VI
description: Eigenthings and the Pauli matrices
img: assets/img/bra ket.png
importance: 7
category: quantum mechanics research project (P)
---

<h2>
Eigenthings and the Pauli matrices
</h2>

<br>
As indicated by the title, we will be focusing on eigenthings, namely eigenvectors, eigenvalues, and eigendecomposition (aka diagonalisation). We will also be investigating the Pauli matrices a little bit, which we will derive later once I learn more. 
<br>
<br>
An eigenvector of a linear operator $$A$$ on a vector space is a vector $$|v\rangle \in V$$ such that $$A|v\rangle = \lambda |v\rangle$$, where $$\lambda$$ denotes the eigenvalue, and is a number scalar. An intuitive approach to understanding the eigenvector and eigenvalue is to visualize a vector being transformed. The linear operator $$A$$ transforms $$|v\rangle$$, and $$\lambda$$ does as well. When the resulting transformation of $$|v\rangle$$ by $$A$$ and $$\lambda$$ is equivalent, the $$|v\rangle$$ on which the transformation has been acted upon is known as the eigenvector. 
<br>
<br>
Consider some matrix 
<br>

$$
\begin{equation*}
A = 
\begin{bmatrix} 
a & b \\
c & d
\end{bmatrix}.
\end{equation*}
$$

<br>
If we rearrange the eigenthing equation from above, we have
<br>

$$
\begin{align*}
A|v\rangle & = \lambda |v\rangle \\ 
A|v\rangle - \lambda |v\rangle & = 0 \\
(A-\lambda I)|v\rangle & = 0 \\
\text{det}( A-\lambda I ) & = 0.
\end{align*}
$$

<br>
We refer to the $$LHS$$ of the above as the "characteristic polynomial", and if we find the roots of the characteristic equation, then we can determine the eigenvalues. The characteristic equation can be solved for the eigenvalues as follows:
<br> 

$$
\begin{align*}
\text{det}( A-\lambda I ) & = 0 \\
\text{det} \bigg( 
\begin{bmatrix} a & b \\ c & d \end{bmatrix} \bigg)
- \begin{bmatrix} \lambda & 0 \\ 0 & \lambda \end{bmatrix} & = 0 \\
\text{det} \bigg( 
\begin{bmatrix} a - \lambda & b \\ c & d - \lambda \end{bmatrix} \bigg) & = 0 \\
bc - (a - \lambda)(d - \lambda) & = 0.
\end{align*}
$$

<br>
We define an eigenspace to be the set of vectors with eigenvalue $$\lambda$$. If you think about it, the eigenspace is thus a vector subspace corresponding to some fixed eigenvalue (as not all vectors will have the same eigenvalue) on which the linear opeartor $$A$$ acts. 
<br>
<br>
We say that some matrix is diagonisable if it has a diagonal representation. For some linear operator to have a diagonal representation, it must be possible for us to determine its eigenvalues and eigenvectors. The process of finding the eigenvalues and eigenvectors is usually just known as eigendecomposition or diagonalisation. Let $$|i\rangle$$ be an orthonormal set of vectors on a vector space $$V$$. The diagonal representation of the linear operator $$A$$ on $$V$$ is 
<br>

$$
\begin{equation} A = \sum_{i}\lambda_{i}|i\rangle \langle i| = \lambda_{i}I \end{equation} \label{eq:1}.
$$

<br>
Before we proceed to determine the diagonalised form of several linear operators, let us first introduce the Pauli matrices. The Pauli matrices are known as "Pauli spin matrices", as they are the main factors in determining spin. We will in fact discover that the Pauli matrices are Hermitian, and that they possess an incredibly unique function later on. The Pauli spin matrices are as follows: 
<br>

$$
\begin{equation*}
\begin{array}{ll}
    \sigma_{0}=I=\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} & \sigma_{2}=\sigma_{y}=Y=\begin{bmatrix} 0 & -i \\ i & 0 \end{bmatrix} \\
    \sigma_{1}=\sigma_{x}=X=\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} &  \\ \sigma_{3}=\sigma_{z}=Z=\begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}, 
\end{array}
\end{equation*}
$$

<br>
where $$i=\sqrt{-1}$$. Let us diagonalise these matrices and determine their diagonal representations. Beginning with $$I$$, we have 
<br>

$$
\begin{align*}
\text{det}\bigg( \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} - \begin{bmatrix} \lambda & 0 \\ 0 & \lambda \end{bmatrix} \bigg) & = 0 \\
\text{det}\bigg( \begin{bmatrix} 1-\lambda & 0 \\ 0 & 1-\lambda \end{bmatrix} \bigg) & = 0 \\
(1-\lambda)(1-\lambda) & = 0 \\
\lambda & = 1, 1. 
\end{align*}
$$

<br>
To find the eigenvectors, notice that we are trying to solve the matrix equation
<br>

$$
\begin{align*}
\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} x \\ y  \end{bmatrix} & = \begin{bmatrix} x \\ y  \end{bmatrix} \\
\begin{bmatrix} x \\ y  \end{bmatrix} & = \begin{bmatrix} x \\ y  \end{bmatrix}.
\end{align*}
$$

<br>
This is already in diagonalised form, so the eigenvectors are
<br>

$$
\begin{bmatrix} 1 \\ 0  \end{bmatrix} \\ \text{and} \\ \begin{bmatrix} 0 \\ 1  \end{bmatrix}.
$$

<br>
Thus the diagonal representation is $$I=|1\rangle \langle 0| - |0\rangle \langle 1|$$. 
<br>
<br>
This process can be repeated for all other Pauli matrices. Thus the diagonal representations of the other Pauli matrices are $$|1\rangle \langle 1| - |1\rangle \langle -1|$$, $$|1\rangle \langle i| - |1\rangle \langle -i|$$, and $$|1\rangle \langle 0| - |0\rangle \langle 1|$$ for $$X$$, $$Y$$, and $$Z$$ respectively. We will investigate these further soon. 
<br>
(4 June, 2023)
<br>