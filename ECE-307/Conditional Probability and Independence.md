Conditional Probability one of the most important concepts in probability theory. The importance of this concept is twofold. 
1. we are often interested in calculating probabilities when some partial information concerning the result of the experiment is available
2. Conditional probabilities can often be used to compute the desired probabilities more easily
## 3.1 Conditional probability 
Let's define $P(E|F)$ as the probability of E occurring given F already occurred

##### The relationship between $P(E|F)$ and $P(EF)$ 
$P(E|F) = \frac{P(EF)}{P(F)}$ if $P(F) \neq 0$
To understand where the above equivalence came from:
- The key to understand the equation is to understand the difference between $P(EF)$ and $P(E|F)$
- $P(EF)$ = the likelihood of hitting $E \cap F$ over the entire sample space
- $P(E|F)$ = the likelihood of hitting $E \cap F$ over the $F$ space
- Notice that both probabilities describes the region $E \cap F$, but $P(EF) \neq P(E|F)$ because their sample space is different
So, to get $P(EF)$ from $P(E|F)$ we need to expand it's domain to cover all sample space
- Mathematically this is done by multiplying P(E|F) by the probability of getting F
$P(F)P(E|F) = P(EF)$ 

## 3.2 From the above definition, we can derive 3 Relations
1. Multiplication Rule
2. Total law of probability
3. Bayes' Theorem 


Multiplication rule
$P(E_1E_2E_3) = P(E_1)P(E_2|E_1)P(E_3|E_2E_1)...$
- This rule came from recursively apply conditional probability
- If events are independent, this rule degenerates to P(E1)P(E2)P(E3)...

Total Law of probability
$P(E) = P(F)P(E_1|F)+P(F)P(E_2|F)+...$ where $E_1, E_2, ...$ are partition of E
- This relation came from applying conditional probability to partition of an event
- This is useful in applications where P(E) is difficult to compute, but partitions of E with certain constrain are easier to get

Bayes' theorem
- applies conditional probability, multiplication laws, total law of probability together

## 3.3 Bayes' Theorem

## 3.4 Independent Events
if 2 events are independent, then the following equivalence hold 
$P(EF) = P(E)P(F)$
	$P(E|F) = P(E)$

For multiple events that are independent 
- P(every subset) is the P(product of that subset)

## 3.5 $P(.|F)$ is a probability
the conditional probability satisfy all the properties of ordinary probabilities