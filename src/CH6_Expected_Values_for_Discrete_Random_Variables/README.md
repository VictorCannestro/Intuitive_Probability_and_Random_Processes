## Notes:

The **Expected Value** (the _mean_ ) of a discrete random variable $X$ is _the best predictor of the outcome of the experiment_ (i.e. it minimizes the MSE) and is defined as

$$
\mathbb{E}[X] = \sum_{i}x_ip_X[x_i]
$$

Moreover, if $X$ only takes on integer values

$$
\mathbb{E}[X] = \sum_{k=-\infty}^{\infty}kp_X[k]
$$

- Is a _linear_ operator

***
The **Expected Value of a function** of a discrete random variable $Y = g(X)$ is defined as

$$
\mathbb{E}[Y] = \sum_{i}{g(x_i)p_X[x_i]}
$$

- $\mathbb{E}[g(X)] \neq g(\mathbb{E}[X])$

***
The **Variance** of a discrete random variable increases with the _width_ of the PMF and is defined as

$$
\begin{equation}
    \begin{split}
        var(X) &= \mathbb{E}[(X - \mathbb{E}[X])^2] \\
               &= \mathbb{E}[X^2] - \mathbb{E}^2[X] \\
               &\geq 0
    \end{split}
\end{equation}
$$

#### Properties:

- Variance is a _nonlinear_ operator
- $var(c) = 0$ for a constant $c\in\mathbb{R}$
- $var(X+c) = var(X)$ for a constant $c\in\mathbb{R}$
- $var(cX) = c^2var(X)$ for a constant $c\in\mathbb{R}$
- $MSE_{\min} = \mathbb{E}[(X - b_{opt})^2] = \mathbb{E}[(X - \mathbb{E}[X])^2] = var(X)$

***
The **Characteristic Function** of a discrete random variable, $X$: Let $S_X$ is a subset of the integers, then

$$
\begin{equation}
    \begin{split}
        \phi_X(\omega) &= \mathbb{E}[e^{j\omega X}] \\
                       &= \sum_{k=-\infty}^{\infty}{e^{j\omega X}p_X[k]}
    \end{split}
\end{equation}
$$

where $j = \sqrt{-1}$ and $\omega$ takes on a suitable range of values, and $p_X[k]=0$ for those integers not included in $S_X$. This is also the **Fourier Transform** of the sequence $p_X[k]$ for $k\in(-\infty,\infty)$. It is useful in examining the convergence of PMFs.

#### Properties:

- The Characteristic Function always exists since $|\phi_X(\omega)| < \infty$
- Is periodic with period $2\pi$
- Convergnece of the Characteristic Function guarantees convergence of PMFs (i.e. we can approximate PMFs by simpler ones if we can show that the Characteristic Functions are approximately equal)
- The PMF may be recovered from the Characteristic Function via **Inverse Fourier Transform**:

$$
p_X[k] = \frac{1}{2\pi}\int_{-\pi}^{\pi}{\phi_X(\omega)e^{-j\omega k}d\omega}
$$

for $k\in(-\infty,\infty)$.

***
The **$N^{th}$ Moment** of a discrete random variable, $X$:

$$
\mathbb{E}[X^N] = \frac{1}{j^N} \frac{d^N}{d\omega^N}\phi_X(\omega)\bigg|_{\omega=0}
$$

***
**Estimated Mean** (the _sample mean_ ) given $N$ trials:

$$
\widehat{\mathbb{E}[X]} = \frac{1}{N}\sum_{i=1}^{N}{x_i}
$$

***
**Estimated Variance** given $N$ trials:

$$
\widehat{var(X)} = \frac{1}{N}\sum_{i=1}^{N}{x_i^2} - \bigg( \frac{1}{N}\sum_{i=1}^{N}{x_i} \bigg)^2
$$