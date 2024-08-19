One of the best (and most widely used) methods for numerically approximating the eigenvalues of a matrix makes use of the $QR$ factorization. The purpose of this exploration is to introduce this method, the $QR$ algorithm, and to show it at work in a few examples. For a more complete treatment of this topic, consult any good text on numerical linear algebra. (You will find it helpful to use a CAS to perform the calculations in the problems below.)

Given a square matrix $A$, the first step is to factor it as $A = QR$ (using whichever method is appropriate). Then we define $A_1 = RQ$.

# Question 1) First prove that $A_1$ is similar to $A$. Then prove that $A_1$ has the same eigenvalues as $A$.

### 1) Prove $A \sim A\_{1}$

According to the **QR Factorization Theorem**, if $A=QR$, then $Q$ is an orthogonal matrix and $R$ is an invertible upper triangular matrix.
Following the **Definition of Similarity**, $A \sim A_1$ if there's an invertible matrix $P$ such that:
$$A=PA\_{1}P^{-1}$$
and
$$A\_{1}=P^{-1}AP$$
Using the equation $A=PA\_{1}P^{-1}$, let $P=Q$:
$$A=QA\_{1}Q^{-1}$$
since $Q$ is defined as an orthogonal matrix, so $Q^{-1}$ exists where $Q^{-1}=Q^{T}$. 
Now, given that $A\_{1}=RQ$, the equation becomes:
$$A=Q(RQ)Q^{-1}$$
$$A=QRI$$
$$A=QR$$
Given $A$ is defined as $A=QR$, then there is an invertible matrix $Q$ such that $A=QA\_{1}Q^{-1}$. As such, $A \sim A\_{1}$.

### 2) Prove $A_1$ has the same eigenvalues as $A$

As given in another theorem:
Let $A$ and $B$ be *n x n* matrices where $A\sim B$.

1. $detA=detB$.
1. $A$ is invertible $\Leftrightarrow$ $B$ is invertible.
1. $rankA=rankB$.
1. $A$ and $B$ have the same characteristic polynomial.
1. $A$ and $B$ have the same eigenvalues.
1. $A^{m}\sim B^{m}$ for all integers $m \geq 0$.
1. If $A$ is invertible, then $A^{m}\sim B^{m}$ for all integers $m$.
   Specifically focusing on property (4), since $A \sim A\_{1}$ then, following the **Definition of Similarity** there exists an invertible matrix $P$ such that:
   $$A=PA\_{1}P^{-1}$$
   Then, following the **Definition of Characteristic Polynomials** the characteristic polynomial of $A$ is the following:
   $$det(A-\lambda I)$$
   Substituting $A=PA\_{1}P^{-1}$:
   $$det(PA\_{1}P^{-1}-\lambda I)$$
   $$det(PA\_{1}P^{-1}-P(\lambda I)P^{-1})$$
   $$det(P(A\_{1}-\lambda I)P^{-1})$$
   $$(detP)det(A\_{1}-\lambda I)(detP^{-1})$$
   $$(detP)det(A\_{1}-\lambda I)\frac{1}{detP}$$
   $$det(A\_{1}-\lambda I)$$
   Clearly, this expression is the characteristic polynomial of $A\_{1}$, so when $A\sim A\_{1}$, $A$ and $A\_{1}$ have the same characteristic polynomial.
   Now, property (5) is quite trivial to solve since eigenvalues are found via. setting the characteristic polynomial to 0. Given the eigenvalues of $A\_{1}$ is found from solving $det(A\_{1}-\lambda I)=0$, and $det(A\_{1}-\lambda I)=det(A-\lambda I)$. Then characteristic equation for $A$ and $A\_{1}$ are the same, meaning the have the same solution or eigenvalues.

# Question 2) If $A = \begin{bmatrix} 1 & 0 \\ 1 & 3 \end{bmatrix}$, find $A_1$ and verify that it has the same eigenvalues as $A$.

## 1) Find the eigenvalues of A

In order to find the eigenvalues of $A$ solve the following equation:
$$det(A-\lambda I)=0$$
$$det\begin{bmatrix} 1-\lambda & 0 \\ 1 & 3-\lambda \end{bmatrix} = 0$$
$$(1-\lambda)(3-\lambda)-(0)(1)=0$$
$$\lambda^{2}-4\lambda+3=0$$
$$(\lambda-3)(\lambda-1)=0$$
Therefore, the eigenvalues of $A$ are $\lambda\_{1}=3$ and $\lambda\_{2}=1$.

## 2) Find the matrix $A\_{1}$

Now, in order to find the eigenvalues of $A\_{1}$, first find the matrix $A\_{1}$. Given $A\_{1}=RQ$ and $A=QR$, then follow the **QR Factorization Theorem** in order to find the matrices $Q$ and $R$.

