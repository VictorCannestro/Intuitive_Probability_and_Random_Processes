## Notes:

#### Code to simulate a __discrete__ random variable, `X`. 

Assume in general that the possible values of `X` are `{x1, x2, ..., xN}` with probabilities `{p1, p2, ..., xN}`, respectively. Let's assume `N=3` and generate `M` values of `X`, where `M` denotes the number of __trials__. Original MATLAB code:

```MATLAB
for i=1:M
    u=rand(1,1);
    if u<=p1
        x(i,1)=x1;
    elseif u>p1 & u<=p1+p2
        x(i,1)=x2;
    elseif u>p1+p2
        x(i,1)=x3;
    end
end
```

***
The __values__ of `X` are termed the __outcomes__ or __realizations__ of `X`.

***
To generate `M` values from a [Gaussian distribution](https://numpy.org/doc/stable/reference/random/generated/numpy.random.randn.html), a __continuous__ random variable, we can use the MATLAB code:
```MATLAB
x=randn(M,1);
```

***
A __PDF__, `p_X(x)`, may be estimated by first finding the [histogram](https://matplotlib.org/3.2.2/api/_as_gen/matplotlib.pyplot.hist.html) and then dividing the number of outcomes in each bin by `M`, the total number of realizations, to obtain the probability. Moreover

![](https://latex.codecogs.com/svg.latex?P[a%20\leq%20X%20\leq%20b]%20=%20\int_{a}^{b}{p_X(x)dx})

***
To determine `P[a <= X <= b]` we generate `M` realizations of `X`, then count the number of outcomes that fall into the `[a,b]` interval and divide by `M`. Note that a large number of  realizations are needed to obtain accurate results.

***
To obtain the __average__ (aka __mean__ or __expected value)__ of a random variable $X$ we'll use the **sample mean** estimate:

![](https://latex.codecogs.com/svg.latex?\frac{1}{M}\sum_{i=1}^{M}{x_i})

***
#### Estimating a Gaussian Random Variable

![](https://github.com/VictorCannestro/Intuitive_Probability_and_Random_Processes/blob/master/figs/fig_2_7.PNG)
***
![](https://github.com/VictorCannestro/Intuitive_Probability_and_Random_Processes/blob/master/figs/fig_2_8.PNG)
***
![](https://github.com/VictorCannestro/Intuitive_Probability_and_Random_Processes/blob/master/figs/fig_2_9.PNG)
***
#### Estimating the Mean of the Square of a Gaussian Random Variable
![](https://github.com/VictorCannestro/Intuitive_Probability_and_Random_Processes/blob/master/figs/fig_2_11.PNG)
