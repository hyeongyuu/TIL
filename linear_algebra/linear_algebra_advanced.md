# Linear algebra Advanced

### 고유값(Eigenvalue)과 고유벡터(Eigenvector)
$Av = \lambda v$를 만족시키는 $\lambda$는 고유값(eigenvalue), $v$는 고유벡터(eigenvector)  
$A$를 하나의 함수로 보고, $v$가 함수 $A$를 통과해 $Av$로 선형변환 된 것으로 볼 수 있음.  

$Av-\lambda v=(A-\lambda I)v=0$  
- $det(A-\lambda I)=0$을 만족시키는 $\lambda$
    - $(A-\lambda I)$가 역행렬을 갖는다면, 양변에 역행렬을 곱해 $v=0$ 밖에 없음을 의미
    - 즉, $(A-\lambda I)$가 역행렬을 갖지 않기 위해 $det(A-\lambda I)=0$을 만족해야함
- $Nullspace(A-\lambda I)$에 존재하는 $v$
    - Nullspace의 basis를 eigenvector로 삼는다

**행렬식(Determinant)**  
행렬식 값이 0이면, 그 행렬의 역행렬은 존재하지 않는다는 것을 의미  
반대로, 행렬식 값이 0이 아니면, 그 행렬의 역행렬은 존재한다는 것을 의미  

행렬식의 절대값은 도형의 부피로 생각할 수 있음.  
행렬식이 0이라는 것은 행렬을 구성하는 벡터가 영벡터가 아닌데 각 벡터로 구성된 도형의 부피가 0이라는 사실 -> 행렬을 구성하는 벡터가 서로 동일선상(colinear)에 있다는 것을 의미


### 고유값 분해(Eigendecomposition)
행렬 $A$(2x2)가 고유값(eigenvalue), 고유벡터(eigenvector)를 2개씩 갖는다면 $A_{v1}=\lambda_{1}v_{1}$, $A_{v2}=\lambda_{2}v_{2}$ 만족한다. 여기서 $A[v_1, v_2] = [\lambda_{1}v_{1}, \lambda_{2}v_{2}]$ 로 변환하고, 우변의 $[\lambda_1, \lambda_2]$를 대각행렬(diagonal matrix)로 변환하여 $A = V\Lambda V^{-1}$라는 식을 도출한다. 이를 A를 고유값 분해(eigendecomposition)한다고 표현한다.

앞의 식($A = V\Lambda V^{-1}$)을 변형하여 $V^{-1}AV = \Lambda$를 도출하고, 여기서 $A$는 대각행렬(diagonal matrix)$\Lambda$로 표현 할 수 있으며, 이를 diagonalizable이라 한다. 그리고 고유값 분해(eigendecompsition)가 가능한 행렬을 diagonalizable하다고 하며, independent한 eigenvector가 n개 있다.

- $A^k = V\Lambda^kV^{-1}$
- $A^{-1} = (V\Lambda V^{-1})^{-1} = V\Lambda^{-1}V^{-1}$
- $det(A) = det(V\Lambda V^{-1}) = det(V)det(\Lambda)det(V^{-1}) = det(\Lambda)= \lambda_1\lambda_2...$
- $tr(A) = tr(V\Lambda V^{-1}) = tr(\Lambda V^{-1}V) = tr(\Lambda) = \lambda_1 + \lambda_2 ...$
- Rank-dificient <=> $det(A)=0$ <=> $0$인 eigenvalue가 하나 이상 존재

**Diagonalizable matrix의 non-zero eigenvalue의 수 = rank(A)**, rank는 $\Lambda$의 non-zero인 eigenvalue의 수와 같음  
**대칭행렬(Symmetric matrix)는 diagonalizable이며,** $A=Q\Lambda Q^{T}$**가 된다.** 대칭행렬은 성질 $A = A^T$를 만족하기 때문에, $A^T = V^{-T}\Lambda V^{T}$로 표현 가능하며, $V = V{-T}$ -> $V^{-1} = V^{T}$를 만족한다.


### 주성분 분석(PCA. Principal Component Analysis)

### 특이값 분해(SVD. Sigular Vector Decomposition)

### 의사역행렬