### 2.1) Ensure the columns of A are linearly independent

Before proceeding, ensure the the columns of matrix $A$ are linearly independent:
$$\begin{bmatrix} 1 & 0 \\ 1 & 3 \end{bmatrix}R\_{2}-R\_{1}\rightarrow R\_{2} \begin{bmatrix} 1 & 0 \\ 0 & 3 \end{bmatrix} \frac{1}{3}R\_{3} \rightarrow R\_{3} \begin{bmatrix} ① & 0 \\ 0 & ① \end{bmatrix}$$
Since there's a pivot in every column, the columns of $A$ are therefore linearly independent.
Let $colA=\text{Span}\left{ \vec{x}*{1},\vec{x}*{2} \right}$ where $\vec{x}*{1}= \begin{bmatrix} 1 \\ 1 \end{bmatrix}$, $\vec{x}*{2} = \begin{bmatrix} 0 \\ 3 \end{bmatrix}$. 

### 2.2) Find the matrix $Q$

Now, in order to find $Q$, first apply the **Gram-Schmidt Process** in order to find an orthonormal basis for $ColA$:
$$\vec{v}*{1}=\vec{x}*{1}=\begin{bmatrix} 1 \\ 1 \end{bmatrix}$$
$$\vec{v}*{2}= \vec{x}*{2}-\frac{\vec{x}*{2}\cdot\vec{v}*{1}}{\vec{v}*{1}\cdot\vec{v}*{1}}\cdot\vec{v}*{1} = \begin{bmatrix} 0 \\ 3 \end{bmatrix} - \frac{(0)(1)+(3)(1)}{(1)^{2}+(1)^{2}}\begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\ 3 \end{bmatrix} - \frac{3}{2}\begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 0 - \frac{3}{2} \\ 3 - \frac{3}{2} \end{bmatrix} = \begin{bmatrix} -\frac{3}{2} \\ \frac{3}{2} \end{bmatrix}$$
The vectors $\vec{v}*{1}$ and $\vec{v}*{2}$ form an orthogonal basis for for $colA$, but not orthonormal basis. In in order to find an orthonormal basis for $colA$, normalize the vectors $\vec{v}*{1}$ and $\vec{v}*{2}$:
$$\vec{n}*{1} = \frac{1}{||\vec{v}*{1}||}\vec{v}*{1} = \frac{1}{\sqrt{(1)^{2}+(1)^{2}}}\begin{bmatrix} 1 \\ 1 \end{bmatrix} = \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} \end{bmatrix}$$
$$\vec{n}*{2} = \frac{1}{||\vec{v}*{2}||}\vec{v}\_{2} = \frac{1}{\sqrt{( -\frac{3}{2} )^{2}+( \frac{3}{2} )^{2}}}\begin{bmatrix} -\frac{3}{2} \\  \frac{3}{2} \end{bmatrix} = \frac{1}{\sqrt{ \frac{18}{4} }}\begin{bmatrix} -\frac{3}{2} \\  \frac{3}{2} \end{bmatrix} = \frac{1}{\frac{3\sqrt{2}}{2}}\begin{bmatrix} -\frac{3}{2} \\  \frac{3}{2} \end{bmatrix} = \frac{2}{3\sqrt{2}}\begin{bmatrix} -\frac{3}{2} \\  \frac{3}{2} \end{bmatrix} = \begin{bmatrix} -\frac{1}{\sqrt{2}} \\  \frac{1}{\sqrt{2}} \end{bmatrix}$$
Therefore, and orthonormal basis for $colA$ is:
$$\left{ \begin{bmatrix} \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} -\frac{1}{\sqrt{2}} \\  \frac{1}{\sqrt{2}} \end{bmatrix} \right}$$
Given $Q$ is an orthogonal matrix, then its columns must form an orthonormal set. As such:
$$Q = \begin{bmatrix} \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \end{bmatrix}$$

### 2.3) Find the matrix $R$

In order to find $R$, consider the original equation:
$$A=QR$$
Left multiplying both sides by $Q^{T}$ results in:
$$Q^{T}A=Q^{T}QR$$
Since $Q$ is an orthogonal matrix, then according to then $Q^{T}Q=I\_{n}$:
$$Q^{T}A=IR$$
$$Q^{T}A=R$$
As such:
$$R = Q^{T}A = \begin{bmatrix} \frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ -\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \end{bmatrix}\begin{bmatrix} 1 & 0 \\ 1 & 3 \end{bmatrix} = \begin{bmatrix} \frac{2}{\sqrt{2}} & \frac{3}{\sqrt{2}} \\ 0 & \frac{3}{\sqrt{2}} \end{bmatrix}$$

