# Linear algebra
### 선형대수학이란?  
행렬과 벡터에 대한 학문으로 선형방정식만으로 고차원의 수식을 표현  

ex. $ ax^2 + bx + c = 0 = ax1 + bx2 + c = 0 $  

### 고유벡터, 고유값

#### 정방행렬과 선형변환
정방행렬은 선형변환을 의미. 선형변환은 좌표공간 내에서 일어날 수 있는 모든 변환으로 하나의 벡터에 확대, 축소, 회전, 반사 등을 취하여 다른 벡터로 변환 시키는 것  

ex. Ax는 x라는 벡터에 선형변환(A)를 취한 것을 의미. 벡터 x에 변환을 취한 것

#### 고유벡터
고유란 characteristic(특징)을 의미하며, 고유벡터란 직역하면 어떤 특징을 가지고 있는 벡터로 해석. (여기서 특징은 방향이 아닌 크기만 변하는 특징을 의미)  
즉, 고유벡터란 선형변환을 취했을 때, 방향은 변하지 않고 크기만 변하는 벡터를 의미

#### 고유값
고유값은 고유벡터에 선형변환을 취했을 때, 변하는 크기를 의미  

ex. 고유값이 2라면 기존 벡터 크기의 2배만큼 길어진 것, 고유값이 1/2이라면 기존 벡터 크기의 1/2만큼 줄어든 것

### Inner product(내적)과 정사영
#### 스칼라곱(Dot product)
두 벡터로부터 실수 스칼라를 얻는 연산.  
스칼라곱(dot product) $\subset$ 내적(inner product)에 포함 관계  

#### 내적 (Inner product)  
덧셈, 뺄셈, 곱셈과 같은 연산 중 하나로 벡터와 벡터의 연산을 의미. 다른 연산의 경우 '벡터 + 벡터 = 벡터', '스칼라 + 스칼라 = 스칼라'와 같이 인풋 아웃풋이 같지만, 내적은 벡터와 벡터의 연산으로 스칼라를 반환하는 것이 특이점

내적은 하나의 벡터를 transpose(전치) 시켜 다른 벡터와 곱하는 것, 또는 하나의 벡터를 다른 벡터 위로 정사영시킨 길이와 그 다른 벡터의 길이를 곱한 것을 의미 (정사영이란? 어떤 평면 위 물체에 수직방향으로 빛을 비추면 생기는 그림자)  

두 벡터가 이루는 각이 90도일 땐, 일치하는 정도가 전혀 없기 때문에 내적의 값은 0이다.

$ a \cdot b = a^Tb $  
$ a^Tb = \begin{Vmatrix*} a \\ \end{Vmatrix*} \begin{Vmatrix*} b \\ \end{Vmatrix*} \cdot cos\theta $  

**내적과 $\measuredangle(\mathbf {a},\mathbf {b})$의 관계**  
$ a \cdot b=0$ 일 필요충분조건은 $a \perp b $ 이다.  
$ a \cdot b>0$ 일 필요충분조건은 $\measuredangle(\mathbf {a},\mathbf {b})<90^{\circ} $ 이다.  
$ a \cdot b<0$ 일 필요충분조건은 $\measuredangle(\mathbf {a},\mathbf {b})>90^{\circ} $ 이다.  

#### Norm
**1-norm**  
$ \begin{Vmatrix} a \\ \end{Vmatrix}_1 := \displaystyle\sum_{i=1}^{n}|a_{i}| $

**2-norm**  
$ \begin{Vmatrix} a \\ \end{Vmatrix}_2 := \sqrt{\displaystyle\sum_{i=1}^{n}a_{i}^{2}} $

**p-norm**  
$ \begin{Vmatrix} a \\ \end{Vmatrix}_p := \Bigg( \displaystyle\sum_{i=1}^{n}a^{p} \Bigg)^{1/p} $

### 행렬의 네 가지 관점
1. 내적으로 바라보기 
2. Rank-1 matrix의 합  
3. Column space로 바라보기  
4. Row space로 바라보기  

### Span과 Column space(열공간)
#### Span
벡터들을 이용하여 온갖 선형결합을 통해 만들어진 벡터 스페이스, 또는 내가 가진 벡터로 표현할 수 있는 vector space. 전체가 10차원 공간이지만 벡터가 표현 가능한 차원이 2차원이면, span 되는 공간은 2차원

**Linear combination(선형 결합)**
벡터를 더하고 곱해서 만들 수 있는 조합. Span은 벡터의 linear combination(선형 결합)으로 나타낼 수 있는 모든 벡터를 모은 집합이라고도 표현 가능  
즉, Linear combination으로 벡터를 span 한다.

#### Column space
행렬의 열들이 span하는 vector space, 또는 열벡터로 span 할 수 있는 공간  

ex. **Row space, Column space**
<p align="left"><img src=https://raw.githubusercontent.com/hyeongyuu/TIL/main/images/linear_algebra/column_space.png height="140px" width="500px"></p>

위 이미지에서 Row space와 Column space의 차원은 동일하다. Row space에서 3개의 값이 있더라도 두 개의 행으로 만들 수 있는 최대 차원은 2차원이고, Column space에서 3개의 열로 만들 수 있는 차원도 한 평면인 2차원이 최대이다.

### Linear independent(선형 독립)과 Basis(기저)
#### Linear independent
independent 한 벡터들의 수가 곧, 벡터들이 표현할 수 있는 차원(dimension)의 수 -> 좋은(=independent) 벡터가 많아야 표현할 수 있는 범위가 넓어짐, 또는 span 하는 범위가 넓어짐

#### Basis
어떤 공간을 이루는 필수적인 구성요소. 주어진 vector space가 있을 때, 그 space를 span하는 linear independent한 벡터들로 basis는 unique하지 않다.

### Identity matrix(항등행렬), Inverse matrix(역행렬), Orthogonal matrix(직교행렬)
#### Orthogonal matrix
행벡터와 열벡터가 정규 직교 기저를 이루는 실수 행렬, 쉽게말해 행렬의 모든 컬럼들이 서로서로 직교하는 행렬. 여기서 정규 직교 기저란? '벡터의 크기가 1이고 서로 수직인 기저 벡터'를 의미  

**Orthogonal matrix 성질**
- 직교행렬의 전치행렬은 직교행렬
- 직교행렬의 역행렬은 직교행렬
- 직교행렬의 곱은 직교행렬
- 직교행렬의 행렬식은 1 또는 -1

### Rank(행렬의 계수)
행렬이 가지는 independent 한 column의 수, 또는 column space의 dimension. 행렬의 열벡터에 의해 span 된 벡터공간의 차원을 의미

### Null space(영공간)
$ A_x = 0 $ 을 만족하는 x의 집합. A가 m x n 일 때, dim(N(A)) = n - r(rank)  
Null space는 row space와 수직한 space. dim(N(A)) + dim(R(A)) = n  
주어진 행렬 A가 있을때, 행렬 A는 Column space(열공간), Row space(행공간), Null space(Null space)으로 구성된다.

### Ax = b 의 해의 수
- full column rank 일 때, 해가 없거나 한 개
- full row rank 일 때, 해가 무한
- full rank, 해가 한 개
- rank-deficient 일 때, b가 C(A)에 들어있다면 무한, 들어있지 않으면 해가 없다.