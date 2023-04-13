# Convex optimization Basic

### Convex optimization problem
Optimization problem은 선택가능한 값 중에서 최적의 해 또는 최적의 해에 근접한 값을 찾는 문제로, 머신러닝에서 cost function을 최소화 시키는 모델 파라미터를 구하는 작업이 대표적인 optimization problem이다.

Convex optimization problem은 $f(x)$가 convex고 feasible set이 convex한 optimization problem을 칭한다. 모든 $x_1, x_2\in S$(feasible set)이면서, $\alpha x_1 + (1-\alpha)x_2\in S, (\alpha \in [0,1])$를 만족해야 한다.

**Convex function**  
<p align="left"><img src=https://raw.githubusercontent.com/hyeongyuu/TIL/main/images/convex_optimization/convex_function.png height="150px" width="350px"></p>

모든 $x_1, x_2 \in$ 정의역, $\alpha \in [0,1]$에 대해서 $f(\alpha x_1 + (1-\alpha)x_2) = \alpha f(x_1) + (1-\alpha)f(x_2)$를 만족한다. 위 그래프에서 임의의 두 점$(x,f(x)), (y,f(y))$에 대해서 두 점을 잇는 선분을 $x$축 관점에서 본다면, $[x,y]$ 구간 안의 값을 갖는다. 즉, $f(x), f(y)$보다 큰 값을 가질 수 없다.

**Convex set**
<p align="left"><img src=https://raw.githubusercontent.com/hyeongyuu/TIL/main/images/convex_optimization/convex_set.png height="150px" width="400px"></p>

어떤 집합(set)의 원소인 두 점 $x1, x2$를 잇는 선분이 이 집합에 다시 포함되는 집합을 convex set이라고 부른다. 즉, feasible set이 convex한 경우를 의미하면서, 두 점을 잇는 선분 위 값들이 모두 집합(set)에 포함되어 있어야 한다.


### Gradient descent
Gradient descent는 최적화 기법으로 방향(search direction)과 크기(step size)에 따라 local minimum을 탐색한다. 초기 값으로 $x_0$를 선택하고, 다음 식 $x_{k-1} = x_k - \alpha \frac{df}{dx}$을 반복적으로 실행하며 조건을 만족하는 값을 찾는다.

$\vec{Z} = \vec{x} + \vec{n}$이고, $f = (\vec{Z} - \vec{x})^2$일때, $(\vec{Z} - \vec{x}) ^2$(행렬의 제곱)은 전치(Transpose)로 표현한다. 즉, $f = (\vec{Z} - \vec{x})^T(\vec{Z} - \vec{x})$로 나타낸다.

위 식을 활용해 $\vec{Z} = A\vec{x} + \vec{n}$일때, $f = (\vec{Z}-A\vec{x})^T(\vec{Z}-A\vec{x})$라면, 미분을 통해 $df = -2(\vec{Z}-A{\vec{x}})^Td\vec{x}$를 도출할 수 있다.

#### 스칼라, 벡터, 행렬 미분
>Scalar(스칼라)는 소문자 $x,y,z$로 표기  
Vector(벡터)는 볼드체 소문자 **x, y, z**로 표기(or $\vec{x}, \vec{y}, \vec{z}$)  
Matrix(행렬)는 볼드체 대문자 **X, Y, Z**로 표기

스칼라, 벡터, 행렬 미분은 아래 표와 같은 형태로 나타낼 수 있다.
<p align="left"><img src=https://raw.githubusercontent.com/hyeongyuu/TIL/main/images/convex_optimization/type_of_derivative.png height="180px" width="300px"></p>

상수벡터 $\vec{a}$와 열벡터 $\vec{x}$에 대해 $\vec{a}^T\vec{x}$를 $\vec{x}$로 미분하면 결과값은 $\vec{a}^T$이다.

$\vec{a}^T\vec{x} = a_1x_1 + a_2x_2 ... + a_nx_n$을 벡터 $\vec{x}$로 미분하면, $[\frac{\partial(a_1x_1 + ... + a_nx_n)}{\partial x_1} ... \frac{\partial(a_1x_1 + ... + a_nx_n)}{\partial x_n}]$으로 벡터의 각 스칼라에 대해 편미분한다. 그 결과 $\frac{\partial(a_1x_1 + ... + a_nx_n)}{\partial x_1} = a_1, \frac{\partial(a_1x_1 + ... + a_nx_n)}{\partial x_n} = a_n$을 통해 최종적으로 $\frac{\partial \vec{a}^T\vec{x}}{\partial \vec{x}} = [a_1...a_n] = \vec{a}^T$와 같이 된다.


<!-- $Z = A\vec{x} + n$, $f = (Z - Ax)^T(Z - Ax)$  
$df = \frac{\partial{f}}{\partial{x^T}}dx$ -->



## Reference
https://convex-optimization-for-all.github.io/  
https://en.wikipedia.org/wiki/Matrix_calculus
