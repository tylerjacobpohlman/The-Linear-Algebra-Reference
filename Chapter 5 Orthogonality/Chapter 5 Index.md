# Orthogonal and Orthonormal Sets of Vectors

* [Definition](5.1%20Orthogonality.md#definition-orthogonal-set): Orthogonal sets.
  * [Example](5.1%20Orthogonality.md#example-standard-unit-vectors-form-an-orthogonal-set): The stand unit vectors ${e\_{1},e\_{2},\dots,e\_{n}}$ form an orthogonal set for $\mathbb{R}^{n}$.
  * [Example](5.1%20Orthogonality.md#example-orthogonal-set-in-mathbb-r-2): An orthogonal set in $\mathbb{R}^{2}$.
* [Theorem](5.1%20Orthogonality.md#theorem-orthogonal-set-independence-theorem): Every set of orthogonal nonzero vectors in $\mathbb{R}^{n}$, $\left{\vec{v\_{1}}, \vec{v\_{2}}, \dots, \vec{v\_{n}}\right}$, is linearly independent.
* [Definition](5.1%20Orthogonality.md#definition-orthogonal-basis): Orthogonal Bases.
* [Theorem](5.1%20Orthogonality.md#theorem-orthogonal-projection-theorem): Let $W=\left{ \vec{v\_{1}},\vec{v\_{2}},\dots,\vec{v\_{k}} \right}$ be an orthogonal set of nonzero vectors in $\mathbb{R}^{n}$ and let $\vec{w}\in W$. Then the  unique scalar $c\_{1},c\_{2},\dots,c\_{k}$ such that $\vec{w} = c\_{1}\vec{v\_{1}}+c\_{2}\vec{v\_{2}}+\dots+c\_{k}\vec{v\_{k}} = \sum\_{i=1}^kc\_{i}\vec{v\_{i}}$ are give by $c\_{i} = \frac{\vec{w}\cdot\vec{v\_{i}}}{\vec{v\_{i}}\cdot\vec{v\_{i}}}$ for $i=1,2,\dots,k$.
* [Definition](5.1%20Orthogonality.md#definition-orthonormal-sets-and-orthonormal-bases): Orthonormal Sets and Orthonormal Bases.
  * [Remark](5.1%20Orthogonality.md#remark-orthonormal-sets): If $\left{ \vec{q\_{1}},\vec{q\_{2}},\dots,\vec{q\_{k}} \right}$ is an orthonormal set then: $\vec{q\_{i}} \cdot \vec{q\_{j}} = 0$ if $i \neq j$ and $\vec{q\_{i}} \cdot \vec{q\_{j}} = 1$ if $i = j$.
  * [Remark](5.1%20Orthogonality.md#remark-dot-product-as-matrix-multiplication): $\vec{x}^{T}\vec{y}=\vec{x}\cdot\vec{y}$.

# Orthogonal Matrices

* [Definition](5.1%20Orthogonality.md#definition-orthogonal-matrix): Orthogonal Matrices.
  * [Example](5.1%20Orthogonality.md#example-i-n-is-an-orthogonal-matrix):  $I\_{n}$ is an orthogonal matrix.
* [Theorem](5.1%20Orthogonality.md#theorem-orthonormal-columns-theorem): Let $Q$ be an *n x m* matrix. The columns of $Q$ forms an orthonormal set if and only if $Q^{T}Q=I\_{n}$.
* [Theorem](5.1%20Orthogonality.md#theorem-orthogonal-matrix-theorem): An *n x n* square matrix $Q$ is orthogonal if and only if $Q^{-1}=Q^{T}$.
* [Theorem](5.1%20Orthogonality.md#theorem-equivalent-conditions-for-orthogonality-theorem): Let $Q$ be an *n x n* matrix. The following conditions are equivalent:
  1. $Q$ is orthogonal.
  1. $|Q\vec{x}|=|\vec{x}|$ for every $\vec{x},\vec{y}\in\mathbb{R}^{n}$.
  1. $Q\vec{x}\cdot Q\vec{x} = \vec{x}\cdot\vec{y}$ for every $\vec{x},\vec{y}\in\mathbb{R}^{n}$.
* [Theorem](5.1%20Orthogonality.md#theorem-orthonormality-of-rows-of-an-orthogonal-matrix): If $Q$ is an orthogonal matrix, then the rows of $Q$ form an orthogonal set.
* [Theorem](5.1%20Orthogonality.md#theorem-properties-of-orthogonal-matrices): Let $Q$ be an orthogonal matrix.
  1. $Q^{-1}$ is orthogonal.
  1. $detQ=\pm 1$.
  1. If $\lambda$ is an eigenvalue of $Q$, $|\lambda|=1$.
  1. If $Q\_{1}$ and $Q\_{2}$ are orthogonal *n x n* matrices, then so is $Q\_{1}Q\_{2}$.

# Orthogonal Complements

* [Definition](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#definition-orthogonal-complement): Orthogonal Complement.
* [Theorem](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#theorem-properties-of-the-orthogonal-complements): Let $W$ be a subspace of $\mathbb{R}^{n}$.
  1. $W^{\perp}$ is a subspace of $\mathbb{R}^{n}$.
  1. $(W^{\perp})^{\perp}=W$.
  1. $W\cap W^{\perp}=\left{ 0 \right}$.
  1. If $W=span(\vec{w\_{1}},\vec{w\_{2}},\dots,\vec{w\_{k}})$, then $\vec{v}\in W^{\perp}$ if and only if $\vec{v}\cdot\vec{w\_{i}}=0$ for all $i=1,2,\dots,k$. 
* [Theorem](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#theorem-orthogonal-complements-with-row-column-and-null-spaces): Let $A$ be an *n x n* matrix. $(row(A))^{\perp}=null(A)$ and $(col(A))^{\perp}=null(A^{T})$.
* [Example](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#example-finding-a-basis-of-an-orthogonal-complement): Finding a Basis of an Orthogonal Complement.

# Orthogonal Projections

* [Definition](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#definition-orthogonal-projection): Orthogonal Projection.
* [Theorem](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#theorem-the-decomposition-theorem-for-projections-and-orthogonal-complements): Let $\left{ \vec{u\_{1}},\vec{u\_{2}},\dots,\vec{u\_{k}} \right}$ be an orthogonal basis for a subspace $W\subseteq\mathbb{R}^{n}$ and let $W^{\perp}$ be the orthogonal complement of $W$.  For any vector $\vec{v}\in\mathbb{R}^{n}$, $\text{proj}\_{W} (\vec{v})\in W$ and $\text{perp}\_W (\vec{v})\in W^{\perp}$.
* [Theorem](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#theorem-the-orthogonal-decomposition-theorem): Let $W\subseteq\mathbb{R}^{n}$ be a subspace and let $\vec{v}\in\mathbb{R}^{n}$ be a vector. Then there are unique vectors $\vec{w}\in W$ and $\vec{w}^{\perp}\in W^{\perp}$ such that: $\vec{v}=\vec{w}+\vec{w}^{\perp}$.
* [Theorem](5.2%20Orthogonal%20Complements%20and%20Orthogonal%20Projections.md#theorem-dimension-theorem-for-subspaces): If $W\subseteq\mathbb{R}^{n}$ is a subspace, then: $dimW+dimW^{\perp}=n$.

# The Gram-Schmidt Process

* [Theorem](5.3%20The%20Gram-Schmidt%20Process%20and%20the%20QR%20Factorization.md#theorem-the-gram-schmidt-process): The Gram-Schmidt Process. 
  Let $\left{ \vec{x\_{1}},\vec{x\_{2}},\dots,\vec{x\_{k}} \right}$ be a basis for a subspace $W$ of $\mathbb{R}^{n}$ and define the following: $\vec{v}*{1}=\vec{x}*{1}$, $\vec{v}*{2}=\vec{x}*{2}-\text{proj}*{\vec{v}*{1}} (\vec{x}*{2})$, $\vec{v}*{3}=\vec{x}*{3}-\text{proj}*{\vec{v}*{1}} (\vec{x}*{3})-\text{proj}*{\vec{v}*{2}} (\vec{x}*{3})$, $\dots$, $\vec{v}*{k} = \vec{x}*{k} - \sum*{i=1}^{k-1}\text{proj}*{\vec{v}*{i}} (\vec{x}*{k})$. Then $\left{ \vec{v}*{1},\vec{v}*{2},\dots,\vec{v}*{k} \right}$ is an [orthogonal basis](5.1%20Orthogonality.md#definition-orthogonal-basis) for $W$. In particular, for each $i=1,2,\dots,k$, $\left{ \vec{v}*{1},\dots,\vec{v}*{i} \right}$ is an orthogonal basis for $\text{Span}\left{ \vec{x}*{1},\dots,\vec{x}*{i} \right}$.
  * [Remark](5.3%20The%20Gram-Schmidt%20Process%20and%20the%20QR%20Factorization.md#remark-purpose-of-the-gram-schmidt-process): Purpose of the Gram-Schmidt Process.
  * [Remark](5.3%20The%20Gram-Schmidt%20Process%20and%20the%20QR%20Factorization.md#remark-finding-an-orthonormal-basis): Finding an orthonormal basis.
  * [Example](5.3%20The%20Gram-Schmidt%20Process%20and%20the%20QR%20Factorization.md#example-using-the-gram-schmidt-process-to-find-an-orthogonal-basis): Using the Gram-Schmidt Process to find an Orthogonal Basis.

# The QR Factorization

* [Theorem](5.3%20The%20Gram-Schmidt%20Process%20and%20the%20QR%20Factorization.md#theorem-the-qr-factorization): The QR Factorization. 
  Let $A$ be an *m x n* matrix whose columns are linearly independent. Then $A$ can be written as: $A=QR$ where $Q$ is an *m x n* matrix [orthogonal matrix](5.1%20Orthogonality.md#definition-orthogonal-matrix) and $R$ is an [invertible](../Chapter%203%20Matrices/3.3%20The%20Inverse%20of%20a%20Matrix.md#definition-invertible-matrix) upper triangular matrix.
  * [Example](5.3%20The%20Gram-Schmidt%20Process%20and%20the%20QR%20Factorization.md#example-finding-the-qr-factorization-of-a-matrix): Finding the QR Factorization of a Matrix.

# Orthogonal Diagonalization of Symmetric Matrices

* [Remark](5.4%20Orthogonal%20Diagonalization%20of%20Symmetric%20Matrices.md#remark-matrices-may-have-non-real-eigenvalues): Matrices May Have Non-Real Eigenvalues.
* [Remark](5.4%20Orthogonal%20Diagonalization%20of%20Symmetric%20Matrices.md#remark-matrices-may-have-real-eigenvalues-and-not-be-diagonalizable): Matrices May Have Real Eigenvalues and Not Be Diagonalizable.
* [Definition](5.4%20Orthogonal%20Diagonalization%20of%20Symmetric%20Matrices.md#definition-orthogonally-diagonalizable): Orthogonally Diagonalizable.
* [Theorem](5.4%20Orthogonal%20Diagonalization%20of%20Symmetric%20Matrices.md#theorem-orthogonal-diagonalization-symmetry-theorem): If an *n x n* matrix $A$ is orthogonally diagonalizable, then $A$ is symmetric.
* [Theorem](5.4%20Orthogonal%20Diagonalization%20of%20Symmetric%20Matrices.md#theorem-real-eigenvalue-theorem-for-symmetric-matrices): If a *n x n* matrix $A$ is a real [symmetric matrix](../Chapter%203%20Matrices/3.1%20Matrix%20Operations.md#definition-symmetric-matrix), then the [eigenvalues](../Chapter%204%20Eigenvalues%20and%20Eigenvectors/4.1%20Eigenvalues%20and%20Eigenvectors.md#definition-eigenvalue-and-eigenvector) of $A$ are real.
* [Theorem](5.4%20Orthogonal%20Diagonalization%20of%20Symmetric%20Matrices.md#theorem-orthogonal-eigenvectors-theorem-for-symmetric-matrices): If $A$ is symmetric then any two eigenvectors associated to *distinct* eigenvalues are orthogonal.
* [Theorem](5.4%20Orthogonal%20Diagonalization%20of%20Symmetric%20Matrices.md#theorem-spectral-theorem): Spectral Theorem.
  An *n x n* matrix $A$ is orthogonally diagonalizable if and only if $A$ is symmetric.
