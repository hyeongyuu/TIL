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
Gradient descent는 최적화 기법으로 방향(search direction)과 크기(step size)에 따라 local minimum을 탐색한다. 초기 값으로 $x_0$를 선택하고, 다음 식 $x_{k-1} = x_k - \alpha \frac{\partial{f}}{\partial{x}}$을 반복적으로 실행하며 조건을 만족하는 값을 찾는다.


## Reference
https://convex-optimization-for-all.github.io/