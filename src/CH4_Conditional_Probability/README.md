## Notes:

- Definition of **conditional probability** (for finite sample space) is the proportion of time $A\cap B$ occurs divided by the proportion of time $B$ occurs:

$$
\begin{equation}
    \begin{split}
        P[A|B] &= \frac{N_{A\cap B}}{N_B} \\
               &= \frac{\big(\frac{N_{A\cap B}}{N_S}\big)}{\big(\frac{N_B}{N_S}\big)} \\
               &\approx \frac{P[A\cap B]}{P[B]} \\
               &\geq 0
    \end{split}
\end{equation}
$$

Note: we must assume the **marginal probability** satisfies $P[B] \neq 0$. Also, the event $B$ comprises a new sample space, denoted as the **reduced sample space**.

***
-  If $A$ and $C$ are mutually exclusive events, then

$$
P[A\cup C|B] = P[A|B] + P[C|B]
$$

***
- The **Law of Total Probability** states that for a partition of the sample space $S = \bigcup_{i=1}^{N}B_i$ such that $B_i\cap B_j = \emptyset$ for $i\neq j$ we have

$$
\begin{equation}
    \begin{split}
        P[A] &= \sum_{i=1}^{N}{P[A\cap B_i]} \\
             &= \sum_{i=1}^{N}{P[A| B_i]P[B_i]}
    \end{split}
\end{equation}
$$

***
- **Statistically Independent** events are characterized by $P[A\cap B] = P[A]P[B]$

***
- **Bayes Theorem** states that 

$$
\begin{equation}
    \begin{split}
        P[B|A] &= \frac{P[A|B]P[B]}{P[A]} \\
               &= \frac{P[A|B]P[B]}{P[A|B]P[B] + P[A|B^c]P[B^c]}
    \end{split}
\end{equation}
$$

where $P[B|A]$ is called the **posterior probability** and $P[B]$ is called the **prior probability**. Moreover, if a set of $B_i$s partition the sample space, then Baye's Theorem can be stated as

$$
P[B_k|A] = \frac{P[A|B_k]P[B_k]}{ \sum_{i=1}^{N}{P[A|B_i]P[B_i]} }
$$

where $k=1,2,\dots, N$ and the denominator serves to normalize the posterior probability so that the conditional probabilities, $P[B_k|A]$, sum to one.

***
- The **Binomial Probability Law** describes the probability of $k$ successes in $M$ independent Bernoulli trials:

$$
P[k] = {M\choose k}p^k(1-p)^{M-k}
$$

***
- The **Geometric Probability Law** describes the probability of the first success at trial $k$ if $M=k-1$ independent Bernoulli trials have been carried out

$$
P[k] = p(1-p)^{k-1}
$$

***
- The **Multinomial Probability Law** describes the probability of obtaining $k_1$ $s_1$'s, $k_2$ $s_2$'s, $\dots$, and $k_N$ $s_N$'s from a sample space $S=\{s_1, s_2, \dots, s_N\}$ where $M$ independent Bernoulli trials were performed with $N$ possible outcomes for each trial:
<br></br><br></br>
$$
P[k_1,k_2,\dots,k_N] =  {M \choose {k_1,k_2,\dots,k_N}} p_1^{k_1} p_2^{k_2} \dots p_N^{k_N}
$$
<br></br>
where ${M \choose {k_1,k_2,\dots,k_N}} = \frac{M!}{k_1!k_2!\dots k_N!}$ and $k_1 + k_2 + \dots + k_N = M$.

***
- **Non-Independent Subexperiments** require the probability to be found using the probability chain rule:

$$
P[A] = P[A_{M}|A_{M-1},\dots,A_2,A_1]P[A_{M-1}|A_{M-2},\dots,A_2,A_1]\cdots P[A_2|A_1]P[A_1].
$$

If the probabilities for trial $i$ depend only on the outcome of the previous trial (i.e. it has a memory of $i-1$) then the sequence is called a **Markov sequence**. We can then reexpress the probability above as

$$
\begin{equation}
    \begin{split}
        P[A] &=  P[A_{M}|A_{M-1}]P[A_{M-1}|A_{M-2}]\cdots P[A_2|A_1]P[A_1] \\
             \\
             &= P[A_1]\prod_{i=2}^{M}{P[A_i|A_{i-1}]}
    \end{split}
\end{equation}
$$

where the following are called the **state transition probabilities**

$$
P[A_{i}|A_{i-1},\dots,A_2,A_1] = P[A_i|A_{i-1}].
$$
