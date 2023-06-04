---
layout: page
title: Notes V
description: The Cauchy-Schwarz inequality and proofs
img: assets/img/bra ket.png
importance: 6
category: quantum mechanics research project (P)
---

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
<br>
(3 June, 2023)