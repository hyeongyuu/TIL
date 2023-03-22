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

## 스칼라곱(Dot product)
스칼라곱. 두 벡터로부터 실수 스칼라를 얻는 연산  
스칼라곱(dot product) $\subset$ 내적(inner product)에 포함 관계  

내적. 한 벡터를 다른 벡터 위로 정사영시킨 길이와 그 다른 벡터의 길이를 곱한 것  
>**내적은 정사영(projection)이다.**

벡터에는 방향이 있으므로, 방향이 일치하는 만큼만 곱한다. 예를 들어 두 벡터의 방향이 같으면, 두 벡터의 크기를 그냥 곱한다. **두 벡터가 이루는 각이 90도일 땐, 일치하는 정도가 전혀 없기 때문에 내적의 값은 0이다.** 내적은 한 벡터를 다른 벡터로 정사영 시켜서, 그 벡터의 크기를 곱한다.  


- $a \cdot b=0$ 일 필요충분조건은 $a \perp b$ 이다.
- $a \cdot b>0$ 일 필요충분조건은 $\measuredangle(\mathbf {a},\mathbf {b})<90^{\circ}$ 이다.
- $a \cdot b<0$ 일 필요충분조건은 $\measuredangle(\mathbf {a},\mathbf {b})>90^{\circ}$ 이다.


$$a = \begin{bmatrix} 1 \\ 3 \end{bmatrix}, b = \begin{bmatrix} 5 \\ 1 \end{bmatrix}$$  
$$a \cdot b = 8 = a^Tb = b^Ta$$


$a^Tb = \begin{Vmatrix}a\\\end{Vmatrix} \cdot \begin{Vmatrix}b\\\end{Vmatrix} \cdot cos\theta$  
$a^Tb = \begin{Vmatrix}a\\\end{Vmatrix} \cdot cos\theta \cdot \begin{Vmatrix}b\\\end{Vmatrix}$  
$a^Ta = \begin{Vmatrix}a\\\end{Vmatrix} \cdot \begin{Vmatrix}a\\\end{Vmatrix} = \begin{Vmatrix}a\\\end{Vmatrix}^2$

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



