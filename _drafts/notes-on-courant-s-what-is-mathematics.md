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

### Introduction
