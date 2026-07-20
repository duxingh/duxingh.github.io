---
layout: post
title: Notes on Courant's "What Is Mathematics?"
category: Notes
tags: [mathematics]
media_subpath: /assets/img/posts/notes-on-courant-s-what-is-mathematics
image: cover.jpg
math: true
---
*What Is Mathematics?: An Elementary Approach to Ideas and Methods* by Richard Courant and Herbert Robbins was originally published in 1941, and was revised with contributions from Ian Stewart in 1996. It is a book exploring the ideas and ways of thinking behind the subject.

## Preface to the Second Edition

—by Ian Stewart

Ian Stewart says that this book aims to put the meaning back into mathematics. The meaning of mathematical objects doesn't depend on themselves but on the relationship between them:

> It doesn't matter what mathematical things *are*: it's what they *do* that counts.

---

Ian Stewart wrote a new chapter introducing recent developments for the second edition of this book, and he also introduced his book *From Here to Infinity* as a companion to it.

## Chapter I. The Natural Numbers

### &sect;1. Calculation with Integers

We can define natural numbers as a set with two operations—addition and multiplication—that satisfy some so-called arithmetic laws. In other words, natural numbers are just tokens obeying some game rules. If we change or extend the game rules, there will be some new "numbers".

### &sect;2. The Infinitude of the Number System. Mathematical Induction

The mathematical induction is accepted as an axiom. We can use it to prove some useful results.

---

The arithmetical progression:

$$
A_n := \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

Proof by induction: The formula obviously holds when $n = 1$. Now suppose it holds for a positive integer $n$, then we have

$$
A_{n+1} = A_n + (n+1) = \frac{n(n+1)}{2} + (n+1) = \frac{(n+1)(n+2)}{2}
$$

Thus, the formula holds for every positive integer $n$ by mathematical induction. $\square$

A hint for deriving the arithmetical progression:

$$
\begin{align*}
A_n &= 1 + 2 + \cdots + n \\
A_n &= n + (n-1) + \cdots + 1 \\
2A_n &= n(n+1)
\end{align*}
$$

---

The geometrical progression:

$$
G_n := \sum_{i=0}^{n} q^i = \frac{1-q^{n+1}}{1-q}
$$

where $q \neq 1$.

Proof by induction: The formula obviously holds when $n = 0$. Now suppose it holds for a natural number $n$, then we have

$$
G_{n+1} = G_n + q^{n+1} = \frac{1-q^{n+1}}{1-q} + q^{n+1} = \frac{1-q^{n+2}}{1-q}
$$

Thus, the formula holds for every natural number $n$ by mathematical induction. $\square$

A hint for deriving the geometrical progression:

$$
\begin{align*}
G_n &= 1 + q + \cdots + q^n \\
qG_n &= q + q^2 + \cdots + q^n + q^{n+1} \\
(1-q) G_n &= 1-q^{n+1}
\end{align*}
$$

---

The sum of the first $n$ squares:

$$
S_n := \sum_{i=1}^{n} i^2 = \frac{n(n+1)(2n+1)}{6}
$$

Proof by induction: The formula obviously holds when $n = 1$. Now suppose it holds for a positive integer $n$, then we have

$$
\begin{align*}
    S_{n+1} &= S_n + (n+1)^2 \\
            &= \frac{n(n+1)(2n+1)}{6} + (n+1)^2 \\
            &= \frac{(n+1)[n(2n+1)+6(n+1)]}{6} \\
            &= \frac{(n+1)(2n^2 + 7n + 6)}{6} \\
            &= \frac{(n+1)(n+2)(2n+3)}{6} \\
\end{align*}
$$

Thus, the formula holds for every positive integer $n$ by mathematical induction. $\square$

A hint for deriving this formula:

$$
\begin{align*}
    S_n = & 1 + \\
          & 2 + 2 + \\
          & 3 + 3 + 3 + \\
          & \cdots \\
          & n + n + n + \cdots + n\\
\end{align*}
$$

$$
\Downarrow
$$

