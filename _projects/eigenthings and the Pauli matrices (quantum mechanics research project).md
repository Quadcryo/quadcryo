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
<br>
(4 June, 2023)
<br>





































(4 June, 2023)