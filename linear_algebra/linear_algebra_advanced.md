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

### 주성분 분석(PCA. Principal Component Analysis)

### 특이값 분해(SVD. Sigular Vector Decomposition)

### 의사역행렬