---
layout: post
title: Notes on "Introduction to Calculus and Analysis, Vol. 1"
category: Notes
tags: [mathematics, analysis, calculus]
media_subpath: /assets/img/posts/notes-on-introduction-to-calculus-and-analysis-vol-1
image: cover.jpg
math: true
---
*Introduction to Calculus and Analysis* by Richard Courant and Fritz John is a classic, two-volume textbook known for its rigorous yet intuitive approach, bridging the gap between elementary calculus and higher mathematics. Volume 1 focuses on single-variable calculus.

## Chapter 1. Introduction

### 1.1 The Continuum of Numbers

The natural numbers do not suffice to describe quantities that can change continuously. Thus, we need to extend them to a new number system called the real numbers (the continuum of numbers).

#### a. The System of Natural Numbers and Its Extension. Counting and Measuring

We establish addition and multiplication on the natural number system, and these arithmetic operations obey some basic laws. To make these operations always possible and these laws still work, we extend the natural number system by introducing zero, negative integers, and fractions. Finally, we obtain a rational number system.

The rational number system is dense, that is, there are infinitely many rational numbers between any two rational numbers. However, this property still does not make rational numbers sufficient to describe continuous quantities. For example, the length of the diagonal of a square with sides of unit length is not a rational number.

Without rigorously constructing a real number system, we can use an intuitive approach to extend the rational number system. After selecting a zero point and a unit length on a line, we can mark every rational number at a specific point on the line; those points that cannot be marked by a rational number are called irrational points. Now we just assume that every irrational point corresponds to a specific irrational number; both irrational and rational numbers obey the same arithmetic laws.

#### b. Real Numbers and Nested Intervals

Although we cannot represent an irrational point with a rational number, we can approach it with a sequence of nested intervals with rational endpoints; the error—the length of the interval—is successively smaller. The converse statement is not so obvious; therefore, it should be accepted as an axiom:

> If $I_1, I_2, I_3, \cdots$ form a nested sequence of intervals with rational endpoints, there is a point $x$ contained in all $I_n$.
{: .prompt-info }

#### e. Inequalities

Inequalities in mathematical analysis play important roles. Thus, the authors mention some important inequalities here.

Triangle inequality:

$$
|a+b| \leq |a| + |b|
$$

By replacing $a = \alpha - \gamma$ and $b = \gamma - \beta$, we have

$$
|\alpha - \beta| \leq |\alpha - \gamma| + |\gamma - \beta|
$$

The geometrical interpretation of this inequality is that the direct distance from $\alpha$ to $\beta$ is less than or equal to the sum of distances via a third point $\gamma$.

The Cauchy-Schwarz inequality:

$$
(\sum_{i=1}^{n} a_i b_i)^2 \leq (\sum_{i=1}^{n} a_i^2)(\sum_{i=1}^{n} b_i^2)
$$

Proof: We have $(a_i x + b_i)^2 \geq 0$ for every $a_i,b_i$ and real number $x$. Thus, we have

$$
\begin{gather*}
\sum_{i=1}^{n} (a_i x + b_i)^2 \geq 0 \\
\Downarrow \\
(\sum_{i=1}^{n} a_i^2) x^2 + 2(\sum_{i=1}^{n} a_i b_i) x+ (\sum_{i=1}^{n} b_i^2) \geq 0
\end{gather*}
$$

Let $A = \sum_{i=1}^{n} a_i^2$, $B = \sum_{i=1}^{n} b_i^2$, and $C = \sum_{i=1}^{n} a_i b_i$, we have

$$
A x^2 + 2 C x + B \geq 0
$$

The necessary condition for this inequality to hold for any real number $x$ is that $C^2 - AB \leq 0$. We can get the Cauchy-Schwarz inequality by expanding it. $\square$

In the special case $n = 2$ and

$$
a_1 = \sqrt{x}, a_2 = \sqrt{y}, b_1 = \sqrt{y}, b_2 = \sqrt{x}
$$

the Cauchy-Schwarz inequality becomes to

$$
\begin{gather*}
(2\sqrt{xy})^2 \leq (x+y)(x+y) \\
\Downarrow \\
\sqrt{xy} \leq \frac{x+y}{2}
\end{gather*}
$$

This inequality states that the geometric mean $\sqrt{xy}$ of two positive numbers $x,y$ never exceeds their arithmetic mean $(x+y)/2$.

![Figure 1.6](fig-1-6.jpg){: w="400" }

### 1.2 The Concept of Function
