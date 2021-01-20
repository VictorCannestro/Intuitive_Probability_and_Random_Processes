## Notes:

The **Expected Value** ( the _mean_ ) of a discrete random variable ![](https://latex.codecogs.com/svg.latex?X) is _the best predictor of the outcome of the experiment_ (i.e. it minimizes the MSE) and is defined as

![](https://latex.codecogs.com/svg.latex?\mathbb{E}[X]%20=%20\sum_{i}x_ip_X[x_i])

Moreover, if ![](https://latex.codecogs.com/svg.latex?X) only takes on integer values

![](https://latex.codecogs.com/svg.latex?\mathbb{E}[X]%20=%20\sum_{k=-\infty}^{\infty}kp_X[k])

- Is a _linear_ operator

***
The **Expected Value of a function** of a discrete random variable ![](https://latex.codecogs.com/svg.latex?Y%20=%20g(X)) is defined as

![](https://latex.codecogs.com/svg.latex?\mathbb{E}[Y]%20=%20\sum_{i}{g(x_i)p_X[x_i]})

- ![](https://latex.codecogs.com/svg.latex?\mathbb{E}[g(X)]%20\neq%20g(\mathbb{E}[X]))

***
The **Variance** of a discrete random variable increases with the _width_ of the PMF and is defined as

![](https://latex.codecogs.com/svg.latex?var(X)%20=%20\mathbb{E}[(X%20-%20\mathbb{E}[X])^2])

![](https://latex.codecogs.com/svg.latex?var(X)%20=%20\mathbb{E}[X^2]%20-%20\mathbb{E}^2[X])

![](https://latex.codecogs.com/svg.latex?var(X)%20\geq%200)

#### Properties:

- Variance is a _nonlinear_ operator
- ![](https://latex.codecogs.com/svg.latex?var(c)%20=%200) for a constant ![](https://latex.codecogs.com/svg.latex?c\in\mathbb{R})
- ![](https://latex.codecogs.com/svg.latex?var(X+c)%20=%20var(X)) for a constant ![](https://latex.codecogs.com/svg.latex?c\in\mathbb{R})
- ![](https://latex.codecogs.com/svg.latex?var(cX)%20=%20c^2var(X)) for a constant ![](https://latex.codecogs.com/svg.latex?c\in\mathbb{R})
- ![](https://latex.codecogs.com/svg.latex?MSE_{\min}%20=%20\mathbb{E}[(X%20-%20b_{opt})^2]%20=%20\mathbb{E}[(X%20-%20\mathbb{E}[X])^2]%20=%20var(X))

***
The **Characteristic Function** of a discrete random variable, ![](https://latex.codecogs.com/svg.latex?X): Let ![](https://latex.codecogs.com/svg.latex?S_X) is a subset of the integers, then

![](https://latex.codecogs.com/svg.latex?\phi_X(\omega)%20=%20\mathbb{E}[e^{j\omega%20X}])

![](https://latex.codecogs.com/svg.latex?\phi_X(\omega)%20=%20\sum_{k=-\infty}^{\infty}{e^{j\omega%20X}p_X[k]})

where ![](https://latex.codecogs.com/svg.latex?j%20=%20\sqrt{-1}) and ![](https://latex.codecogs.com/svg.latex?\omega) takes on a suitable range of values, and ![](https://latex.codecogs.com/svg.latex?p_X[k]=0) for those integers not included in ![](https://latex.codecogs.com/svg.latex?S_X). This is also the **Fourier Transform** of the sequence ![](https://latex.codecogs.com/svg.latex?p_X[k]) for ![]( https://latex.codecogs.com/svg.latex?k\in(-\infty,\infty) ). It is useful in examining the convergence of PMFs.

#### Properties:

- The Characteristic Function always exists since ![](https://latex.codecogs.com/svg.latex?|\phi_X(\omega)|%20%3C%20\infty)
- Is periodic with period ![](https://latex.codecogs.com/svg.latex?2\pi)
- Convergnece of the Characteristic Function guarantees convergence of PMFs (i.e. we can approximate PMFs by simpler ones if we can show that the Characteristic Functions are approximately equal)
- The PMF may be recovered from the Characteristic Function via **Inverse Fourier Transform**:

![](https://latex.codecogs.com/svg.latex?p_X[k]%20=%20\frac{1}{2\pi}\int_{-\pi}^{\pi}{\phi_X(\omega)e^{-j\omega%20k}d\omega})

for ![]( https://latex.codecogs.com/svg.latex?k\in(-\infty,\infty) ).

***
The ![](https://latex.codecogs.com/svg.latex?N^{th}) **Moment** of a discrete random variable, ![](https://latex.codecogs.com/svg.latex?X):

![](https://latex.codecogs.com/svg.latex?\mathbb{E}[X^N]%20=%20\frac{1}{j^N}%20\frac{d^N}{d\omega^N}\phi_X(\omega)\bigg|_{\omega=0})

***
**Estimated Mean** ( the _sample mean_ ) given ![](https://latex.codecogs.com/svg.latex?N) trials:

![](https://latex.codecogs.com/svg.latex?\widehat{\mathbb{E}[X]}%20=%20\frac{1}{N}\sum_{i=1}^{N}{x_i})

***
**Estimated Variance** given ![](https://latex.codecogs.com/svg.latex?N) trials:

![](https://latex.codecogs.com/svg.latex?\widehat{var(X)}%20=%20\frac{1}{N}\sum_{i=1}^{N}{x_i^2}%20-%20\widehat{\mathbb{E}[X]}^2) 
