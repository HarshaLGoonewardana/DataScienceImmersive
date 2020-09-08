**1.05: Discrete Distributions**

**LEARNING OBJECTIVES**
- Define distribution and random variable.
- Describe the difference between discrete and continuous random variables.
- Understand the difference between probability mass functions and cumulative density functions.
- Give examples of the following distributions: Discrete Uniform, Bernoulli, Binomial, and Poisson.

**Data Science Preliminaries:**

The data science process is **non-linear**. Different problems will require different approaches, which means there’s not just one set of steps we can follow in any scenario.

**Defining the problem, gathering data, and performing EDA** are most of the process. **Modeling and evaluating the model** won’t be what most of your time is spent on. **Answering the problem** means translating your data science analysis into real-world suggestions.

**Random Variables and Distributions:**

A **distribution** is the set of all values of a variable and how frequently we observe each of those values. Distributions can be summarized using measures of center, spread, and shape.

An **experiment** is an  infinitely repeatable procedure with well-defined outcomes.

The **sample space** is the set of all possible outcomes of the experiment.

A **random variable** is any function that maps the sample space to the real number line. 

In the example of flipping a coin, the **experiment** is the procedure of flipping a coin. If the coin is flipped twice, the sample space is S = {{H, H}, {H, T}, {T, H}, {T, T}}. The random variable might be **number of heads** -- 0, 1, or 2. We’ve converted the outcome to a **number on the real number line**. Note: the random variable could also be: how often we observe consecutive tails. The sample space can be mapped to the real number line in different ways.

If all of the items can be listed, the sample space is considered **discrete**.

If we cannot list out all of the items, the sample space is **continuous**.

**Discrete random variables** have sample spaces which can be considered “countable.” Some examples are: the number of spades drawn from a deck of cards; the number rolled on a die; the number of people in a room whose birthdays are in January.

This isn’t the case for **continuous variables** -- in a continuous sample space, the number of items in the sample space is uncountable. Some examples are: how much sleep someone got, the weight of a shipping container, likelihood of voting.

We can describe the distribution of discrete random variables using a **probability mass function (pmf)**.

The **discrete uniform distribution** is used when we have a set of **equally likely discrete outcomes**.

The **cumulative distribution function** (cdf) plots the cumulative probability of our outcomes. It starts at the minimum possible outcome and adds the probability of each outcome; each point on the CDF represents the probability that a random variable is less than or equal to that value.

The **Bernoulli distribution** gives likelihood of success in a trial given a constant probability of success for every trial.

The **binomial distribution** gives **the sum of successes of a Bernoulli distributed random variable**. For example, if a coin is flipped a certain number of times with a certain probability of landing on heads, what is the probability of getting a certain number of heads?

**Continuous Probability Distributions**

**LEARNING OBJECTIVES**:
 - Give examples of the following distributions: Continuous Uniform, Exponential, Normal.
- Apply the 68-95-99.7 Rule.
- Calculate and interpret z-scores.
- Describe why the Normal distribution is seen everywhere.
- State the Central Limit Theorem.

A *continuous uniform distribution* is where, within a certain range, any value is equally likely to be chosen. It is defined by its lower-bound, a, and upper-bound, b.
> Check for understanding: Which discrete distribution is this similar to? Why is it different?

The **exponential distribution** models the amount of time until one success. It is **parameterized** by lambda, the rate of event occurrences. Because the exponential distribution models time, it clearly must be a continuous distribution.

> What does it mean for a distribution to be _paramterized_ by a value? Put most simply, distribution’s parameter changes how the distribution is shaped. 

**Note**: When plotting probabilities for continuous distributions, we use a **probability density function** (pdf) (_not_ a pmf.)

The **normal distribution** is parameterized by its mean and standard deviation and has some particular properties that make it extremely useful. In a population described by a normal distribution, 68% of observations from the population will fall within one standard deviation of the mean. 95% of observations from the population will fall between two standard deviations from the mean, and 99.7% will fall within three standard deviations from the mean. This is known as **the 68-95-99.7 Rule**.

A **Z-score** is a generalized measure of how many standard deviations an observation is away from the mean. It is given by dividing the difference between the observation and the population mean by the standard deviation.
> Check for understanding: What does a very large Z-score indicate? What about a very small Z-score?

**1.07: Central Limit Theorem**

**LEARNING OBJECTIVES**:
•Define and describe sampling distribution.
•Define, describe and compute standard error of the mean.
•Describe the Central Limit Theorem.

A sample **statistic** is a random but known variable. A population **parameter** is a constant but unknown. By taking a sample from a population, we can use a sample statistic to make inferences about the population parameter.

The **sample mean** is the mean of a sample taken from a population.

If we take **every possible sample** of size n and plot their respective sample means on a histogram, we get the **sampling distribution of the sample mean**.

This is important because **the sampling distribution of the sample mean is approximately normally distributed**, even when the distribution of the population is not.