### 2.4) Find $A\_{1}$ using $A\_{1}=RQ$

$$A\_{1} = RQ = \begin{bmatrix} \frac{2}{\sqrt{2}} & \frac{3}{\sqrt{2}} \\ 0 & \frac{3}{\sqrt{2}} \end{bmatrix}\begin{bmatrix} \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \end{bmatrix} = \begin{bmatrix} \frac{5}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ \frac{3}{\sqrt{2}} & \frac{3}{\sqrt{2}} \end{bmatrix} = \begin{bmatrix} \frac{5}{2} & \frac{1}{2} \\ \frac{3}{2} & \frac{3}{2} \end{bmatrix}$$

### 3) Find the eigenvalues of $A\_{1}$

$$det(A\_{1}-\lambda I) = 0$$
$$det\begin{bmatrix} \frac{5}{2}-\lambda & \frac{1}{2} \\ \frac{3}{2} & \frac{3}{2}-\lambda \end{bmatrix} = 0$$
$$\left( \frac{5}{2} - \lambda\right)\left( \frac{3}{2} - \lambda\right) - \left( \frac{1}{2} \right)\left( \frac{3}{2} \right)= 0$$
$$\frac{15}{4} - \frac{8}{2}\lambda + \lambda^{2} - \frac{3}{4} = 0$$
$$\lambda^{2}-4\lambda+3=0$$
$$(\lambda-3)(\lambda-1)=0$$
Therefore, the eigenvalues of $A\_{1}$ are $\lambda\_{1}=3$ and $\lambda\_{2}=1$.
All put together, $A$ and $A\_{1}$ have the same eigenvalues when $A = QR = \begin{bmatrix} 1 & 0 \\ 1 & 3 \end{bmatrix}$ and $A\_{1}=RQ$.

# Continuing the algorithm, we factor $A_1$ as $A_1 = Q_1R_1$ and set $A_2 = R_1Q_1$. Then we factor $A_2 = Q_2R_2$ and set $A_3 = R_2Q_2$, and so on. That is, for $k \ge 1$, we compute $A_k = Q_kR_k$ and then set $A\_{k+1} = R_kQ_k$.

# Question 3) Prove that $A_k$ is similar to $A$ for all $k \ge 1$.

