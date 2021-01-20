<!-- 
https://latex.codecogs.com/
-->
## Notes:

- Definition of **conditional probability** (for finite sample space) is the proportion of time ![](https://latex.codecogs.com/svg.latex?A\cap%20B) occurs divided by the proportion of time ![](https://latex.codecogs.com/svg.latex?B) occurs:

![](https://latex.codecogs.com/svg.latex?P[A|B]%20=%20\frac{N_{A\cap%20B}}{N_B})

![](https://latex.codecogs.com/svg.latex?P[A|B]=\frac{\big(\frac{N_{A\cap%20B}}{N_S}\big)}{\big(\frac{N_B}{N_S}\big)})

![](https://latex.codecogs.com/svg.latex?P[A|B]%20\approx%20\frac{P[A\cap%20B]}{P[B]})

![](https://latex.codecogs.com/svg.latex?P[A|B]%20\geq%200)

Note: we must assume the **marginal probability** satisfies ![](https://latex.codecogs.com/svg.latex?P[B]%20\neq%200). Also, the event ![](https://latex.codecogs.com/svg.latex?B) comprises a new sample space, denoted as the **reduced sample space**.

***
-  If ![](https://latex.codecogs.com/svg.latex?A) and ![](https://latex.codecogs.com/svg.latex?C) are mutually exclusive events, then

![](https://latex.codecogs.com/svg.latex?P[A\cup%20C|B]%20=%20P[A|B]%20+%20P[C|B])

***
- The **Law of Total Probability** states that for a partition of the sample space ![](https://latex.codecogs.com/svg.latex?S%20=%20\bigcup_{i=1}^{N}B_i) such that ![](https://latex.codecogs.com/svg.latex?B_i\cap%20B_j%20=%20\emptyset) for ![](https://latex.codecogs.com/svg.latex?i\neq%20j) we have

![](https://latex.codecogs.com/svg.latex?P[A]%20=%20\sum_{i=1}^{N}{P[A\cap%20B_i]})

![](https://latex.codecogs.com/svg.latex?P[A]%20=\sum_{i=1}^{N}{P[A|%20B_i]P[B_i]})

***
- **Statistically Independent** events are characterized by 

![](https://latex.codecogs.com/svg.latex?P[A\cap%20B]%20=%20P[A]P[B])

***
- **Bayes Theorem** states that 

![](https://latex.codecogs.com/svg.latex?P[B|A]%20=%20\frac{P[A|B]P[B]}{P[A]})

![](https://latex.codecogs.com/svg.latex?P[B|A]%20=%20\frac{P[A|B]P[B]}{P[A|B]P[B]%20+%20P[A|B^c]P[B^c]})

where ![](https://latex.codecogs.com/svg.latex?P[B|A]) is called the **posterior probability** and ![](https://latex.codecogs.com/svg.latex?P[B]) is called the **prior probability**. Moreover, if a set of ![](https://latex.codecogs.com/svg.latex?B_i)s partition the sample space, then Baye's Theorem can be stated as

![](https://latex.codecogs.com/svg.latex?P[B_k|A]%20=%20\frac{P[A|B_k]P[B_k]}{%20\sum_{i=1}^{N}{P[A|B_i]P[B_i]}%20})

where ![](https://latex.codecogs.com/svg.latex?k=1,2,\dots,%20N) and the denominator serves to normalize the posterior probability so that the conditional probabilities, ![](https://latex.codecogs.com/svg.latex?P[B_k|A]), sum to one.

***
- The **Binomial Probability Law** describes the probability of ![](https://latex.codecogs.com/svg.latex?k) successes in ![](https://latex.codecogs.com/svg.latex?M) independent Bernoulli trials:

![](https://latex.codecogs.com/svg.latex?P[k]%20=%20{M\choose%20k}p^k(1-p)^{M-k})

***
- The **Geometric Probability Law** describes the probability of the first success at trial ![](https://latex.codecogs.com/svg.latex?k) if ![](https://latex.codecogs.com/svg.latex?M=k-1) independent Bernoulli trials have been carried out

![](https://latex.codecogs.com/svg.latex?P[k]%20=%20p(1-p)^{k-1})

***
- The **Multinomial Probability Law** describes the probability of obtaining ![](https://latex.codecogs.com/svg.latex?k_1) ![](https://latex.codecogs.com/svg.latex?s_1)'s, ![](https://latex.codecogs.com/svg.latex?k_2) ![](https://latex.codecogs.com/svg.latex?s_2)'s, ![](https://latex.codecogs.com/svg.latex?\dots), and ![](https://latex.codecogs.com/svg.latex?k_N) ![](https://latex.codecogs.com/svg.latex?s_N)'s from a sample space ![](https://latex.codecogs.com/svg.latex?S=\{s_1,%20s_2,%20\dots,%20s_N\}) where ![](https://latex.codecogs.com/svg.latex?M) independent Bernoulli trials were performed with ![](https://latex.codecogs.com/svg.latex?N) possible outcomes for each trial:


![](https://latex.codecogs.com/svg.latex?P[k_1,k_2,\dots,k_N]%20=%20%20{M%20\choose%20{k_1,k_2,\dots,k_N}}%20p_1^{k_1}%20p_2^{k_2}%20\dots%20p_N^{k_N})

where 

![](https://latex.codecogs.com/svg.latex?{M%20\choose%20{k_1,k_2,\dots,k_N}}%20=%20\frac{M!}{k_1!k_2!\dots%20k_N!}) 

and 

![](https://latex.codecogs.com/svg.latex?k_1%20+%20k_2%20+%20\dots%20+%20k_N%20=%20M)

***
- **Non-Independent Subexperiments** require the probability to be found using the probability chain rule:

![](https://latex.codecogs.com/svg.latex?P[A]%20=%20P[A_{M}|A_{M-1},\dots,A_2,A_1]P[A_{M-1}|A_{M-2},\dots,A_2,A_1]\cdots%20P[A_2|A_1]P[A_1])

If the probabilities for trial ![](https://latex.codecogs.com/svg.latex?i) depend only on the outcome of the previous trial (i.e. it has a memory of ![](https://latex.codecogs.com/svg.latex?i-1)) then the sequence is called a **Markov sequence**. We can then reexpress the probability above as

![](https://latex.codecogs.com/svg.latex?P[A]%20=%20%20P[A_{M}|A_{M-1}]P[A_{M-1}|A_{M-2}]\cdots%20P[A_2|A_1]P[A_1])

![](https://latex.codecogs.com/svg.latex?P[A]%20=%20%20P[A_1]\prod_{i=2}^{M}{P[A_i|A_{i-1}]})

where the following are called the **state transition probabilities**

![](https://latex.codecogs.com/svg.latex?P[A_{i}|A_{i-1},\dots,A_2,A_1]%20=%20P[A_i|A_{i-1}])
