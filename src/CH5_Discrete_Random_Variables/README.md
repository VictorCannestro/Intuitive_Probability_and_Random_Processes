## Notes:

**Definition of a Discrete Random Variable**: The _function_ ![](https://latex.codecogs.com/svg.latex?X(\cdot)) that maps ![](https://latex.codecogs.com/svg.latex?S) into ![](https://latex.codecogs.com/svg.latex?S_X). Note that the name "random variable" is a poor description in that the _function_ ![](https://latex.codecogs.com/svg.latex?X(\cdot)) is not random, however, it's inputs and outputs are random. We'll denote ![](https://latex.codecogs.com/svg.latex?X) as the random variable and ![](https://latex.codecogs.com/svg.latex?x_i) as it's value:

![](https://latex.codecogs.com/svg.latex?X(s_i)%20=%20x_i)

***
**PMF of a Discrete Random Variable**:

![](https://latex.codecogs.com/svg.latex?p_X[x_i]%20=%20P[X(s)%20=%20x_i])

![](https://latex.codecogs.com/svg.latex?p_X[x_i]%20=%20P[\{s_j:%20X(s_j)%20=%20x_i\}])

![](https://latex.codecogs.com/svg.latex?p_X[x_i]%20=%20\sum_{\{j:X(s_j)=x_i\}}{P[\{s_j\}]})

***
**Transformation of a Random Variable** $Y=g(X)$. The PMF is:

![](https://latex.codecogs.com/svg.latex?p_Y[y_i]%20=%20P[g(x_j)%20=%20y_i])

![](https://latex.codecogs.com/svg.latex?p_Y[y_i]%20=%20\sum_{\{j:g(x_j)=y_i\}}{p_X[x_j]})

***
The **Cumulative Distribution Function (CDF):** for a random variable ![](https://latex.codecogs.com/svg.latex?X) is the "running sum" which adds up the probabilities of the PMF starting at ![](https://latex.codecogs.com/svg.latex?-\infty) and ending at ![](https://latex.codecogs.com/svg.latex?\infty). It is the probabilites that ![](https://latex.codecogs.com/svg.latex?X) lies in the semi-interval ![](https://latex.codecogs.com/svg.latex?(-\infty,x]):

![](https://latex.codecogs.com/svg.latex?F_X(x)%20=%20P[X\leq%20x])

for ![](https://latex.codecogs.com/svg.latex?-\infty%20%3C%20x%20%3C%20\infty) where ![](https://latex.codecogs.com/svg.latex?X=x) **is included** in the interval.

#### Properties:

- ![](https://latex.codecogs.com/svg.latex?p_X[x]%20=%20F_X(x^+)%20-%20F_X(x^-))

- ![](https://latex.codecogs.com/svg.latex?F_X(x)\in%20[0,1])

- CDF is monotonically increasing

- CDF is _right-continuous:_ ![](https://latex.codecogs.com/svg.latex?\lim\limits_{x\rightarrow%20x^+}{F_X(x)}%20=%20F_X(x_0)) 

- ![](https://latex.codecogs.com/svg.latex?P[a%3CX\leq%20b]%20=%20F_X(b^+)%20-%20F_X(a^+))

- ![](https://latex.codecogs.com/svg.latex?P[a\leq%20X\leq%20b]%20=%20F_X(b^+)%20-%20F_X(a^-))

- ![](https://latex.codecogs.com/svg.latex?\lim\limits_{x\rightarrow%20-\infty}{F_X(x)}%20=%200)

- ![](https://latex.codecogs.com/svg.latex?\lim\limits_{x\rightarrow%20\infty}{F_X(x)}%20=%201)

***
**Estimated PMF:** For _finite sample spaces_ , the PMF ![](https://latex.codecogs.com/svg.latex?p_X[k]%20=%20P[X=k]) can be estimated as 

![](https://latex.codecogs.com/svg.latex?\hat%20p_X[k]%20=%20\frac{\text{Number%20of%20outcomes%20equal%20to%20}%20k}{M})

for ![](https://latex.codecogs.com/svg.latex?M) realizations of the random variable ![](https://latex.codecogs.com/svg.latex?X). 

***
**Estimated CDF:** For _finite sample spaces_ , the CDF ![](https://latex.codecogs.com/svg.latex?F_X(x)) can be estimated as

![](https://latex.codecogs.com/svg.latex?\hat%20F_X(x)%20=%20\sum_{\{k:k\leq%20x\}}\hat%20p_X[k])

![](https://latex.codecogs.com/svg.latex?\hat%20F_X(x)%20=%20\frac{\text{Number%20of%20outcomes%20}%20\leq%20x}{M})

for ![](https://latex.codecogs.com/svg.latex?M) realizations of the random variable ![](https://latex.codecogs.com/svg.latex?X). 
