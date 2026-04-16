## Probability Space and Measure Theory Basics

We begin with the definition of a probability space, which is a triple

$$
(\Omega, \mathcal{F}, P)
$$

where $\Omega$ is the sample space, $\mathcal{F}$ is a collection of events, and $P: \mathcal{F} \to [0,1]$ is a function assigning probabilities to those events. We assume that $\mathcal{F}$ is a $\sigma$-algebra.

### $\sigma$-algebra

A $\sigma$-algebra over $\Omega$ is a non-empty collection $\mathcal{F}$ of subsets of $\Omega$ such that if $A \in \mathcal{F}$ then $A^c \in \mathcal{F}$, and if $(A_i)*{i \in \mathbb{N}} \subset \mathcal{F}$ then

$$
\bigcup*{i=1}^{\infty} A_i \in \mathcal{F}.
$$

Using De Morgan’s laws,

$$
\bigcap_{i} A_i = \left( \bigcup_i A_i^c \right)^c,
$$

so a $\sigma$-algebra is also closed under countable intersections. Here “countable” means finite or countably infinite, that is, at most the size of $\mathbb{N}$.

### Measure space

Without the function $P$, the pair $(\Omega, \mathcal{F})$ is called a measure space.

### Measure

A measure is a function

$$
\mu: \mathcal{F} \to [0, \infty]
$$

such that $\mu(\emptyset) = 0$ and for any countable collection of pairwise disjoint sets $(A_i)$ one has

$$
\mu\left( \bigcup_{i=1}^{\infty} A_i \right) = \sum_{i=1}^{\infty} \mu(A_i).
$$

If $\mu(\Omega) = 1$, then $\mu$ is called a probability measure and is usually denoted by $P$.

### Finite additivity

Let $\mu: \mathcal{C} \to \overline{\mathbb{R}} = \mathbb{R} \cup {\pm\infty}$. We say that $\mu$ is finitely additive if $\mu(\emptyset) = 0$ and for any finite collection of pairwise disjoint sets $A_1, \dots, A_n$,

$$
\mu\left( \bigcup_{i=1}^n A_i \right) = \sum_{i=1}^n \mu(A_i).
$$

### Basic properties of measures

Let $\mu$ be a measure on $(\Omega, \mathcal{F})$. If $A \subset B$, then $\mu(A) \leq \mu(B)$. If $A \subset \bigcup_{m} A_m$, then

$$
\mu(A) \leq \sum_{m=1}^{\infty} \mu(A_m).
$$

If $A_1 \subset A_2 \subset \cdots$ and $\bigcup_i A_i = A$, then

$$
\mu(A_i) \uparrow \mu(A).
$$

If $A_1 \supset A_2 \supset \cdots$ and $\bigcap_i A_i = A$, with $\mu(A_1) < \infty$, then

$$
\mu(A_i) \downarrow \mu(A).
$$

### Sketch of proof of monotonicity

Let $B - A = B \cap A^c$. Then $B = A \cup (B - A)$ as a disjoint union, so

$$
\mu(B) = \mu(A) + \mu(B - A) \geq \mu(A).
$$

### Discrete probability space

Let $\Omega$ be countable and let $\mathcal{F}$ be the collection of all subsets of $\Omega$. Define

$$
P(A) = \sum_{\omega \in A} P(\omega),
$$

where $P(\omega) \geq 0$ and $\sum_{\omega \in \Omega} P(\omega) = 1$.
