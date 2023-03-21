# Linear algebra

$ax^2 + bx + c = 0 = ax1 + bx2 + c = 0$  
선형대수학 : 행렬과 벡터에 대한 학문

## Transpose
1. $(A^T)^T = A$
2. $(A + B)^T = A^T + B^T$
3. $(AB)^T = B^TA^T$  
$(A^TA)^T = A^TA$
4. $(kA)^T = kA^T (k는 임의의 상수)$
5. $det(A^T) = det(A)$
6. $(A^T)^{-1} = (A^{-1})^T$

## Dot product
$A = \begin{bmatrix}1\\3\\ \end{bmatrix}$,  $B = \begin{bmatrix}5\\1\\ \end{bmatrix}$

$A \cdot B = 8 = A^TB = B^TA$

내적은 정사영(projection)이다

$A^TB = \begin{Vmatrix}A\\\end{Vmatrix} \cdot \begin{Vmatrix}B\\\end{Vmatrix} \cdot cos\theta$  
$A^TB = \begin{Vmatrix}A\\\end{Vmatrix} \cdot cos\theta \cdot \begin{Vmatrix}B\\\end{Vmatrix}$  
$A^TA = \begin{Vmatrix}A\\\end{Vmatrix} \cdot \begin{Vmatrix}A\\\end{Vmatrix} = \begin{Vmatrix}A\\\end{Vmatrix}^2$

### 단위 벡터(unit vector)
- 크기가 1인 벡터
- $a\over\sqrt{a^Ta}$ $=$ $a\over\begin{Vmatrix}a\\\end{Vmatrix}$ $: Normalize$ 

$a^Tb = \begin{Vmatrix}a\\\end{Vmatrix} cos\theta \begin{Vmatrix}b\\\end{Vmatrix}$  
$\begin{Vmatrix}a\\\end{Vmatrix} cos\theta=$ $a^Tb\over\sqrt{b^Tb}$  

### 정사영된 벡터 구하기


## Norm
### 2-norm
$a= \begin{bmatrix}1\\2\\3\\ \end{bmatrix}, \begin{Vmatrix}a\\\end{Vmatrix}=\sqrt{a^Ta}=\sqrt{1^2+2^2+3^2}=(\left\vert 1 \right\vert^2 + \left\vert 2 \right\vert^2 + \left\vert 3 \right\vert^2)^\frac{1}{2}$

### 1-norm
$b = \begin{bmatrix}1\\2\\-3\\ \end{bmatrix}, \begin{Vmatrix}b\\\end{Vmatrix}= \left\vert 1 \right\vert^1 + \left\vert 2 \right\vert^1 +  \left\vert -3 \right\vert^1=6$

### p-norm