$$
\begin{align*}
S_n &= A_n + (A_n - A_1) + (A_n - A_2) + \cdots + (A_n - A_{n-1}) \\
    &= n A_n - (A_1 + A_2 + \cdots + A_{n-1}) \\
    &= n A_n - \sum_{i=1}^{n-1} A_i \\
    &= n A_n - \sum_{i=1}^{n-1} \frac{i(i+1)}{2} \\
    &= n A_n - \frac{1}{2}\sum_{i=1}^{n-1} (i^2 + i) \\
    &= n A_n - \frac{1}{2} (S_{n-1} + A_{n-1}) \\
    &= n A_n - \frac{1}{2} (S_n - n^2 + A_{n} - n) \\
\end{align*}
$$

$$
\Downarrow
$$

$$
\begin{align*}
3 S_n &= (2n - 1) A_n + n^2 + n \\
    &= (2n - 1) \frac{n(n+1)}{2} + n(n+1) \\
    &= \frac{n(n+1)(2n+1)}{2} \\
\end{align*}
$$

---

The sum of the first $n$ cubes:

$$
C_n := \sum_{i=1}^{n} i^3 = [\frac{n(n+1)}{2}]^2
$$

Proof by induction: The formula obviously holds when $n = 1$. Now suppose it holds for a positive integer $n$, then we have

$$
\begin{align*}
    C_{n+1} &= C_n + (n+1)^3 \\
            &= [\frac{n(n+1)}{2}]^2 + (n+1)^3 \\
            &= \frac{(n+1)^2[n^2 + 4(n+1)]}{4} \\
            &= \frac{(n+1)^2(n+2)^2}{4} \\
            &= [\frac{(n+1)(n+2)}{2}]^2 \\
\end{align*}
$$

Thus, the formula holds for every positive integer $n$ by mathematical induction. $\square$

A hint for deriving this formula:

$$
\begin{align*}
    C_n = & 1^2 + \\
          & 2^2 + 2^2 + \\
          & 3^2 + 3^2 + 3^2 + \\
          & \cdots \\
          & n^2 + n^2 + n^2 + \cdots + n^2 \\
\end{align*}
$$

$$
\Downarrow
$$

$$
\begin{align*}
C_n &= S_n + (S_n - S_1) + (S_n - S_2) + \cdots + (S_n - S_{n-1}) \\
    &= n S_n - (S_1 + S_2 + \cdots + S_{n-1}) \\
    &= n S_n - \sum_{i=1}^{n-1} S_i \\
    &= n S_n - \sum_{i=1}^{n-1} \frac{i(i+1)(2i+1)}{6} \\
    &= n S_n - \frac{1}{6} \sum_{i=1}^{n-1} (2i^3 + 3i^2 + i) \\
    &= n S_n - \frac{1}{6} (2 C_n - 2 n^3 + 3S_n - 3 n^2 + A_n - n) \\
\end{align*}
$$

$$
\Downarrow
$$

$$
\begin{align*}
    8C_n &= (6n-3) S_n - A_n + 2n^3 + 3n^2 + n \\
         &= (6n-3) \frac{n(n+1)(2n+1)}{6} - \frac{n(n+1)}{2} + n(n+1)(2n+1) \\
         &= (2n-1) \frac{n(n+1)(2n+1)}{2} - \frac{n(n+1)}{2} + n(n+1)(2n+1) \\
         &= \frac{n(n+1)[(2n-1)(2n+1) - 1 + 2(2n+1)]}{2} \\
         &= \frac{n(n+1)(4n^2 + 4n)}{2} \\
         &= 2 n(n+1)(n^2 + n) \\
         &= 2 [n(n+1)]^2 \\
\end{align*}
$$

---

An important inequality:

$$
(1+p)^n \geq 1 + np
$$

where $p > -1$.

Proof by induction: We have $(1+p)^n = 1 + np$ when $n = 1$. Thus, this inequality holds for $n=1$. Now suppose it holds for a positive integer $n$, then we have

