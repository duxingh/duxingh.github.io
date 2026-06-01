---
layout: post
title: Reading Walter Rudin's "Principles of Mathematical Analysis, 3rd Edition"
category: Notes
tags: [mathematics, analysis]
media_subpath: /assets/img/posts/reading-walter-rudin-s-principles-of-mathematical-analysis-3rd-edition
image: cover.jpg
math: true
---
Walter Rudin's *Principles of Mathematical Analysis* was originally published in 1953. It is known as Baby Rudin.

## Chapter 1. The Real and Complex Number Systems

### Ordered Sets

> <strong id="def-1-5">1.5 Definition</strong> &emsp; Let $S$ be a set. An *order* on $S$ is a relation, denoted by $<$, with the following properties:
>
> (i) If $x \in S$ and $y \in S$ then one and only one of the statements:  
>
> $$
> x < y, x = y, y > x
> $$
>
> is true.
>
> (ii) If $x, y, z \in S$, if $x < y$ and $y < z$, then $x < z$.
{: .prompt-info }

The set of rational numbers is an ordered set if we define that $x < y$ is equivalent to that $y-x$ being positive.

> <strong id="def-1-10">1.10 Definition</strong> &emsp; An ordered set $S$ is said to have the *least-upper-bound property* if the following is true:
>
> If $E \subset S$, $E$ is not empty, and $E$ is bounded above, then $\sup E$ exists in $S$.
{: .prompt-info }

The set of rational numbers doesn't have this property.

> <strong id="theorem-1-11">1.11 Theorem</strong> &emsp; Suppose $S$ is an ordered set with the least-upper-bound property, $B \subset S$, $B$ is not empty, and $B$ is bounded below. Let $L$ be the set of all lower bounds of $B$. Then
>
> $$
> \alpha = \sup L
> $$
>
> exists in $S$, and $\alpha = \inf B$.
>
> In particular, $\inf B$ exists in $S$.
{: .prompt-info }

In other words, an ordered set with the least-upper-bound property also has a greatest-lower-bound property. This fact is obvious according to the symmetry of an ordered set.

Proof: Because $L$ is the set of all lower bounds of $B$, every member of $B$ is an upper bound of $L$. $\alpha = \sup L$ exists in $S$ since $S$ has a least-upper-bound property.

We have $\alpha \leq b$ for every $b \in B$ since $b$ is an upper bound of $L$ and $\alpha$ is the least upper bound of $L$. Thus, $\alpha$ is an lower bound of $B$. We have $l \leq \alpha$ for every $l \in L$ since $\alpha$ is an upper bound of $L$. Thus, $\alpha$ is the largest one of the lower bounds of $B$, i.e., $\alpha$ is the greatest lower bound of $B$. $\square$

### Fields

> <strong id="def-1-12">1.12 Definition</strong> &emsp; A *field* is a set $F$ with two operations, called *addition* and *multiplication*, which satisfy the following so-called "field axioms" (A), (M), and (D):
>
> **(A) Axioms for addition**
>
> (A1) If $x \in F$ and $y \in F$, then their sum $x + y$ is in $F$.  
> (A2) Addition is commutative: $x + y = y + x$ for all $x, y \in F$.  
> (A3) Addition is associative: $(x + y) + z = x + (y + z)$ for all $x, y, z \in F$.  
> (A4) $F$ contains an element $0$ such that $0 + x = x$ for every $x \in F$.  
> (A5) To every $x \in F$ corresponds an element $-x \in F$ such that
>
> $$
> x+(-x) = 0
> $$
>
> **(M) Axioms for multiplication**
>
> (M1) If $x \in F$ and $y \in F$, then their product $xy$ is in $F$.  
> (M2) Multiplication is commutative: $xy = yx$ for all $x, y \in F$.  
> (M3) Multiplication is associative: $(xy)z = x(yz)$ for all $x, y, z \in F$.  
> (M4) $F$ contains an element $1 \neq 0$: $0$ such that $1x = x$ for every $x \in F$.  
> (M5) If $x \in F$ and $x \neq 0$ then there exists an element $1/x \in F$ such that
>
> $$
> x \cdot (1/x) = 1
> $$
>
> **(D) The distributive law**
>
> $$
> x(y + z) = xy + xz
> $$
>
> holds for all $x,y,z \in F$.
{: .prompt-info }

The rational number set $\mathbf{Q}$ is a field.

