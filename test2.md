## \#Definition Definition of a Matrix

A **matrix** is a rectangular array of numbers - called ***elements*** or ***entries*** - consisting of $m$ rows and $n$ columns:
$$A = \begin{bmatrix} a\_{11}& \dots & a\_{1n}\\ \vdots & a\_{ij}& \vdots \\ a\_{m1}& \dots & a\_{mn}\end{bmatrix}$$

# Special Matrices

### \#Definition Zero Matrix

An *m x n* matrix whose entries are all zero: $$0\_{m,n}= \begin{bmatrix} 0 & \dots & 0 \\ \vdots & \ddots& \vdots \\ 0 & \dots & 0 \end{bmatrix}$$

### \#Definition Square Matrix

An *n x n* matrix where the *number of rows* **equals** the *number of columns*:$$B = \begin{bmatrix} b\_{11}& \dots & b\_{1n}\\ \vdots & b\_{ij}& \vdots \\ b\_{n1}& \dots & b\_{nn}\end{bmatrix}$$

### \#Definition Diagonal Matrix

A [square matrix](3.1%20Matrix%20Operations.md#definition-of-square-matrix) whose nonzero entries lie on the diagonal:$$C = \begin{bmatrix} c\_{11}& \dots & 0\\ \vdots & c\_{ij}& \vdots \\ 0 & \dots & c\_{nn}\end{bmatrix}$$
where $c\_{11}, c\_{ij}, c\_{nn} \neq 0$

### \#Definition Scalar Matrix

A [diagonal matrix](3.1%20Matrix%20Operations.md#definition-of-diagonal-matrix) whose diagonal entries are all the same:$$D = \begin{bmatrix} d & \dots & 0\\ \vdots & d & \vdots \\ 0 & \dots & d \end{bmatrix}$$

### \#Definition Identity Matrix

A [scalar matrix](3.1%20Matrix%20Operations.md#definition-of-scalar-matrix) whose entries are all 1:$$F = \begin{bmatrix} 1 & \dots & 0\\ \vdots &  1 & \vdots \\ 0 & \dots & 1 \end{bmatrix}$$

# Matrix Addition and Scalar Multiplication

## \#Definition Matrix Addition

If $A=\begin{bmatrix}a\_{ij}\end{bmatrix}$ and $B=\begin{bmatrix}b\_{ij}\end{bmatrix}$ are both *m x n* matrices of equal size, then the sum of the matrices is as follows:$$A+B=\begin{bmatrix}a\_{ij} + b\_{ij}\end{bmatrix}$$

### \#Example Multiplying Two Matrices

If $A=\begin{bmatrix} -3 & 5 & \frac{7}{2} \\ 1 & 0 & 1\end{bmatrix}$ and $B=\begin{bmatrix}0 & 1 & 2 \\ 1 &-1 &5\end{bmatrix}$ then:
$$A+B=\begin{bmatrix}-3+1 & 5+1 & \frac{7}{2}+2 \\ 1+1 & 0+(-1)&1+5\end{bmatrix}=\begin{bmatrix}-3&6& \frac{11}{2}\\2&-1&6\end{bmatrix}$$

## \#Definition Scalar Multiplication

If $A=\begin{bmatrix}a\_{ij}\end{bmatrix}$ is a matrix and $c$ is a scalar, then the product $cA$ is as follows:$$cA=c\begin{bmatrix}a\_{ij}\end{bmatrix}=\begin{bmatrix}ca\_{ij}\end{bmatrix}$$

### \#Example Scalar Matrix

If $A=\begin{bmatrix} -3 & 5 & \frac{7}{2} \\ 1 & 0 & 1\end{bmatrix}$ and $c=\frac{1}{2}$ then:$$cA=\frac{1}{2}\begin{bmatrix} -3 & 5 & \frac{7}{2} \\ 1 & 0 & 1\end{bmatrix}=\begin{bmatrix} \frac{-3}{2} & \frac{5}{2} & \frac{7}{4} \\ \frac{1}{2} & 0 & \frac{1}{2}\end{bmatrix}$$

## \#Remark Matrix Addition and Scalar Multiplication

* $-A$ is shorthand for $(-1)A$
* The difference of two matrices is the sum of two where one of the matrices is scaled by $-1$.$$A-B=A+(-B)$$
* The sum of an *n x m* matrix $A$ and the [zero matrix](3.1%20Matrix%20Operations.md#special-matrices-special-matrices-special-matrices-special-matrices-definition-zero-matrix) results in the matrix $A$.$$A+0=A=0+A$$
* The difference between a matrix $A$ and itself results in the [zero matrix](3.1%20Matrix%20Operations.md#special-matrices-special-matrices-special-matrices-special-matrices-definition-zero-matrix).$$A-A=0=-A+A$$

# Matrix Multiplication

## \#Definition Matrix Multiplication

If $A=\begin{bmatrix}a\_{ij}\end{bmatrix}$ is an *m x n* matrix and If $B=\begin{bmatrix}b\_{ij}\end{bmatrix}$ is an *n x p* matrix, then the product matrix $C=AB$ is defined such that:
$$c\_{ij}=\sum\_{k=1}^{n}a\_{ik}b\_{kj}=a\_{i1}b\_{ij}+a\_{i2}b\_{2j}+ \dots + a\_{in}b\_{nj}$$
In essence, the $ij$-th element of $C$ is the *dot product* of the of the $i$*-th* row of $A$ and $j$*-th*column of $B$.

### \#Example

Let If $A=\begin{bmatrix}1 & 3 & -1 \\ -2 & -1 & 1\end{bmatrix}$, $B=\begin{bmatrix}-4 & 0 & 3 & -1 \\ 5 &-2 & -1 & 1 \\ -1 & 2 & 0 & 6\end{bmatrix}$, and $C=AB$, then:$$c\_{11}=\begin{bmatrix}1 & 3 & -1\end{bmatrix}\begin{bmatrix}-4 \\ 5 \\ -1\end{bmatrix}=(1)(-4)+(3)(5)+(-1)(-1)= 12$$$$c\_{23}=\begin{bmatrix}-2 & -1 & 1\end{bmatrix}\begin{bmatrix}3 \\ -1 \\ -0\end{bmatrix}=(-2)(3)+(-1)(-1)+(1)(0)= -5$$

## \#Remark Matrix Multiplication

* Matrix multiplication only applies if the number of columns of $A$ equals the number of rows of $B$. Otherwise, $AB$ is undefined.
* If $AB$ is defined, that doesn't necessarily mean $BA$ is also defined. Likewise, $AB$ isn't necessarily equal to $BA$.
* Although matrix multiplication isn't commutative, it is commutative with [identity matrices](3.1%20Matrix%20Operations.md#special-matrices-special-matrices-special-matrices-special-matrices-definition-identity-matrix). Let $A$ be an *m x n* matrix and $I\_{m}$ and $I\_{n}$ be the respective identity matrices, then:$$I\_{m}A=A$$$$AI\_{n}=A$$

# The Transpose of a Matrix

## \#Definition Transpose of a Matrix

If $A$ is an *m x n* matrix, then the transpose of A, $A^{T}$, is an *n x m* matrix obtained by interchanging the rows and columns of $A$. In other words the $i$*-th* row of $A$ is the  $i$*-th* column of $A^{T}$ for all $i$.

### \#Example Finding the Transpose

Let $A=\begin{bmatrix}a&b&c\\d&e&f\end{bmatrix}$. Then, $A^{T}=\begin{bmatrix}a&d\\b&e\\c&f\end{bmatrix}$.

## \#Definition Symmetric Matrix

A square matrix $A$ is symmetric if $A$ is equal to its own transpose,$$A=A^{T}$$
Likewise, a square matrix $A$ is symmetric if and only if $A\_{ij}=A\_{ji}$ for all $i$ and $j$.

