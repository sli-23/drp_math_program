# Markov Chain

### Definitions

* A **Markov chain** is a mathematical system that experiences transitions from one state to another according to certain [probabilistic](https://brilliant.org/wiki/probability-rule-of-product/) rules.
* It is one of the common _**stochastic process** _ (the process of some values changing randomly over time)_._
* The probability of any state transition is independent of time.

A _stochastic process_ $$X = { X(t): t \in T}$$  is a collection of random variables:

* The index of $$t$$ often represents time, and in that case the process $$X$$models the value of a random variables $$X$$that changes over time.
* We call $$X(t)$$ the _state_ of process at time $$t$$. We use $$X_t$$ interchangeably with $$X_t$$.

#### **Markov property**

A discrete time stochastic process $$X_0, X_1, X_2, ...$$ is a Markov chain if

$$
\begin{aligned} P(X_t = a_1 | X_{t - 1} = a_{t - 1}, X_{t - 2} = a_{t - 2}, ..., X_0 = a_0) &= P(X_t = a_t | X_{t - 1} = a_{t - 1}) \\ &= P_{a_{t - 1}, a_t}.\\ \end{aligned}
$$

* This definition expresses that the state $$X_t$$ depends on the precious state $$X_{t - 1}$$ but is independent of the particular history of how the process arrived at state $$X_{t -1}$$.

{% hint style="warning" %}
It does not imply that $$X_t$$ is independent of the random variables $$X_t$$ is independent of the random variables $$X_0, X_1, ..., X_{t-1}$$; **it just implies that any dependency of** $$X_t$$ **on** **the past is captured in the value of** $$X_{t - 1}$$.
{% endhint %}

* It differs from a general stochastic process in that a Markov chain must be "**memory-less**." That is, (the probability of) future actions are <mark style="color:blue;">**not dependent**</mark> upon the steps that led up to the present state.

**The transition probability**:

$$
P_{i,j} = P(X_t = j | X_{t - 1} = i)
$$

is the probability that the process moves from $$i$$ to $$j$$ in one step.

* **Example**: A variant of the same question asks once again for ball color, but it allows replacement each time a ball is drawn. This creates a stochastic process with color for the random variable, which satisfies the Markov property.

**The transition matrix:**

$$
P = \begin{pmatrix}P_{0,0}&P_{0,1}&\cdots&P_{0,j} & \cdots\\P_{1,0}&P_{1,1}&\cdots&P_{1,j}& \cdots\\\vdots& \vdots &\ddots & \vdots & \ddots\\P_{i,0}& P_{i,1}&\cdots & P_{i,j} & \cdots \\ \vdots & \vdots & \ddots & \vdots & \ddots\end{pmatrix}
$$

That is, the entry in $$i$$th row and $$j$$th column is the transition probability $$P_{i,j}$$. It follows that, for all $$i, \sum_{j \geq 0} P_{i,j} = 1$$.

* A **transition matrix** $$P$$​ for Markov chain at time $$t$$ is a matrix containing information on the probability of transitioning between **states**.



### References

1. [Markov Chain by Brilliant Math](https://brilliant.org/wiki/markov-chains/)
2.
