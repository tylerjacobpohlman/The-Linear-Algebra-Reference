# Eigenvalues and Eigenvectors

* [Definition](4.1%20Eigenvalues%20and%20Eigenvectors.md#definition-eigenvalue-and-eigenvector): Eigenvalues and Eigenvectors.
  * [Remark](4.1%20Eigenvalues%20and%20Eigenvectors.md#remark-the-zero-vector-for-eigenvectors-and-0-for-eigenvalues): The zero vector, $\vec{0}$, is **never** an eigenvector, but $\lambda=0$ **could be** an eigenvalue.
  * [Example](4.1%20Eigenvalues%20and%20Eigenvectors.md#example-showing-that-a-vector-is-an-eigenvector-of-a-matrix): Showing that a vector is an eigenvector of a matrix.
* [Definition](4.1%20Eigenvalues%20and%20Eigenvectors.md#definition-eigenspace): Eigenspace.
  * [Example](4.1%20Eigenvalues%20and%20Eigenvectors.md#example-finding-the-eigenspace-of-a-matrix-given-an-eigenvalue): Finding the eigenspace of a matrix given an eigenvalue.
* [Theorem](4.1%20Eigenvalues%20and%20Eigenvectors.md#theorem-eigenspaces-and-subspaces): $E\_{k} = \left{ \vec{v} \in \mathbb{R}^{n} \mid A\vec{v} = \lambda \vec{v} \right}$ is a subspace of $\mathbb{R}^{n}$.

# Determinants of 1 x 1, 2 x 2, and 3 x 3 matrices

* [Definition](4.2%20Determinants.md#definition-determinant-of-a-1-x-1-matrix): Determinant of a 1 x 1 Matrix.
* [Definition](4.2%20Determinants.md#definition-determinant-of-a-2-x-2-matrix):  Determinant of a 2 x 2 Matrix.
* [Definition](4.2%20Determinants.md#definition-determinant-of-a-3-x-3-matrix): Determinant of a 3 x 3 Matrix.
  * [Procedure](4.2%20Determinants.md#procedure-alternative-method-for-finding-the-determinant-of-3-x-3-matrices): Alternative Method for Finding the Determinant of a 3 x 3 Matrix.
* [Definition](4.2%20Determinants.md#definition-i-j-minor): (i,j)-minor.
  * [Example](4.2%20Determinants.md#example-finding-the-i-j-minor-of-a-matrix): Finding the (i,j)-minor of a matrix.

# Determinants of n x n Matrices

* [Definition](4.2%20Determinants.md#definition-i-j-cofactor): (i,j)-cofactor.
* [Definition](4.2%20Determinants.md#definition-determinant-of-an-n-x-n-matrix): Determinant of an n x n Matrix.
  * [Remark](4.2%20Determinants.md#remark-determinant-of-an-n-x-n-matrix): The Definition of the Determinant of a n x n Matrix is defined is terms of the determinants of smaller *n-1 x n-1* matrices. This process works recursively until finally computing the determinants of 2 x 2 matrices.
  * [Remark](4.2%20Determinants.md#remark-determinant-of-an-n-x-n-matrix): As later described in the Laplace Expansion Theorem, the Definition of the Determinant of a n x n Matrix is referred to as the *cofactor expansion along the first row*.
  * [Remark](4.2%20Determinants.md#remark-incorporating-the-i-j-minor-into-the-determinant-of-a-3-x-3-matrix): When incorporating the Definition of the (i, j)-cofactor, the summation notation of the determinant of an n x n matrix is rewritten as $detA=\sum\_{j=1}^na\_{1j}C\_{1j}$.
  * [Remark](4.2%20Determinants.md#remark-the-determinant-of-an-identity-matrix): $detI\_{n}=1$.
* [Theorem](4.2%20Determinants.md#theorem-the-laplace-expansion-theorem): The Laplace Expansion Theorem.
  * [Example](4.2%20Determinants.md#example-using-the-laplace-expansion-theorem-on-a-5-x-5-matrix): Using the Laplace Expansion Theorem on a 5 x 5 Matrix.
  * [Example](4.2%20Determinants.md#example-using-the-laplace-expansion-theorem-on-a-4-x-4-matrix): Using the Laplace Expansion Theorem on a 4 x 4 Matrix.
* [Procedure](4.2%20Determinants.md#procedure-determining-the-plus-or-minus-signs-for-each-cofactor-expansion): Determining the Plus or Minus Signs for Each Cofactor Expansion.
* [Theorem](4.2%20Determinants.md#theorem-determinant-of-a-triangular-matrix): The determinant of a (upper or lower) triangular matrix is the **product of the entries on its main diagonal**. If $A=\begin{bmatrix}a\_{ij}\end{bmatrix}$ is an *n x x* matrix then: $detA=a\_{11}a\_{22} \dots a\_{nn}$.

# Properties of the Determinant

* [Theorem](4.2%20Determinants.md#theorem-properties-of-the-determinant): Properties of the Determinant.
  1. If $A$ has a zero row or column, then $detA=0$.
  1. If $B$ is obtained by interchanging two rows or columns of $A$, then $detB=-detA$.
  1. If $A$ has two identical rows or columns, then $detA=0$.
  1. If $B$ is obtained by multiplying a row or column of $A$ by $k$, then $detB=kdetA$.
  1. If $A$, $B$, and $C$ are identical except that the *i-th* row or column of $C$ is the sum of the *i-th* rows and columns of $A$ and $B$, the $detC=detA+detB$.
  1. If $B$ is obtained by adding a multiple of one row or column of $A$ to another row or column, the $detB=detA$.
  * [Example](4.2%20Determinants.md#example-using-properties-of-the-determinants-to-find-determinants-of-matrices): Using Properties of the Determinants to find Determinants of Matrices.

# Determinants of Elementary Matrices

* [Theorem](4.2%20Determinants.md#theorem-properties-of-the-determinant-of-an-elementary-matrix): Properties of the Determinant of Elementary Matrices.
  1. If $E$ results from interchanging two rows of $I\_{n}$, the $detE=-1$.
  1. If $E$ results from multiplying one row of $I\_{n}$ by $k$, then $detE=k$.
  1. If $E$ results from adding a multiple of one row of $I\_{n}$ to another row, then $detE=1$.
* [Theorem](4.2%20Determinants.md#theorem-determinants-and-elementary-matrices): Let $A$ be an *n x n* matrix and $E$ be an *n x n* elementary matrix. Then, $det(EA)=(detE)(detA)$.
* [Theorem](4.2%20Determinants.md#theorem-determinants-and-invertibility): A square matrix $A$ is invertible if and only if $detA\neq 0$.

# Determinants and Matrix Operations

* [Theorem](4.2%20Determinants.md#proof-scalar-multiplication-and-determinants): If $A$ is an *n x n* matrix, then $det(kA)=k^{n}detA$.
* [Remark](4.2%20Determinants.md#remark-matrix-addition-and-determinants): In general, $det(A+B)\neq detA+detB$.
* [Theorem](4.2%20Determinants.md#theorem-matrix-multiplication-and-determinants): If $A$ and $B$ are *n x n* matrices, then $det(AB)=(detA)(detB)$.
* [Theorem](4.2%20Determinants.md#theorem-invertible-matrices-and-determinants): If $A$ is invertible, then $det(A^{-1})=\frac{1}{det(A)}$.
* [Theorem](4.2%20Determinants.md#theorem-the-transpose-and-determinants): $det(A)=det(A^{T})$.

# Cramer's Rule

* [Theorem](4.2%20Determinants.md#theorem-cramer-s-rule): Cramer's Rule.
  Let $A$ be an invertible *n x n* matrix and let $\vec{b}$ be a vector in $\mathbb{R}^{n}$. Then the unique solution $\vec{x}$ of the linear system $A\vec{x}=\vec{b}$ is given by $x\_{i}= \frac{det\[A\_{i}(\vec{b})\]}{detA}$ for $i = 1,2,\dots,n$.
  * [Remark](4.2%20Determinants.md#remark-a-i-vec-b-is-the-matrix-obtained-by-replacing-the-i-th-column-of-a-by-vec-b): $A\_{i}(\vec{b})$ is the matrix obtained by replacing the $i^{th}$ column of $A$ by $\vec{b}$.
  * [Example](4.2%20Determinants.md#example-using-cramer-s-rule-to-find-vec-x-in-a-vec-x-vec-b): Using Cramer's Rule to find $\vec{x}$ for $A\vec{x}=\vec{b}$.

# Eigenvalues and Eigenvectors of n x n Matrices

* [Remark](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#remark-eigenvalues-of-a-square-matrix): The eigenvalues of a square matrix $A$ are the solutions $\lambda$ of the equation $det(A-\lambda I)=0$.
* [Definition](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#definition-characteristic-polynomial-and-characteristic-equation): Characteristic Polynomials and Characteristic Equations.
  * [Example](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#example-finding-the-characteristic-polynomial): Finding the characteristic polynomial of a matrix.
* [Procedure](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#procedure-find-the-eigenvalues-and-eigenspaces): Finding the eigenvalues and eigenspaces of a matrix.
* [Definition](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#definition-algebraic-multiplicity-and-geometric-multiplicity): Algebraic Multiplicity and Geometric Multiplicity.
  * [Remark](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#remark-values-of-algebraic-multiplicity-and-geometric-multiplicity): The geometric multiplicity of $\lambda$ is always less than or equal to its algebraic multiplicity.
* [Theorem](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#theorem-eigenvalues-of-a-triangular-matrix): The eigenvalues of a triangular matrix are the entries on its main diagonal.
* [Theorem](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#theorem-eigenvalues-and-invertibility): A square matrix $A$ is invertible if and only if $0$ **is not** an eigenvalue of $A$.
* [Theorem](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#theorem-the-fundamental-theorem-of-invertible-matrices-version-3): The Fundamental Theorem of Invertible Matrices: Version 3.
  Let $A$ be an *n x n* matrix. The following statements are equivalent :
  1. $A$ is invertible.
  1. $A\vec{x}=\vec{b}$ has a unique solution for every $\vec{b}$ in $\mathbb{R}^{n}$.
  1. $A\vec{x}=\vec{0}$ has only the trivial solution. In other words, the only solution is $\vec{x}=\vec{0}$.
  1. The reduced row echelon form of $A$ is $I\_{n}$.
  1. $A$ is a product of elementary matrices.
  1. $rank(A)=n$.
  1. $nullity(A)=0$.
  1. The columns of $A$ are linearly independent.
  1. The column vectors of $A$ span $\mathbb{R}^{n}$.
  1. The column vectors of A form a basis for $\mathbb{R}^{n}$.
  1. The row vectors of $A$ are linearly independent.
  1. The row vectors of $A$ span $\mathbb{R}^{n}$.
  1. The row vectors of $A$ form a basis for $\mathbb{R}^{n}$.
  1. $detA\neq 0$
  1. $0$ is not an eigenvalue of $A$.
* [Theorem](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#theorem-properties-of-eigenvalues-and-eigenvectors): Let $A$ be a square matrix with an eigenvalue $\lambda$ and associated eigenvector $\vec{v}$.
  1. For all $n\geq 1$, $\lambda^{n}$ is an eigenvalue of $A^{n}$ with associated eigenvector $\vec{v}$.
  1. If $A$ is invertible, then $\frac{1}{\lambda}$ is an eigenvalues of $A^{-1}$ with associated eigenvector $\vec{v}$.
  1. If $A$ is invertible, then for any integer $n$, $\lambda^{n}$ is an eigenvalue of $A^{n}$ with associated eigenvector $\vec{x}$.
  1. If $\vec{v}$ is a column eigenvector of $A$ and $B$ with respective eigenvalues $\lambda$ and $\mu$, then $\vec{v}$ is an eigenvector of $AB$ and $BA$, both which have eigenvalue $\lambda\mu$.
* [Theorem](4.3%20Eigenvalues%20and%20Eigenvectors%20of%20n%20x%20n%20Matrices.md#theorem-eigenvector-independence-theorem): Let $A$ be an *n x n* matrix with distinct eigenvalues $\lambda\_{1},\lambda\_{2},\dots,\lambda\_{m}$ and corresponding eigenvectors $\vec{v}*{1},\vec{v}*{2},\dots,\vec{v}*{m}$. Then $\vec{v}*{1},\vec{v}*{2},\dots,\vec{v}*{m}$ are linearly independent.

# Similar Matrices

* [Definition](4.4%20Similarity%20and%20Diagonalization.md#definition-similarity): Similarity.
* [Theorem](4.4%20Similarity%20and%20Diagonalization.md#theorem-properties-of-similarity): Let $A$, $B$, and $C$ be *n x n* matrices.
  1. $A\sim A$.
  1. If $A\sim B$, then $B \sim A$.
  1. If $A\sim B$ and $B \sim C$, then $A\sim C$.
* [Theorem](4.4%20Similarity%20and%20Diagonalization.md#theorem-properties-of-similarity-continued): Let $A$ and $B$ be *n x n* matrices where $A\sim B$.
  1. $detA=detB$.
  1. $A$ is invertible $\Leftrightarrow$ $B$ is invertible.
  1. $rankA=rankB$.
  1. $A$ and $B$ have the same characteristic polynomial.
  1. $A$ and $B$ have the same eigenvalues.
  1. $A^{m}\sim B^{m}$ for all integers $m \geq 0$.
  1. If $A$ is invertible, then $A^{m}\sim B^{m}$ for all integers $m$.
  * [Remark](4.4%20Similarity%20and%20Diagonalization.md#remark-eigenvectors-of-similar-matrices): Although similar matrices may have the same eigenvalues, the do not necessarily share the same eigenvectors. 

# Diagonalization

* [Definition](4.4%20Similarity%20and%20Diagonalization.md#definition-diagonalizable): Diagonalizable.
* [Theorem](4.4%20Similarity%20and%20Diagonalization.md#theorem-diagonalizability-criterion-theorem): An *n x n* matrix $A$ is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors. In other words, there exists a diagonal matrix $D$ and invertible $P$ such that $A=PDP^{-1}$ if and only if the columns of $P$ are $n$ linearly independent eigenvectors of $A$ and the diagonal entries of $D$ are the eigenvalues of $A$ corresponding to the eigenvectors in $P$ in the same order.
  * [Example](4.4%20Similarity%20and%20Diagonalization.md#example-determining-whether-a-matrix-is-diagonalizable): Determining whether a matrix is diagonalizable.
* [Theorem](4.4%20Similarity%20and%20Diagonalization.md#theorem-eigenspace-union-independence-theorem): Let $A$ be an *n x n* matrix with distinct eigenvalues $\lambda\_{1},\lambda\_{2},\dots,\lambda\_{k}$. If $B\_{i}$ is a basis for the eigenspace $E\_{k\_{i}}$, where $i=1,2,\dots,k$, then $B=B\_{1}\cup B\_{2}\cup\dots B\_{k}$ is linearly independent.
* [Theorem](4.4%20Similarity%20and%20Diagonalization.md#theorem-geometric-algebraic-multiplicity-theorem): If $A$ is an *n x n* matrix, then the geometric multiplicity of each eigenvalue is less than or equal to its algebraic multiplicity.
* [Theorem](4.4%20Similarity%20and%20Diagonalization.md#theorem-distinct-eigenvalue-diagonalizability-theorem): If $A$ is an *n x n* matrix with $n$ distinct eigenvalues, the $A$ is diagonalizable.
* [Theorem](4.4%20Similarity%20and%20Diagonalization.md#theorem-the-diagonalization-theorem): The Diagonalization Theorem.
  Let $A$ be an *n x n* matrix with distinct eigenvalues $\lambda\_{1},\lambda\_{2},\dots,\lambda\_{k}$. The following statements are equivalent:
  1. $A$ is diagonalizable.
  1. The union of the bases of the eigenspaces of $A$ ($B=B\_{1}\cup B\_{2}\cup\dots B\_{k}$) contains $n$ vectors.
  1. The algebraic multiplicity of each eigenvalue equals its geometric multiplicity.
