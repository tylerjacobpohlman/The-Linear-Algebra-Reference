# Vector Spaces

* \[\[6.1 Vector Spaces and Subspaces#Remark $ mathbb{R} {n}$, $ mathbb{P}*{n}$, and $M*{m,n}$ and their Respective Operations|Remark\]\]: Definitions of $\mathbb{R}^{n}$, $\mathbb{P}*{n}$, and $M*{m,n}$.
* [Definition](6.1%20Vector%20Spaces%20and%20Subspaces.md#definition-vector-spaces-and-vectors): Vector Spaces and Vectors.
  * [Remark](6.1%20Vector%20Spaces%20and%20Subspaces.md#remark-mathbb-r-n-is-a-vector-space): $\mathbb{R}^{n}$ is a Vector Space.
  * [Remark](6.1%20Vector%20Spaces%20and%20Subspaces.md#remark-mathbb-p-n-is-a-vector-space): $\mathbb{P}^{n}$ is a Vector Space.
  * [Remark](6.1%20Vector%20Spaces%20and%20Subspaces.md#remark-m-m-n-is-a-vector-space): $M\_{m,n}$ is a Vector Space.
  * [Remark](6.1%20Vector%20Spaces%20and%20Subspaces.md#remark-mathcal-f-is-a-vector-space): $\mathcal{F}$ is a Vector Space.
  * [Remark](6.1%20Vector%20Spaces%20and%20Subspaces.md#remark-all-continuous-functions-are-vector-spaces): All Continuous Functions are Vector Spaces.
  * [Remark](6.1%20Vector%20Spaces%20and%20Subspaces.md#remark-all-differentiable-functions-are-vector-spaces): All Differentiable Functions are Vector Spaces.
  * [Example](6.1%20Vector%20Spaces%20and%20Subspaces.md#example-examples-of-vector-spaces): Examples of Vector Spaces.
  * [Example](6.1%20Vector%20Spaces%20and%20Subspaces.md#example-non-examples-of-vector-spaces): Non-Examples of Vector Spaces.

# Subspaces

* [Definition](6.1%20Vector%20Spaces%20and%20Subspaces.md#definition-subspace): Subspaces.
  * [Example](6.1%20Vector%20Spaces%20and%20Subspaces.md#example-examples-of-subspaces): Examples of Subspaces.
* [Theorem](6.1%20Vector%20Spaces%20and%20Subspaces.md#theorem-subspace-characterization-theorem): Let $V$ be a vector space and let $W$ be a nonempty subset of $V$. Then $W$ is a subspace of $V$ if and only if the following conditions hold:
  1. $\vec{0} \in W$.
  1. If $\vec{u}, \vec{v}\in W$, then $\vec{u}+\vec{v}\in W$.
  1. If $\vec{v}\in W$ and $c\in\mathbb{R}$, then $c\vec{v}\in W$.

# Spanning Sets

* [Definition](6.1%20Vector%20Spaces%20and%20Subspaces.md#definition-spanning): Spanning.

# Linear Independence

* [Definition](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#definition-linear-combination): Linear Combination.
* [Definition](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#definition-linear-independence-and-linear-dependence): Linear Independence and Linear Dependence.
* [Theorem](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#theorem-linear-dependence-theorem): Let $V$ be a vector space with the vectors $\vec{v}*{1}, \dots, \vec{v}*{k} \in V$. The set $\left{ \vec{v}*{1}, \dots, \vec{v}*{k} \right}$ is linearly dependent if and only if at least one of the vectors can be expressed as a linear combination of the others.
  * [Example](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#example-is-left-1-ln-x-ln-2x-right-a-linearly-independent-subset-of-mathcal-f): Determining whether $\left{ 1, \ln x, \ln(2x) \right}$ a linearly independent subset of $\mathcal{F}$.
* [Definition](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#definition-basis): Basis.
  * [Example](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#example-what-s-the-basis-for-m-2-2): Finding the basis for $M\_{2,2}$.
  * \[\[6.2 Linear Independence Basis and Dimension#Example What's the basis for *2 x 2* upper triangular matrices?|Example\]\]: Finding the basis for *2 x 2* upper triangular matrices.

# Coordinates

* [Theorem](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#theorem-basis-representation-theorem): Let $V$ be a vector space and let $\mathcal{B}$ be a basis for $V$. For every vector $\vec{v} \in V$, there is exactly one way to write $\vec{v}$ as a linear combination of the basis vectors in $\mathcal{B}$. In other words, if $c\_{1}, \dots, c\_{k} \in \mathbb{R}$ and $\mathcal{B} = {\vec{v}*{1}, \dots, \vec{v}*{k}}$ is a basis for $V$, then $\vec{v} = c\_{1}\vec{v}*{1} + \dots + c*{k}\vec{v}*{k}$ can be written with only one unique set of scalars $c*{1}, \dots, c\_{k}$.
* [Definition](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#definition-b-coordinates): B-Coordinates.
  * \[\[6.2 Linear Independence Basis and Dimension#Example Finding the $ mathcal{B}$-Coordinates of Subsets of $ mathbb{P}*{2}$|Example\]\]: Finding the $\mathcal{B}$-Coordinates of Subsets of $\mathbb{P}*{2}$.
* [Theorem](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#theorem-coordinate-vector-properties): Let $\mathcal{B}=\left{ \vec{v}*{1},\dots,\vec{v}*{k} \right}$ be a basis for a vector space $V$. Also, let $\vec{u},\vec{v}\in V$ and let $c\in\mathbb{R}$. Then
  1. $\[\\vec{u}+\vec{v}\]*{\mathcal{B}}=\[\\vec{u}\]*{\mathcal{B}}+\[\\vec{v}\]\_{\mathcal{B}}$.
  1. $\[c\vec{v}\]*{\mathcal{B}}=c\[\\vec{v}\]*{\mathcal{B}}$.
* [Theorem](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#theorem-linear-independence-theorem): let $\mathcal{B}=\left{\vec{v}*{1},\dots,\vec{v}*{n}\right}$ be a basis for a vector space $V$ and let the vectors $\vec{v}*{1},\dots,\vec{v}*{k}\in V$. Then the set $\left{ \vec{u}*{1},\dots,\vec{u}*{k} \right}$ is linearly independent in $V$ if and only if $\left{ \[\\vec{u}*{1}\]*{\mathcal{B}},\dots,\[\\vec{u}*{k}\]*{\mathcal{B}} \right}$ is linearly independent in $\mathbb{R}^{n}$.
* [Theorem](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#theorem-properties-of-basis-and-dimension): let $\mathcal{B}=\left{\vec{v}*{1},\dots,\vec{v}*{n}\right}$ be a basis for a vector space $V$.
  1. Any set of more than $n$ vectors in $V$ is linearly independent.
  1. Any set of fewer than $n$ vectors in $V$ doesn't span $V$.
* [Theorem](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#theorem-the-basis-theorem): If a vector space $V$ has a basis with $n$ vectors, then every basis for $V$ has exactly $n$ vectors.
* [Theorem](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#theorem-basis-extension-theorem): Let $V$ be a vector space where $\dim V = n$. Then:
  1. Any set consisting of more than $n$ vectors in $V$ is linearly dependent.
  1. Any set consisting of fewer than $n$ vectors in $V$ does not span $V$.
  1. Any linearly independent set of $n$ vectors in $V$ is a basis for $V$.
  1. Any set consisting of $n$ vectors that spans $V$ is a basis for $V$.
  1. Any linearly independent set in $V$ can be extended to a basis for $V$.
  1. Any spanning set for $V$ can be reduced to a basis for $V$.
* [Definition](6.2%20Linear%20Independence%20Basis%20and%20Dimension.md#definition-dimension-of-a-vector-space): Dimension of a Vector Space.

# Change-of-Basis

* [Remark](6.3%20Change%20of%20Basis.md#remark-relationship-between-b-coordinates-of-the-same-vector): Relationship Between B-Coordinates of the Same Vector.
* [Definition](6.3%20Change%20of%20Basis.md#definition-change-of-basis-matrix): Change-of-Basis Matrix.
* [Theorem](6.3%20Change%20of%20Basis.md#theorem-properties-of-change-of-basis-matrices): Let $\mathcal{B} = {\vec{u}\_1, \ldots, \vec{u}\_n}$ and $\mathcal{C} = {\vec{v}\_1, \ldots, \vec{v}*n}$ be bases for a vector space $V$ and let $P*{\mathcal{C} \leftarrow \mathcal{B}}$ be the change-of-basis matrix from $\mathcal{B}$ to $\mathcal{C}$. Then,
  1. $P\_{\mathcal{C} \leftarrow \mathcal{B}} \[\\vec{x}\]*{\mathcal{B}} = \[\\vec{x}\]*{\mathcal{C}}$ for all $\vec{x}$ in $V$.
  1. $P\_{\mathcal{C} \leftarrow \mathcal{B}}$ is the unique matrix $P$ with the property that $P \[\\vec{x}\]*{\mathcal{B}} = \[\\vec{x}\]*{\mathcal{C}}$ for all $\vec{x}$ in $V$.
  1. $P\_{\mathcal{C} \leftarrow \mathcal{B}}$ is invertible and $(P\_{\mathcal{C} \leftarrow \mathcal{B}})^{-1} = P\_{\mathcal{B} \leftarrow \mathcal{C}}$.
* [Example](6.3%20Change%20of%20Basis.md#example-finding-the-change-of-bases-matrices-in-the-vector-space-mathbb-r-2): Finding the Change-of-Bases Matrices in the Vector Space $\mathbb{R}^{2}$.
* [Example](6.3%20Change%20of%20Basis.md#example-finding-the-change-of-bases-matrices-in-the-vector-space-mathbb-p-1): Finding the Change-of-Bases Matrices in the Vector Space $\mathbb{P}^{1}$.

# Linear Transformations

* [Definition](6.4%20Linear%20Transformations.md#definition-linear-transformations): Linear Transformations.
  * [Remark](6.4%20Linear%20Transformations.md#remark-alternative-definition-of-linear-transformations): Alternative Definition for Linear Transformations.
  * [Example](6.4%20Linear%20Transformations.md#example-proving-the-transpose-of-a-matrix-is-a-linear-transformation): Proving the Transpose of a Matrix is a Linear Transformation.
  * [Example](6.4%20Linear%20Transformations.md#example-differentiating-a-function-is-a-linear-transformation): Proving that Differentiating Functions is a Linear Transformation.
  * [Example](6.4%20Linear%20Transformations.md#example-proving-integrating-functions-is-a-linear-transformation): Proving that Integrating Functions is a Linear Transformation.
  * [Remark](6.4%20Linear%20Transformations.md#remark-the-zero-vector-and-linear-transformations): The Zero Vector and Linear Transformations.

# The Kernel and Range of a Linear Transformation

* [Definition](6.5%20The%20Kernel%20and%20Range%20of%20a%20Linear%20Transformation.md#definition-kernel): Kernel.
* [Definition](6.5%20The%20Kernel%20and%20Range%20of%20a%20Linear%20Transformation.md#definition-image): Image.
