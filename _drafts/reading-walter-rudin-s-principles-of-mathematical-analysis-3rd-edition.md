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