> <strong id="proposition-1-14">1.14 Proposition</strong> &emsp; The axioms for addition imply the following statements.
>
> (a) If $x + y = x + z$ then $y = z$.  
> (b) If $x + y = x$ then $y = 0$.  
> (c) If $x + y = 0$ then $y = -x$.  
> (d) $-(-x) = x$.
{: .prompt-info }

(a) is a cancellation law; (b) asserts that the addition unit is unique; (c) asserts that an addition inverse is unique.

Proof: If $x + y = x + z$ holds, by axioms (A), we have

$$
\begin{gather*}
(-x) + (x + y) = (-x) + (x + z) \\
\Downarrow \\
((-x)+x) + y = ((-x)+x) + z \\
\Downarrow \\
(x+(-x)) + y = (x+(-x)) + z \\
\Downarrow \\
0 + y = 0 + z \\
\Downarrow \\
y = z
\end{gather*}
$$

This proves (a). Take $z = 0$ in (a) to obtain (b). Take $z = -x$ in (a) to obtain (c).

Since $-x + x = 0$, by (c), we have $x = -(-x)$. This proves (d). $\square$

> <strong id="proposition-1-15">1.15 Proposition</strong> &emsp; The axioms for multiplication imply the following statements.
>
> (a) If $x \neq 0$ and $xy = xz$ then $y = z$.  
> (b) If $x \neq 0$ and $xy = x$ then $y = 1$.  
> (c) If $x \neq 0$ and $xy = 1$ then $y = 1/x$.  
> (d) If $x \neq 0$ then $1/(1/x) = x$.  
{: .prompt-info }

The proof is similar to that of Proposition 1.14.

> <strong id="proposition-1-16">1.16 Proposition</strong> &emsp; The field axioms imply the following statements, for any $x, y, z \in F$.
>
> (a) $0x = 0$.  
> (b) If $x \neq 0$ and $y \neq 0$ then $xy \neq 0$.  
> (c) $(-x)y = -(xy) = x(-y)$.  
> (d) $(-x)(-y) = xy$.
{: .prompt-info }

Proof: Since $x + 0x = 1x + 0x = (1+0)x = 1x = x$, by Proposition 1.14 (b), we have $0x = 0$. (a) holds.

Assume $xy = 0$, then $x = x + 0 = x + xy = x(1+y)$; by Proposition 1.15 (b), we have $1+y = 1$. Thus, $y = 0$. Similarly, we can show that $x = 0$. This is contradictory to $x \neq 0$ and $y \neq 0$. This proves (b).

Since

$$
xy + (-x)y = (x + (-x)) y = 0y = 0
$$

we have $(-x)y = -(xy)$. Similarly, we can show that $x(-y) = -(xy)$. (c) holds.

Since

$$
-(xy) + (-x)(-y) = (-x)y + (-x)(-y) = (-x)(y + (-y)) = (-x) 0 = 0
$$

we have $(-x)(-y) = -(-(xy)) = xy$. (d) holds. $\square$

Proposition 1.16 (a) shows why it asserts $1 \neq 0$ in (M4). If $1 = 0$, we have $1x = 0x = 0 = 1$ for any $x \in F$. It means that there is only one element in $F$. It's a boring set.

> <strong id="def-1-17">1.17 Definition</strong> &emsp; An *ordered field* is a *field* $F$ which is also an *ordered set*, such that
>
> (i) $x+y < x+z$ if $x,y,z \in F$ and $y < z$,  
> (ii) $xy > 0$ if $x \in F$, $y \in F$, $x > 0$, and $y > 0$.
{: .prompt-info }

The rational number set is an ordered field.

> <strong id="proposition-1-18">1.18 Proposition</strong> &emsp; The following statements are true in every ordered field.
>
> (a) If $x > 0$ then $-x < 0$, and vice versa.  
> (b) If $x > 0$ and $y < z$ then $xy < xz$.  
> (c) If $x < 0$ and $y < z$ then $xy > xz$.  
> (d) If $x \neq 0$ then $x^2 > 0$. In particular, $1 > 0$.  
> (e) If $0 < x < y$ then $0 < 1/y < 1/x$.  
{: .prompt-info }

Proof: (a) Suppose $x > 0$. Since Definition 1.5 (i), we just need to prove that neither $-x = 0$ nor $-x > 0$. If $-x = 0$ then $x = 0$; it's contradictory to $x > 0$. If $-x > 0$ then $x + (-x) > x + 0$ since Definition 1.17 (i). It implies that $0 > x$; it's contradictory to $x > 0$. Thus, $-x < 0$.

(b) $y < z$ implies that $0 < -y + z$ since Definition 1.17 (i). By Definition 1.17 (ii), we have $x(-y+z) > 0$. It implies that $-xy + xz > 0$, which implies that $xz > xy$.

