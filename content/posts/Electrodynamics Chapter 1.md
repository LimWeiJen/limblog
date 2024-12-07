---
title: electrodynamics chapter 1
date: 2024-11-06
tags:
  - tag2
---

# 1.1 Vector Analysis
---
## Dot Product
$$
\begin{align}
\vec{A} \cdot \vec{B} & = |A||B|\cos \theta \\
\left(\begin{matrix}
i_{a} \\
j_{a} \\
k_{a}
\end{matrix}\right) \cdot
\left(\begin{matrix}
i_{b} \\
j_{b} \\
k_{b}
\end{matrix}\right) & =i_{a}i_{b}+j_{a}j_{b}+k_{a}k_{b}
\end{align}
$$
<p style="text-align: center">Dot products are distributive and commutative</p>
$$
\begin{align}
\vec{A} \cdot \vec{B} & = \vec{B} \cdot \vec{A} \\
\vec{A} \cdot (\vec{B} +\vec{C}) & =\vec{A} \cdot \vec{B}+\vec{A}\cdot \vec{C}
\end{align}
$$
---
## Cross Product
$$
\begin{align}
|\vec{A}\times \vec{B}| & =|\vec{A}||\vec{B}|\sin \theta\\
\vec{A}\times \vec{B} & =|\vec{A}||\vec{B}|\sin \theta \hat{n},\hat{n}\text{ is a unit vector perpendicular to both }\vec{A}\text{ and }\vec{B} \\
\left(\begin{matrix}
i_{a} \\
j_{a} \\
k_{a}
\end{matrix}\right) \times
\left(\begin{matrix}
i_{b} \\
j_{b} \\
k_{b} \\
\end{matrix}
\right) & =\left|
\begin{matrix}
\hat{i} & \hat{j} & \hat{k} \\
i_{a} & j_{a} & k_{a} \\
i_{b} & j_{b} & k_{b}
\end{matrix}
\right|
\end{align}
$$
<p style="text-align: center">Cross products are distributive but not commutative</p>
$$
\begin{align}
\vec{A}\times(\vec{B}+\vec{C}) & =(\vec{A}\times \vec{B})+(\vec{A}\times \vec{C}) \\
\vec{A}\times \vec{B} & =-(\vec{B}\times \vec{A})
\end{align}
$$

Geometrically, cross product is the area of the parallelogram formed by the two vectors.
!![Image Description](/images/Pasted%20image%2020241207155118.png)

--- 
## Vector Algebra
$$
\begin{align}
\text{if }\vec{A} & =A_{i}\hat{i}+A_{j}\hat{j}+A_{k}\hat{k} \\
\text{then }|\vec{A}| & =\sqrt{ A_{i}^2+A_{j}^2 +A_{k}^2}
\end{align}
$$
---
## Triple Products
$$
\begin{align}
\text{Area of the cube} & =(\vec{B} \times \vec{C})\cdot \vec{A}=(\vec{B}\times \vec{A})\cdot \vec{C}=(\vec{A}\times \vec{C})\cdot{\vec{B}} \\
 & =\left|
\begin{matrix}
A_{i} & A_{j} & A_{k} \\
B_{i} & B_{j} & B_{k} \\
C_{i} & C_{j} & C_{k}
\end{matrix}
\right|
\end{align}
$$
---