$$
(1+p)^{n+1} = (1+p)^n (1+p) \geq (1+np)(1+p) = 1 + (n+1)p + np^2 \geq 1 + (n+1)p
$$

Thus, this inequality holds for every positive integer $n$ by mathematical induction. $\square$

---

We can expand $(a+b)^n$ as

$$
\sum_{i=0}^{n} C_{i}^{n} a^{n-i}b^i
$$

where $C_0^n = C_n^n = 1$ and $C_i^n = C_i^{n-1} + C_{i-1}^{n-1}$. These $C_i^n$ form the so-called Pascal's Triangle.

The binomial theorem states that

$$
C_i^n = \frac{n!}{i!(n-i)!}
$$

Proof by induction: Obviously, this formula holds for $n=1$. Now suppose this formula holds for a positive integer $n$, then we have

$$
\begin{align*}
C_{i}^{n+1} &= C_i^{n} + C_{i-1}^{n} \\
            &= \frac{n!}{i!(n-i)!} + \frac{n!}{(i-1)!(n-i+1)!} \\
            &= \frac{(n+1-i) \cdot n!}{i!(n+1-i)!} + \frac{i \cdot n!}{i!(n+1-i)!} \\
            &= \frac{(n+1) \cdot n!}{i!(n+1-i)!} \\
            &= \frac{(n+1)!}{i!(n+1-i)!} \\
\end{align*}
$$

Thus, this formula holds for every positive integer $n$ by mathematical induction. $\square$

## Supplement to Chapter I. The Theory of Numbers

### &sect;1. The Prime Numbers

> There are infinitely many prime numbers.
{: .prompt-info }

Proof: Suppose there are only finite many primes $p_1, p_2, \cdots, p_n$, then we form a number

$$
A = p_1 p_2 \cdots p_n + 1
$$

$A$ is larger than any prime $p_i$; thus, $A$ must be a composite number, i.e., there is at least one $p_i$ that is a factor of $A$. However, we can see that $A$ divided by any $p_i$ always leaves a remainder of $1$. This contradiction proves that there are infinitely many primes. $\square$.

This proof was first given by Euclid.

---

The fundamental theorem of arithmetic:

> Every integer $N$ greater than $1$ can be factored into a product of primes in only one way.
{: .prompt-info }

Proof: Suppose there are integers that can be factored into a product of primes at least in two ways, then there is a smallest one

$$
m = p_1 p_2 \cdots p_r = q_1 q_2 \cdots q_s \tag{S1.1.1}
$$

where $p_i,q_i$ are primes, and $p_1 \leq p_2 \leq \cdots \leq p_r$, $q_1 \leq q_2 \leq \cdots \leq q_s$.

It's obvious that $p_1 \neq q_1$, otherwise we can delete them from (S1.1.1) to get a smaller integer that can be factored into a product of primes in two ways. Thus, we can assume $p_1 < q_1$.

We form an integer

$$
m' = m - p_1 q_2 q_3 \cdots q_s
$$

Thus, we have

$$
\begin{align*}
m' &= p_1 (p_2 p_3 \cdots p_r - q_2 q_3 \cdots q_s) \tag{S1.1.2} \\
m' &= (q_1 - p_1) q_2 q_3 \cdots q_s \tag{S1.1.3} \\
\end{align*}
$$

From (S1.1.2), we know that $p_1$ is a factor of $m'$.

Then we introduce a proposition: *If a prime $p$ is a factor of the product of two integers $ab$, it is a factor of either $a$ or $b$.*

By applying this proposition to (S1.1.3), we know that $p_1$ is a factor of either $q_1 - p_1$ or $q_2 q_3 \cdots q_s$. If $p_1$ is a factor of $q_2 q_3 \cdots q_s$, it means that $q_2 q_3 \cdots q_s$ can be decomposited into a different product of primes since $q_2 q_3 \cdots q_s$ doesn't contain $p_1$. Thus, $p_1$ is a factor of $q_1 - p_1$, i.e., there exists a positive integer $n$ such that