This proof is [carried out by induction](https://www.mathcentre.ac.uk/resources/uploaded/mathcentre-proof.pdf). According to the **QR Factorization Theorem**, if $A=QR$, then $Q$ is an orthogonal matrix and $R$ is an invertible upper triangular matrix.

### 1) Base Case

As [proven in the first step](Witten%20Assignment%203.md#1-prove-a-sim-a-1), when $A\_{1}=RQ$, then $A \sim A\_{1}$.

### 2) Induction Step

Assuming $A \sim A\_{k}$, prove $A \sim A\_{k+1}$.
Let $A\_{k}=Q\_{k}R\_{k}$. Using the algorithm described above, then $A\_{k+1}=R\_{k}Q\_{k}$. 
Assuming that $A \sim A\_{k}$, then there exists an invertible matrix $P$ such that:
$$A=P\_{k}A\_{k}P\_{k}^{-1}$$
Substituting $A\_{k}=Q\_{k}R\_{k}$ into the equation yields:
$$A=P\_{k}(Q\_{k}R\_{k})P\_{k}^{-1}$$
Now substitute $P\_{k+1}=P\_{k}Q\_{k}$ into the equation:
$$A=P\_{k+1}R\_{k}P\_{k}^{-1}$$
Solving the equation $P\_{k+1}=P\_{k}Q\_{k}$ in terms of $P\_{k}^{-1}$ results in:
$$P\_{k+1}=P\_{k}Q\_{k}$$
$$P\_{k+1}Q\_{k}^{-1}=P\_{k}Q\_{k}Q\_{k}^{-1}$$
$$P\_{k+1}Q\_{k}^{-1}=P\_{k}I$$
$$P\_{k}=P\_{k+1}Q\_{k}^{-1}$$
$$P\_{k}^{-1}=(P\_{k+1}Q\_{k}^{-1})^{-1}$$
$$P\_{k}^{-1}=Q\_{k}P\_{k+1}^{-1}$$
since $Q$ is defined as an orthogonal matrix, meaning $Q^{-1}$ exists where $Q^{-1}=Q^{T}$.
Substituting $P\_{k}^{-1}=Q\_{k}P\_{k+1}^{-1}$ into the equation $A=P\_{k+1}R\_{k}P\_{k}^{-1}$ yields:
$$A=P\_{k+1}R\_{k}(Q\_{k}P\_{k+1}^{-1})$$
Given $A\_{k+1}=R\_{k}Q\_{k}$, the equation can finally be rewritten as:
$$A=P\_{k+1}A\_{k+1}P\_{k+1}^{-1}$$
This equation means that $A \sim A\_{k+1}$. 
Therefore, by induction, $A \sim A\_{k}$ for all $k \geq 1$.

# Question 4) Continuing Problem 2, compute $A_2$, $A_3$, $A_4$, and $A_5$, using two-decimal-place accuracy. What do you notice?

## 1) Computation of $A_2$, $A_3$, $A_4$, and $A_5$

For the sake of redundancy, all QR factorizations are computed on [this website](https://www.emathhelp.net/en/calculators/linear-algebra/qr-factorization-calculator/) while all matrix multiplications are computed on [this website](https://www.symbolab.com/). Following the algorithm:
$$A=QR$$
$$A\_{1}=RQ=Q\_{1}R\_{1}$$
$$A\_{2}=R\_{1}Q\_{1}=Q\_{2}R\_{2}$$
$$A\_{3}=R\_{2}Q\_{2}=Q\_{3}R\_{3}$$
$$A\_{4}=R\_{3}Q\_{3}=Q\_{4}R\_{4}$$
$$A\_{5}=R\_{4}Q\_{4}=Q\_{5}R\_{5}$$

### $A\_{2}$

[Given](Witten%20Assignment%203.md#2-4-find-a-1-using-a-1-rq) $A\_{1}=\begin{bmatrix} \frac{5}{2} & \frac{1}{2} \\ \frac{3}{2} & \frac{3}{2} \end{bmatrix}$ then [its QR factorizations is as follows](https://www.emathhelp.net/en/calculators/linear-algebra/qr-factorization-calculator/?i=%5B%5B5%2F2%2C1%2F2%5D%2C%5B3%2F2%2C3%2F2%5D%5D):
$$Q\_{1} = \begin{bmatrix} \frac{5\sqrt{34}}{34} & -\frac{3\sqrt{34}}{34} \\ \frac{3\sqrt{34}}{34} & \frac{5\sqrt{34}}{34} \end{bmatrix} \approx \begin{bmatrix} 0.857492925712544 & -0.514495755427527 \\ 0.514495755427527 & 0.857492925712544 \end{bmatrix}
$$
$$R\_{1} = \begin{bmatrix} \frac{\sqrt{34}}{2} & \frac{7\sqrt{34}}{34} \\ 0 & \frac{3\sqrt{34}}{17} \end{bmatrix} \approx \begin{bmatrix} 2.91547594742265 & 1.200490095997562 \\ 0 & 1.028991510855053 \end{bmatrix}
$$
Given $A\_{2}=R\_{1}Q\_{1}$, then $A\_{2}$ is [the following matrix](https://www.symbolab.com/solver/step-by-step/%5Cbegin%7Bpmatrix%7D%5Cfrac%7B%5Csqrt%7B34%7D%7D%7B2%7D%26%5Cfrac%7B7%5Csqrt%7B34%7D%7D%7B34%7D%5C%5C%20%20%20%200%26%5Cfrac%7B3%5Csqrt%7B34%7D%7D%7B17%7D%5Cend%7Bpmatrix%7D%5Cbegin%7Bpmatrix%7D%5Cfrac%7B5%5Csqrt%7B34%7D%7D%7B34%7D%26-%5Cfrac%7B3%5Csqrt%7B34%7D%7D%7B34%7D%5C%5C%20%20%20%5Cfrac%7B3%5Csqrt%7B34%7D%7D%7B34%7D%26%5Cfrac%7B5%5Csqrt%7B34%7D%7D%7B34%7D%5Cend%7Bpmatrix%7D?or=input):
$$A\_{2} = R\_{1}Q\_{1} = \begin{bmatrix} \frac{\sqrt{34}}{2} & \frac{7\sqrt{34}}{34} \\ 0 & \frac{3\sqrt{34}}{17} \end{bmatrix}\begin{bmatrix} \frac{5\sqrt{34}}{34} & -\frac{3\sqrt{34}}{34} \\ \frac{3\sqrt{34}}{34} & \frac{5\sqrt{34}}{34} \end{bmatrix} = \begin{bmatrix} \frac{53}{17} & -\frac{8}{17} \\ \frac{9}{17} & \frac{15}{17} \end{bmatrix} \approx \begin{bmatrix} 3.12 & -0.47 \\ 0.53 & 0.88 \end{bmatrix}$$

### $A\_{3}$

Given $A\_{2} = \begin{bmatrix} \frac{53}{17} & -\frac{8}{17} \\ \frac{9}{17} & \frac{15}{17} \end{bmatrix}$ then [its QR factorizations is as follows](https://www.emathhelp.net/en/calculators/linear-algebra/qr-factorization-calculator/?i=%5B%5B53%2F17%2C-8%2F17%5D%2C%5B9%2F17%2C15%2F17%5D%5D):
$$Q\_{2} = \begin{bmatrix} \frac{53\sqrt{10}}{170} & -\frac{9\sqrt{10}}{170} \\ \frac{9\sqrt{10}}{170} & \frac{53\sqrt{10}}{170} \end{bmatrix} \approx \begin{bmatrix} 0.98588656464073 & -0.167414699655973 \\ 0.167414699655973 & 0.98588656464073 \end{bmatrix}
$$
$$R_2 = \begin{bmatrix} \sqrt{10} & -\frac{\sqrt{10}}{10} \\ 0 & \frac{3\sqrt{10}}{10} \end{bmatrix} \approx \begin{bmatrix} 3.162277660168379 & -0.316227766016838 \\ 0 & 0.948683298050514 \end{bmatrix}
$$
Given $A\_{3}=R\_{2}Q\_{2}$, then $A\_{3}$ is [the following matrix](https://www.symbolab.com/solver/step-by-step/%5Cbegin%7Bbmatrix%7D%20%5Csqrt%7B10%7D%20%26%20-%5Cfrac%7B%5Csqrt%7B10%7D%7D%7B10%7D%20%5C%5C%20%200%20%26%20%5Cfrac%7B3%5Csqrt%7B10%7D%7D%7B10%7D%20%5Cend%7Bbmatrix%7D%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7B53%5Csqrt%7B10%7D%7D%7B170%7D%20%26%20-%5Cfrac%7B9%5Csqrt%7B10%7D%7D%7B170%7D%20%5C%5C%20%20%5Cfrac%7B9%5Csqrt%7B10%7D%7D%7B170%7D%20%26%20%5Cfrac%7B53%5Csqrt%7B10%7D%7D%7B170%7D%20%5Cend%7Bbmatrix%7D?or=input):
$$A\_{2} = R\_{2}Q\_{2} = \begin{bmatrix} \sqrt{10} & -\frac{\sqrt{10}}{10} \\ 0 & \frac{3\sqrt{10}}{10} \end{bmatrix}\begin{bmatrix} \frac{53\sqrt{10}}{170} & -\frac{9\sqrt{10}}{170} \\ \frac{9\sqrt{10}}{170} & \frac{53\sqrt{10}}{170} \end{bmatrix} = \begin{bmatrix} \frac{521}{170} & -\frac{143}{170} \\ \frac{27}{170} & \frac{159}{170} \end{bmatrix} \approx \begin{bmatrix} 3.06 & -0.84 \\ 0.16 & 0.94 \end{bmatrix}$$

### $A\_{4}$

Given $A\_{3} = \begin{bmatrix} \frac{521}{170} & -\frac{143}{170} \\ \frac{27}{170} & \frac{159}{170} \end{bmatrix}$ then [its QR factorizations is as follows](https://www.emathhelp.net/en/calculators/linear-algebra/qr-factorization-calculator/?i=%5B%5B521%2F170%2C-143%2F170%5D%2C%5B27%2F170%2C159%2F170%5D%5D):
$$Q_3 = \begin{bmatrix} \frac{521\sqrt{272170}}{272170} & -\frac{27\sqrt{272170}}{272170} \\ \frac{27\sqrt{272170}}{272170} & \frac{521\sqrt{272170}}{272170} \end{bmatrix} \approx \begin{bmatrix} 0.998659865513183 & -0.051753966159033 \\ 0.051753966159033 & 0.998659865513183 \end{bmatrix}
$$
$$R_3 = \begin{bmatrix} \frac{\sqrt{272170}}{170} & -\frac{413\sqrt{272170}}{272170} \\ 0 & \frac{3\sqrt{272170}}{1601} \end{bmatrix} \approx \begin{bmatrix} 3.068818511874485 & -0.791644000877053 \\ 0 & 0.977574916337281 \end{bmatrix}
$$
Given $A\_{4}=R\_{3}Q\_{3}$, then $A\_{3}$ is [the following matrix](https://www.symbolab.com/solver/step-by-step/%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7B%5Csqrt%7B272170%7D%7D%7B170%7D%20%26%20-%5Cfrac%7B413%5Csqrt%7B272170%7D%7D%7B272170%7D%20%5C%5C%20%200%20%26%20%5Cfrac%7B3%5Csqrt%7B272170%7D%7D%7B1601%7D%20%5Cend%7Bbmatrix%7D%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7B521%5Csqrt%7B272170%7D%7D%7B272170%7D%20%26%20-%5Cfrac%7B27%5Csqrt%7B272170%7D%7D%7B272170%7D%20%5C%5C%20%20%5Cfrac%7B27%5Csqrt%7B272170%7D%7D%7B272170%7D%20%26%20%5Cfrac%7B521%5Csqrt%7B272170%7D%7D%7B272170%7D%20%5Cend%7Bbmatrix%7D?or=input):
$$A\_{4} = R\_{3}Q\_{3} = \begin{bmatrix} \frac{\sqrt{272170}}{170} & -\frac{413\sqrt{272170}}{272170} \\ 0 & \frac{3\sqrt{272170}}{1601} \end{bmatrix}\begin{bmatrix} \frac{521\sqrt{272170}}{272170} & -\frac{27\sqrt{272170}}{272170} \\ \frac{27\sqrt{272170}}{272170} & \frac{521\sqrt{272170}}{272170} \end{bmatrix} = \begin{bmatrix} \frac{4841}{1601} & -\frac{1520}{1601} \\ \frac{81}{1601} & \frac{1563}{1601} \end{bmatrix} \approx \begin{bmatrix} 3.02 & -0.95 \\ 0.05 & 0.98 \end{bmatrix}$$

### $A\_{5}$

Given $A\_{4} = \begin{bmatrix} \frac{4841}{1601} & \frac{-1520}{1601} \\ \frac{81}{1601} & \frac{1563}{1601} \end{bmatrix}$ then [its QR factorization is as follows](https://www.emathhelp.net/en/calculators/linear-algebra/qr-factorization-calculator/?i=%5B%5B4841%2F1601%2C-1520%2F1601%5D%2C%5B81%2F1601%2C1563%2F1601%5D%5D): 
$$Q_4 = \begin{bmatrix} \frac{4841\sqrt{23441842}}{23441842} & -\frac{81\sqrt{23441842}}{23441842} \\ \frac{81\sqrt{23441842}}{23441842} & \frac{4841\sqrt{23441842}}{23441842} \end{bmatrix} \approx \begin{bmatrix} 0.999860048132219 & -0.016729738462861 \\ 0.016729738462861 & 0.999860048132219 \end{bmatrix}
$$
$$R_4 = \begin{bmatrix} \frac{\sqrt{23441842}}{1601} & -\frac{4517\sqrt{23441842}}{23441842} \\ 0 & \frac{3\sqrt{23441842}}{14642} \end{bmatrix} \approx \begin{bmatrix} 3.024158402138392 & -0.932941094280776 \\ 0 & 0.992011528853346 \end{bmatrix}
$$
Given $A\_{5}=R\_{4}Q\_{4}$ then [its QR factorization is as follows](https://www.symbolab.com/solver/step-by-step/%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7B%5Csqrt%7B23441842%7D%7D%7B1601%7D%20%26%20-%5Cfrac%7B4517%5Csqrt%7B23441842%7D%7D%7B23441842%7D%20%5C%5C%20%200%20%26%20%5Cfrac%7B3%5Csqrt%7B23441842%7D%7D%7B14642%7D%20%5Cend%7Bbmatrix%7D%20%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7B4841%5Csqrt%7B23441842%7D%7D%7B23441842%7D%20%26%20-%5Cfrac%7B81%5Csqrt%7B23441842%7D%7D%7B23441842%7D%20%5C%5C%20%20%5Cfrac%7B81%5Csqrt%7B23441842%7D%7D%7B23441842%7D%20%26%20%5Cfrac%7B4841%5Csqrt%7B23441842%7D%7D%7B23441842%7D%20%5Cend%7Bbmatrix%7D?or=input):
$$A\_{5}=R\_{4}Q\_{4} = \begin{bmatrix} \frac{\sqrt{23441842}}{1601} & -\frac{4517\sqrt{23441842}}{23441842} \\ 0 & \frac{3\sqrt{23441842}}{14642} \end{bmatrix} \begin{bmatrix} \frac{4841\sqrt{23441842}}{23441842} & -\frac{81\sqrt{23441842}}{23441842} \\ \frac{81\sqrt{23441842}}{23441842} & \frac{4841\sqrt{23441842}}{23441842} \end{bmatrix} = \begin{bmatrix}\frac{44045}{14642}&-\frac{14399}{14642}\\ \frac{243}{14642}&\frac{14523}{14642}\end{bmatrix} \approx \begin{bmatrix} 3.01 & -0.98 \\ 0.02 & 0.99 \end{bmatrix}$$

## 2) Observations

As this algorithm continues infinitely, it approaches the upper triangular matrix $\begin{bmatrix} 3 & -1 \\ 0 & 1 \end{bmatrix}$.

# It can be shown that if the eigenvalues of $A$ are all real and have distinct absolute values, then the matrices $A_k$ approach an upper triangular matrix $U$.

# Question 5) What will be true of the diagonal entries of this matrix $U$?

Recall the [eigenvalues of A](Witten%20Assignment%203.md#1-find-the-eigenvalues-of-a). Clearly the diagonal entries of $U$ are approximately the eigenvalues of $A$. 

# Question 6) Approximate the eigenvalues of the following matrices by applying the $QR$ algorithm. Use two-decimal-place accuracy and perform at least five iterations.

Once again, for the sake of redundancy, all QR factorizations are computed on [this website](https://www.emathhelp.net/en/calculators/linear-algebra/qr-factorization-calculator/) while all matrix multiplications are computed on [this website](https://www.symbolab.com/).

## a. $A = \begin{bmatrix} 2 & 3 \\ 2 & 1 \end{bmatrix}$

$A = QR$
$A_1 = RQ \approx \begin{bmatrix} -0.60 & -3.35 \\ 1.60 & 2.60 \end{bmatrix}$
$A_1 = Q\_{1}R\_{1}$
$A_2 = R\_{1}Q\_{1} \approx \begin{bmatrix} 2.67 & 3.39 \\ -0.39 & -0.67 \end{bmatrix}$
$A_2 = Q\_{2}R\_{2}$
$A_3 = R\_{2}Q\_{2} \approx \begin{bmatrix} 2.90 & 1.35 \\ -0.04 & 0.10 \end{bmatrix}$
$A_3 = Q\_{3}R\_{3}$
$A_4 = R\_{3}Q\_{3} \approx \begin{bmatrix} 2.93 & 0.12 \\ -0.02 & 0.07 \end{bmatrix}$
$A_4 = Q\_{4}R\_{4}$
$A_5 = R\_{4}Q\_{4} \approx \begin{bmatrix} 2.95 & 0.06 \\ -0.01 & 0.02 \end{bmatrix}$
The eigenvalues of $A$ are $\lambda\_{1} \approx 2.67$ and $\lambda\_{2} \approx 0.02$.

## b. $B = \begin{bmatrix} 1 & 1 \\ 2 & 1 \end{bmatrix}$

$B = QR$
$B_1 = RQ \approx \begin{bmatrix} -0.44 & -1.73 \\ 1.73 & 0.44 \end{bmatrix}$
$B_1 = Q\_{1}R\_{1}$
$B_2 = R\_{1}Q\_{1} \approx \begin{bmatrix} 2.16 & 1.38 \\ -0.38 & -0.16 \end{bmatrix}$
$B_2 = Q\_{2}R\_{2}$
$B_3 = R\_{2}Q\_{2} \approx \begin{bmatrix} 2.60 & 0.54 \\ -0.06 & -0.10 \end{bmatrix}$
$B_3 = Q\_{3}R\_{3}$
$B_4 = R\_{3}Q\_{3} \approx \begin{bmatrix} 2.66 & 0.19 \\ -0.03 & 0.00 \end{bmatrix}$
$B_4 = Q\_{4}R\_{4}$
$B_5 = R\_{4}Q\_{4} \approx \begin{bmatrix} 2.68 & 0.06 \\ -0.01 & 0.00 \end{bmatrix}$
The eigenvalues of $B$ are $\lambda\_{1} \approx 2.68$ and $\lambda\_{2} \approx 0.00$

## c. $C = \begin{bmatrix} 1 & 0 & -1 \\ 1 & 2 & 1 \\ -4 & 0 & 1 \end{bmatrix}$

$C = QR$
$C_1 = RQ \approx \begin{bmatrix} 3.16 & -0.22 & 0.19 \\ -0.37 & 2.68 & 1.15 \\ -1.58 & 1.15 & 1.16 \end{bmatrix}$
$C_1 = Q\_{1}R\_{1}$
$C_2 = R\_{1}Q\_{1} \approx \begin{bmatrix} 3.50 & -0.12 & -0.32 \\ -0.12 & 2.16 & 0.84 \\ -0.32 & 0.84 & 0.33 \end{bmatrix}$
$C_2 = Q\_{2}R\_{2}$
$C\_{3} = R\_{2}Q\_{2} \approx \begin{bmatrix} 3.58 & -0.07 & -0.13 \\ -0.07 & 2.05 & 0.49 \\ -0.13 & 0.49 & 0.33 \end{bmatrix}$
$C\_{3} = Q\_{3}R\_{3}$
$C_4 = R\_{3}Q\_{3} \approx \begin{bmatrix} 3.60 & -0.04 & -0.05 \\ -0.04 & 2.01 & 0.20 \\ -0.05 & 0.20 & 0.31 \end{bmatrix}$
$C_4 = Q\_{4}R\_{4}$
$C_5 = R\_{4}Q\_{4} \approx \begin{bmatrix} 3.61 & -0.02 & -0.02 \\ -0.02 & 2.00 & 0.08 \\ -0.02 & 0.08 & 0.31 \end{bmatrix}$
The eigenvalues of $C$ are $\lambda\_{1} \approx 3.61$, $\lambda\_{2} \approx 2.00$, and $\lambda\_{3} \approx 0.31$.

## d. $D = \begin{bmatrix} 1 & 1 & -1 \\ 0 & 2 & 0 \\ -2 & 4 & 2 \end{bmatrix}$

$D = QR$
$D_1 = RQ \approx \begin{bmatrix} -1.34 & 0.89 & -1.34 \\ 2.68 & -0.22 & 0.67 \\ 1.34 & 1.78 & 1.34 \end{bmatrix}$
$D_1 = Q\_{1}R\_{1}$
$D_2 = R\_{1}Q\_{1} \approx \begin{bmatrix} 4.05 & -0.49 & 1.83 \\ -0.25 & 2.33 & -0.29 \\ 1.83 & -0.29 & 1.16 \end{bmatrix}$
$D_2 = Q\_{2}R\_{2}$
$D_3 = R\_{2}Q\_{2} \approx \begin{bmatrix} 4.39 & -0.26 & -0.14 \\ -0.26 & 2.08 & -0.27 \\ -0.14 & -0.27 & 0.64 \end{bmatrix}$
$D_3 = Q\_{3}R\_{3}$
$D_4 = R\_{3}Q\_{3} \approx \begin{bmatrix} 4.49 & -0.13 & -0.05 \\ -0.13 & 2.02 & -0.16 \\ -0.05 & -0.16 & 0.49 \end{bmatrix}$
$D_4 = Q\_{4}R\_{4}$
$D_5 = R\_{4}Q\_{4} \approx \begin{bmatrix} 4.53 & -0.07 & -0.02 \\ -0.07 & 2.00 & -0.06 \\ -0.02 & -0.06 & 0.46 \end{bmatrix}$
The eigenvalues of $D$ are $\lambda\_{1} \approx 4.53$, $\lambda\_{2} \approx 2.00$, and $\lambda\_{3} \approx 0.46$.

# Question 7) Apply the $QR$ algorithm to the matrix $A = \begin{bmatrix} 2 & 3 \\ -1 & -2 \end{bmatrix}$. What happens? Why?

## 1) Computation

For the last time, all QR factorizations are computed on [this website](https://www.emathhelp.net/en/calculators/linear-algebra/qr-factorization-calculator/) while all matrix multiplications are computed on [this website](https://www.symbolab.com/).
$$A=QR$$
$$A_1 = RQ \approx \begin{bmatrix} \frac{2}{5} & -\frac{21}{5} \\ - \frac{1}{5} & -\frac{2}{5} \end{bmatrix} \approx \begin{bmatrix} 0.40 & -4.20 \\ -0.20 & -0.40 & \end{bmatrix}$$
$$A_1 = Q\_{1}R\_{1}$$
$$A_2 = R\_{1}Q\_{1} = \begin{bmatrix} 2 & 3  \\ -1 & -2 \end{bmatrix} \approx \begin{bmatrix} 2.00 & 3.00 \\ -1.00 & -2.00 \end{bmatrix}$$

## 2) Observations

Clearly there's a back-and-forth in the algorithm, with each iterating producing the matrix $\begin{bmatrix} \frac{2}{5} & -\frac{21}{5} \\ - \frac{1}{5} & -\frac{2}{5} \end{bmatrix}$ and then back to the 
The matrix $A$ remains unchanged despite the number of iterations. This phenomena is a result of the eigenvalues of $A$:
$$det(A-\lambda I)=0$$
$$det\begin{bmatrix} 2-\lambda & 3 \\ -1 & -2-\lambda \end{bmatrix} = 0$$
$$(2-\lambda)(-2-\lambda)-(3)(-1)=0$$
$$-4-2\lambda +2\lambda +\lambda^{2} +3 = 0$$
$$\lambda^{2}-1=0$$
$$\lambda^{2}=1$$
So the eigenvalues are $\lambda\_{1}=-1$ and $\lambda\_{2}=1$.
Clearly the eigenvalues are negative multiples of one another. As such, in this particular example, these eigenvalues result in the QR algorithm constantly cycling between another matrix and itself.
