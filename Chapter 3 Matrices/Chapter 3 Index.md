* [Definition of a Matrix](3.1%20Matrix%20Operations.html#definition-definition-of-a-matrix)

# Special Matrices

* [Definition of a Zero Matrix](3.1%20Matrix%20Operations.html#definition-zero-matrix)
* [Definition of a Square Matrix](3.1%20Matrix%20Operations.html#definition-square-matrix)
* [Definition of a Diagonal Matrix](3.1%20Matrix%20Operations.html#definition-diagonal-matrix)
* [Definition of a Scalar Matrix](3.1%20Matrix%20Operations.html#definition-scalar-matrix)
* [Definition of a Identity Matrix](3.1%20Matrix%20Operations.html#definition-identity-matrix)

# Matrix Addition and Scalar Multiplication

* [Definition of a Matrix Addition](3.1%20Matrix%20Operations.html#definition-matrix-addition)
  * [Example](3.1%20Matrix%20Operations.html#example): Adding two Matrices.
* [Definition of Scalar Multiplication](3.1%20Matrix%20Operations.html#definition-scalar-multiplication)
  * [Example](3.1%20Matrix%20Operations.html#example-scalar-matrix): Multiplying a Matrix by a Scalar.
* [Remarks for Matrix Addition and Scalar Multiplication](3.1%20Matrix%20Operations.html#remark-matrix-addition-and-scalar-multiplication) 
* [Properties of Matrix Addition and Scalar Multiplication](3.2%20Matrix%20Algebra.html#theorem-algebraic-properties-of-matrix-addition-and-scalar-multiplication)

# Matrix Multiplication

* [Definition of Matrix Multiplication](3.1%20Matrix%20Operations.html#definition-matrix-multiplication)
  * [Example](3.1%20Matrix%20Operations.html#example-multiplying-two-matrices): Multiplying two Matrices.
* [Remarks for Matrix Multiplication](3.1%20Matrix%20Operations.html#remark-matrix-multiplication)
* [Properties of Matrix Multiplication](3.2%20Matrix%20Algebra.html#theorem-properties-of-matrix-multiplication)

# The Transpose of a Matrix

* [Definition of the Transpose of a Matrix](3.1%20Matrix%20Operations.html#definition-transpose-of-a-matrix)
  * [Example](3.1%20Matrix%20Operations.html#example-finding-the-transpose): Finding the Transpose of a Matrix.
* [Definition of a Symmetric Matrix](3.1%20Matrix%20Operations.html#definition-symmetric-matrix)
* [Properties of the Transpose](3.2%20Matrix%20Algebra.html#theorem-properties-of-the-transpose)
* [Theorem](3.2%20Matrix%20Algebra.html#theorem-transpose-and-symmetric): If $A$ is a square matrix, the $A+A^{T}$ is a symmetric matrix.
* [Theorem](3.2%20Matrix%20Algebra.html#theorem-transpose-and-symmetric): For any matrix $A$, $AA^{T}$ and $A^{T}A$ are symmetric matrices.

# Inverse of a Matrix

* [Definition of the Inverse of a Matrix](3.3%20The%20Inverse%20of%20a%20Matrix.html#definition-invertible-matrix)
  * [Example](3.3%20The%20Inverse%20of%20a%20Matrix.html#example-proving-an-inverse-is-true): Proving that an Inverse is True.
  * [Example](3.3%20The%20Inverse%20of%20a%20Matrix.html#example-proving-a-matrix-is-not-invertible): Proving a Matrix isn't Invertible.
  * [Remark for Invertible Matrices](3.3%20The%20Inverse%20of%20a%20Matrix.html#remark-matrix-multiplication-and-inverses)
* [Properties of Invertible Matrices](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-properties-of-invertible-matrices)
  * [Remark for Properties of Invertible Matrices](3.3%20The%20Inverse%20of%20a%20Matrix.html#remark-properties-of-invertible-matrices)
* [Definition of Negative Matrix Powers](3.3%20The%20Inverse%20of%20a%20Matrix.html#definition-invertible-matrices-and-powers)
* [Theorem](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-inverse-of-2-x-2-matrices): If $A=\begin{bmatrix}a&b\\c&d\end{bmatrix}$, the $A$ is invertible if $ad-bc\neq0$, in which case: $A^{-1}=\frac{1}{ad-bc}\begin{bmatrix}d&-b\\-c&a\end{bmatrix}$. If $ad-bc=0$, then $A$ is not invertible.
* [Theorem](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-inverses-and-unique-solutions): If $A$ is an invertible matrix then its inverse is **unique**.
* [Theorem](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-invertible-matrices-and-systems-of-linear-equations): If $A$ is an invertible *n x n* matrix, then the system of linear equations given by $A\vec{x}=\vec{b}$ has the unique solution $\vec{x}=A^{-1}\vec{b}$ in $\mathbb{R}^{n}$.
* [Theorem](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-invertible-matrix-theorem): If $A$ and $B$ are square matrices such that either $AB=I$ or $BA=I$, then $A$ is invertible and $B=A^{-1}$.

# Elementary Matrices

* [Definition of an Elementary Matrix](3.3%20The%20Inverse%20of%20a%20Matrix.html#definition-elementary-matrix)
  * [Remark for Elementary Matrices](3.3%20The%20Inverse%20of%20a%20Matrix.html#remark-elementary-matrix)
* [Theorem](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-elementary-matrices-and-elementary-row-operations): Let $E$ be the elementary matrix obtained by performing an elementary row operation on $I\_{n}$. If the same elementary row operation is performed on an *n x r* matrix $A$, the result is the same as the matrix $EA$.
* [Theorem](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-invertibility-of-elementary-matrices): Each elementary matrix is invertible, and its inverse is an elementary matrix of the same type.
  * [Example](3.3%20The%20Inverse%20of%20a%20Matrix.html#example-invertibility-of-elementary-matrices): Finding the Inverse of an Elementary Matrix.

# [The Fundamental Theorem of Invertible Matrices Version 1](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-the-fundamental-theorem-of-invertible-matrices-version-1)

* [Theorem](3.3%20The%20Inverse%20of%20a%20Matrix.html#theorem-inverse-and-elementary-matrices): Let $A$ be a square matrix. If a sequence of elementary row operations reduce $A$ to $I$, then the same sequence of elementary row operation transform $I$ into $A^{-1}$.

# [The Gauss-Jordan Method for Computing the Inverse](3.3%20The%20Inverse%20of%20a%20Matrix.html#the-gauss-jordan-method-for-computing-the-inverse)

* [Remark for the Gauss-Jordan Method for Computing the Inverse](3.3%20The%20Inverse%20of%20a%20Matrix.html#the-gauss-jordan-method-for-computing-the-inverse-remark-the-gauss-jordan-method-for-computing-the-inverse)
* [Example](3.3%20The%20Inverse%20of%20a%20Matrix.html#example-the-gauss-jordan-method-for-computing-the-inverse): Showing a matrix is invertible and finding its inverse.

# Subspace

* [Definition of a Subspace](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#definition-subspace)
  * [Remark for the Definition of a Subspace](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#remark-subspace)
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-subspace-of-itself): $W=\mathbb{R}^{n}$ is a subspace of itself.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-zero-vector-and-subspaces): $W={\vec{0}}$ is a subspace of $\mathbb{R}^{n}$.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-determining-whether-a-set-is-a-subspace): Determining whether a set is a subset of $\mathbb{R}^{n}$.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-showing-a-set-is-a-subspace): Showing a set is a subset of $\mathbb{R}^{n}$.
* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-span-and-subspace): Let $\vec{v\_{1}},\vec{v\_{2}},\dots,\vec{v\_{k}}$ be vectors in $\mathbb{R}^{n}$. Then $span(\vec{v\_{1}},\vec{v\_{2}},\dots,\vec{v\_{k}})$ is a subspace of $\mathbb{R}^{n}$. 

# Subspaces Associated with Matrices

* [Definition of Row Space and Column Space](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#definition-row-space-and-column-space)
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-row-space-and-column-space): Determining whether a vector is in a given matrix's column space
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-row-space-and-column-space): Determining whether a vector is in a given matrix's row space.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-row-space-and-column-space): Describing the row and column spaces of a given matrix.
  * [Remark for Row Space and Column Space](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#remark-row-space-and-column-space)
* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-row-equivalence): Two *m x n* matrices $A$ and $B$ are **row equivalent** if either can be obtained from the other by applying a sequence of elementary row operations. As such, if $A$ and $B$ are **row equivalent**, then $Row(A)=Row(B)$. In particular, if $R$ is a row echelon form of $A$, then $Row(A)=Row(R)$.
* [Definition of Null Space](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#definition-null-space)
  * [Remark](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#remark-null-space): If $A$ and $R$ are row equivalent, then $Null(A)=Null(R)$. 
* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-solutions-to-a-vec-x-vec-b): Let $A$ be a *m x n* matrix and $\vec{b}\in\mathbb{R}^{m}$. The linear system $A\vec{x}=\vec{b}$ either has (1) no solution, (2) a unique solution, or (3) infinitely many solutions. 

# Basis

* [Definition](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#definition-basis): Basis.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-showing-a-set-is-a-basis): Showing that a set is a basis for $\mathbb{R}^{n}$.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-bases-and-standard-unit-vectors): The standard unit vectors in $\mathbb{R}^{n}$ form a basis for $\mathbb{R}^{n}$.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-find-a-row-space-s-basis): Finding the basis of a given matrix's row space.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-find-a-column-space-s-basis): Finding the basis of a given matrix's column space.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-find-a-null-space-s-basis): Finding the basis of a given matrix's null space.
  * [Remark for the Definition of a Basis](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#remark-basis) 

# Dimension and Rank

* [Definition of Dimension](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#definition-dimension)
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-dim-vec-0-0-because-vec-0-has-no-basis):  $dim(\vec{0})=0$ because $\vec{0}$ has no basis.
* [Definition of Rank](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#definition-rank)
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-1): Since the standard basis for $\mathbb{R}^{n}$, ${\vec{e\_{1}},\vec{e\_{2}},\dots,\vec{e\_{n}}}$, has $n$ vectors, then $dim(\mathbb{R}^{n})=n$.
  * [Example](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#example-2): Suppose $R$ is a row echelon form of a given matrix. Then, $dim(Row(R))=$ *\# number of rows in R* $=$ *\# of pivots of R* $=$ $rank(R)$.
* [Definition of Nullity](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#definition-nullity)
* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-the-basis-theorem): Let $S$ be a subspace of $\mathbb{R}^{n}$. Any two bases for $S$ have the same number of vectors.
* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-rank-and-transpose-equivalency): For any matrix $A$, $rank(A^{T})=rank(A)$.
* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-rank-nullity-theorem): If $A$ is an *m x n* matrix then, $rank(A)+nullity(A)=n$.

# [The Fundamental Theorem of Invertible Matrices: Version 2](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-the-fundamental-theorem-of-invertible-matrices-version-2)

* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-rank-and-transpose): $rank(A^{T}A)=rank(A)$.
* [Theorem](3.5%20Subspaces,%20Basis,%20Dimension,%20and%20Rank.html#theorem-rank-and-transpose): The *n x n* matrix $A^{T}A$ is invertible if and only if $rank(A)=n$.