(c) Since $x < 0$, we have $-x > 0$ by (a). We have $(-x)y < (-x)z$ since (b). It implies that $-xy < -xz$. By adding $xy$ to both sides, we have $0 < xy + (-xz)$. By adding $xz$ to both sides, we have $xz < xy$.

(d) Since $x \neq 0$, we have $x > 0$ or $x < 0$. If $x > 0$, we have $x^2 > 0$ since Definition 1.17 (ii). If $x < 0$, we have $-x > 0$ since (a). Thus, $(-x)(-x) > 0$ since Definition 1.17 (ii). By Proposition 1.16 (d), we have $x^2 = (-x)(-x) > 0$. In particuler, we have $1 > 0$ since $1^2 = 1$.

(e) If $x > 0$ and $1/x < 0$, we have $1 = x (1/x) < 0$ since (b), but this result is contradictory to (d). Thus, $1/x > 0$. Similarly, we can show that $y > 0$ implies $1/y > 0$. If $x < y$, by multiplying $1/x$ to both sides, we get $1 < y (1/x)$; again, by multiplying $1/y$ to both sides, we get $1/y < 1/x$. $\square$

### The Real Field

> <strong id="theorem-1-19">1.19 Theorem</strong> &emsp; There exists an ordered field $\mathbf{R}$ which has the least-upper-bound property.
>
> Moreover, $\mathbf{R}$ contains $\mathbf{Q}$ as a subfield.
{: .prompt-info }

To prove this theorem, we need to construct $\mathbf{R}$ based on $\mathbf{Q}$. The author puts this tedious work into the Appendix to chapter 1.

> <strong id="theorem-1-20">1.20 Theorem</strong> &emsp; (a) If $x \in \mathbf{R}$, $y \in \mathbf{R}$, and $x > 0$, then there is a positive integer $n$ such that
>
> $$
> nx > y
> $$
>
> (b) If $x \in \mathbf{R}$, $y \in \mathbf{R}$, and $x < y$, then there exists a $p \in \mathbf{Q}$ such that $x < p < y$.
{: .prompt-info }

(a) is called the *archimedean property* of $\mathbf{R}$. In many other books, this is accepted as an axiom. (b) means rational numbers are dense in the real field.

Proof: (a) Let $S$ be a set of all $nx$, and suppose that $nx \leq y$ holds for every positive integer $n$. Then $S$ is upper bounded. By the least-upper-bound property, there exists $z \in \mathbf{R}$ that is the least upper bound of $S$.

By $x > 0$, we have $-x < 0$. By adding $z$ into the both sides, we have $z-x < z$, so that $z-x$ is not an upper bound of $S$. Thus, there exists an $nx$ such that $z-x < nx$. By adding $x$ into the both sides, we have $z < (n+1)x$. This is contradictory to the fact that $z$ is an upper bound of $S$ since $(n+1)x \in S$.

This proves that there exists an $nx$ such that $nx > y$.

(b) We have $y-x > 0$ since $x < y$. To find out a rational number $p$ between $x$ and $y$, we need to compare $x$ and $y$ to the unit length $1$. By (a), we know that there exists a positive integer $n$ such that $n(y-x) > 1$, i.e.,

$$
nx < ny - 1
$$

Again, by (a), there exists positive integers $m_1$ and $m_2$ such that $m_1 > nx$ and $m_2 > -nx$, i.e.,

$$
-m_2 < nx < m_1
$$

There is an integer $m$ such that

$$
m-1 \leq nx < m
$$

$nx < m$ implies $x < m/n$.

$m-1 \leq nx$ and $nx < ny-1$ imply

$$
m-1 \leq nx < ny -1
$$

Thus, $m/n < y$. Letting $p = m/n$, (b) is proved. $\square$

> <strong id="theorem-1-21">1.21 Theorem</strong> &emsp; For every real $x > 0$ and every integer $n > 0$ there is one
and only one positive real $y$ such that $y^n = x$.
{: .prompt-info }

Proof: If $x \geq 1$, let $S$ be a set of all positive real numbers $s$ satisfying $s^n < x$, then $S$ is upper bounded. There exists a least-upper bound $y$ of $S$. One and only one of the below three statements is true:

$$
y^n < x, y^n = x, y^n > x
$$

If $y^n < x$, $y \in S$. Thus, $y$ is the largest member of $S$. By Theorem 1.20 (b), we can choose a rational number $p$ such that $y^n < p < x$.