$$
q_1 - p_1 = n p_1 \Rightarrow q_1 = (n+1)p_1
$$

This is contradictory to that $q_1$ is a prime. This contradiction proves this theorem. $\square$

Now we back to consider the proposition mentioned above:

*If a prime $p$ is a factor of the product of two integers $ab$, it is a factor of either $a$ or $b$.*

Proof: In fact, it is a corollary of the fundamental theorem of arithmetic. If $p$ were a factor of neither $a$ nor $b$, it wouldn't be appeared in the unique prime decompositions of $a$ and $b$. Thus, $p$ wouldn't be appeared in the unique prime decomposition of $ab$. However, there exists an integer $t$ such that $ab = pt$ since $p$ is a factor of $ab$. If we decomposite $t$ into a product of primes, we could see that $p$ appears in the unique prime decomposition of $ab$. This contradiction proves this proposition. $\square$

How can we prove a theorem based on a proposition that is a corollary of the theorem? Is a circular logical reasoning? No. Actually, this proposition just need a condition that the prime decompositions of $a$ and $b$ are unique. In (S1.1.3), the prime decompositions of $q_1 - p_1$ and $q_2 q_3 \cdots q_s$ are unique since both of them are smaller than $m$.

---

Fermat made a conjecture that all numbers of the form

$$
F(n) = 2^{2^n} + 1
$$

are primes.

For $n=1,2,3,4$, $F(n)$ is prime. But in 1732, Euler discovered that

$$
F(5) = 641 \cdot 6700417
$$

---

Lejeune Dirichlet (1805–1859) proved that there are infinite many primes in any arithmetical progression $a+nd$ where $a$ and $d$ have no common factors. His proof applies the most advanced tools of calculus and function theory, and it's difficult to grasp.

However, the authors showed us the proof of two special cases $4n+3$ and $6n+5$. The method is a generalization of Euclid's proof of the inifinitude of primes.

Proof of $4n+3$: Suppose there are only finite many primes $p_1, p_2, \cdots, p_r$ of the form $4n+3$. We construct an integer

$$
A = 4 p_1 p_2 \cdots p_r - 1 = 4(p_1 p_2 \cdots p_r - 1) + 3
$$

$A$ is the form of $4n+3$.

We notice that any primes greater than $2$ is the form of either $4n+1$ or $4n+3$, and the product of any two integers of the form $4n+1$ is still the form of $4n+1$. Thus, $A$ contains at least one prime factor of the form $4n+3$. However, we can see that $A$ divided by any $p_i$ leaves a remainder $-1$. Thus, there exists a prime factor of the form $4n+3$ that is greater than any $p_i$. This is contradictory to the assumption. $\square$

Proof of $6n+5$: Suppose there are only finite many primes $p_1, p_2, \cdots, p_r$ of the form $6n+5$. We construct an integer

$$
A = 6 p_1 p_2 \cdots p_r - 1 = 6(p_1 p_2 \cdots p_r - 1) + 5
$$

$A$ is the form of $6n+5$.

We notice that any primes greater than $3$ is the form of either $6n+1$ or $6n+5$, and the product of any two integers of the form $6n+1$ is still the form of $6n+1$. Thus, $A$ contains at least one prime factor of the form $6n+5$. However, we can see that $A$ divided by any $p_i$ leaves a remainder $-1$. Thus, there exists a prime factor of the form $6n+5$ that is greater than any $p_i$. This is contradictory to the assumption. $\square$

We can't continue this proof pattern for the case of $8n+7$ because any prime greater than $5$ has four possible forms $8n+1$, $8n+3$, $8n+5$ and $8n+7$.

---

Let $A_n$ be the number of primes among integers $1,2,\cdots,n$. Gauss made a conjecture that

$$
\frac{A_n}{n} \sim \frac{1}{\ln n}
$$

It means

$$
\lim_{n \to \infty} \frac{A_n \ln n}{n}  = 1
$$

Hadamard and Poussin independently gave a rigorous proof of this so-called prime number theorem in 1896.

### &sect;2. Congruences
