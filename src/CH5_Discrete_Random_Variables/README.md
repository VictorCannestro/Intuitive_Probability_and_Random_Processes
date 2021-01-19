## Notes:

**Definition of a Discrete Random Variable**: The _function_ $X(\cdot)$ that maps $S$ into $S_X$. Note that the name "random variable" is a poor description in that the _function_ $X(\cdot)$ is not random, however, it's inputs and outputs are random. We'll denote $X$ as the random variable and $x_i$ as it's value:

$$
X(s_i) = x_i.
$$


***
**PMF of a Discrete Random Variable**:

$$
\begin{equation}
    \begin{split}
        p_X[x_i] &= P[X(s) = x_i] \\
                 \\
                 &= P[\{s_j: X(s_j) = x_i\}] \\
                 \\
                 &= \sum_{\{j:X(s_j)=x_i\}}{P[\{s_j\}]}
    \end{split}
\end{equation}
$$


***
**Transformation of a Random Variable** $Y=g(X)$. The PMF is:

$$
\begin{equation}
    \begin{split}
        p_Y[y_i] &= P[g(x_j) = y_i] \\
                 \\
                 &= \sum_{\{j:g(x_j)=y_i\}}{p_X[x_j]}.
    \end{split}
\end{equation}
$$

***
The **Cumulative Distribution Function (CDF):** for a random variable $X$ is the "running sum" which adds up the probabilities of the PMF starting at $-\infty$ and ending at $\infty$. It is the probabilites that $X$ lies in the semi-interval $(-\infty,x]$:

$$
F_X(x) = P[X\leq x]
$$

for $-\infty < x < \infty$ where $X=x$ **is included** in the interval.

#### Properties:

- $p_X[x] = F_X(x^+) - F_X(x^-)$


- $F_X(x)\in[0,1]$


- CDF is monotonically increasing


- CDF is _right-continuous:_ $\lim\limits_{x\rightarrow x^+}{F_X(x)} = F_X(x_0)$ 


- $P[a<X\leq b] = F_X(b^+) - F_X(a^+)$


- $P[a\leq X\leq b] = F_X(b^+) - F_X(a^-)$


- $\lim\limits_{x\rightarrow -\infty}{F_X(x)} = 0$


- $\lim\limits_{x\rightarrow \infty}{F_X(x)} = 1$


***
**Estimated PMF:** For _finite sample spaces_ , the PMF $p_X[k] = P[X=k]$ can be estimated as 

$$
\hat p_X[k] = \frac{\text{Number of outcomes equal to } k}{M}
$$

for $M$ realizations of the random variable $X$. 


***
**Estimated CDF:** For _finite sample spaces_ , the CDF $F_X(x)$ can be estimated as

$$
\begin{equation}
    \begin{split}
        \hat F_X(x) &= \sum_{\{k:k\leq x\}}\hat p_X[k] \\
                    \\
                    &= \frac{\text{Number of outcomes } \leq x}{M}
    \end{split}
\end{equation}
$$

for $M$ realizations of the random variable $X$. 