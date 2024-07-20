---
title: "Exercises in linear algebra"
date: 2024-07-19T10:50:10+09:00
lastmod: 2024-07-20
draft: false
params:
  math: true
---

Page created on *19 July 2024*

Last modified on *20 July 2024*

## I. Eigenvalue problems
As a review, the eigenvalue problem of a given matrix $\mathbf{M}$ is
{{< raw >}}
\[
\mathbf{M} \vec{v} = \lambda \vec{v}.
\]
The vector $\vec{v}$ is an eigenvector and the scalar $\lambda$ is the corresponding eigenvalue.
{{< /raw >}}

### I.1 Eigenvalues of a symmetric matirx
We haven't talked about how to solve the eigenvalue problem from scratch.
So, here, we write down a matrix and I will tell you the eigenvectors.
You try calculting the corresponding eignevalues.
Here is the matrix
{{< raw >}}
\[
\mathbf{S} =
\begin{pmatrix}
1 & 3 \\
3 & 1 
\end{pmatrix},
\]
{{< /raw >}}
and I tell you its two eigenvectors are
{{< raw >}}
\[
\vec{v}_1 =
\begin{pmatrix}
1 \\
1 
\end{pmatrix},
\vec{v}_2 =
\begin{pmatrix}
1 \\
-1 
\end{pmatrix}.
\]
{{< /raw >}}
Please calculate the corresponding eigenvalues.

### I.2 Eigendecomposition of a matrix 
Try writing the two eigenvalues equations of the above exercise as an eigendecomposition of the matrix $\mathbf{S} = \mathbf{Q} \mathbf{\Lambda} \mathbf{Q}^{-1}$.
Wrtie down the $\mathbf{Q}$ and $\mathbf{\Lambda}$ matrices and plug them into the right-hand side to check whether you reproduce the matrix $\mathbf{S}$.

- Hint 1. The two columns of $\mathbf{Q}$ are two eigenvectors and the eigenvalues are in the diagonal matrix $\mathbf{\Lambda}$.
- Hint 2. Since the matrix $\mathbf{S}$ is symmetric, the matrix $\mathbf{Q}$ *can be made as orthgonal matrix* if you rescale the eigenvecotors to ensure that they have unit length (In the above expression I gave you, they both have length $\sqrt{2}$).
    For an orthogonal matrix, the inverse is just its transpose $\mathbf{Q}^{-1} = \mathbf{Q}^{\top}$.


## II. Inner product 
> Hey, I will add some exercises when I have ideas.
> Come back and check later!
