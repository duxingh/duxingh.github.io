---
layout: post
title: Notes on "The Feynman Lectures on Physics, Volume I"
category: Notes
tags: [physics]
media_subpath: /assets/img/posts/notes-on-the-feynman-lectures-on-physics-volume-i
image: cover.jpeg
math: true
---
[*The Feynman Lectures on Physics*](https://www.feynmanlectures.caltech.edu/) is a classic, three-volume physics textbook based on lectures given by Nobel laureate Richard Feynman at Caltech from 1961–1964, with co-authors Robert B. Leighton and Matthew Sands. Known for their clarity and deep insight, the books cover fundamental physics from mechanics to quantum mechanics, remaining a definitive introduction to the subject for students and enthusiasts alike. The set is often sold with [*Feynman's Tips on Physics*](https://www.feynmanlectures.caltech.edu/TIPS_toc.html), a problem-solving supplement.

## Chapter 4. Conservation of Energy

### 4–1 What is energy?

> The law is called the *conservation of energy*. It states that there is a certain quantity, which we call energy, that does not change in the manifold changes which nature undergoes.

Obviously, this law is not obtained through direct experience with nature. It is summarized from many other laws, and finally, we set it as a basic principle.

### 4–2 Gravitational potential energy

> Conservation of energy can be understood only if we have the formula for all of its forms. I wish to discuss the formula for gravitational energy near the surface of the Earth, and I wish to derive this formula in a way which has nothing to do with history but is simply a line of reasoning invented for this particular lecture to give you an illustration of the remarkable fact that a great deal about nature can be extracted from a few facts and close reasoning. It is an illustration of the kind of work theoretical physicists become involved in. It is patterned after a most excellent argument by Mr. Carnot on the efficiency of steam engines.

The reasoning Feynman gives us here is a good example of a physicist's work. Doing physics is not doing mathematics; a physicist does not necessary to reason from the most basic principle of a well-built theoretical framework.

Here is Feynman's reasoning:

First, let's define a weight-lifting machine, which is a machine lifting a weight by lowering another weight. A level or a pulley is an example.

Then we mention a principle we summarize from the real-world experience: **there is no perpetual motion.** A perpetual-motion weight-lifting machine is a machine that, after a process, if the machine is restored to the original state, the net result is to have lifted a weight, so that we can use the lifted weight to run another machine.

Next, we define a reversible weight-lifting machine. If a machine lifts a weight $W$ by lowering a weight $V$, and it also lifts $V$ by lowering $W$, it is a reversible weight-lifting machine. There are no reversible weight-lifting machines in the real world, but idealization is a good way to reason in physics.

We can prove that a reversible weight-lifting machine is the most efficient. Suppose A is a weight-lifting machine that lifts a weight $W$ a distance $Y$ by lowering a unit weight a unit distance, and B is a *reversible* weight-lifting machine that lifts a weight $W$ a distance $X$ by lowering a unit weight a unit distance. If we can show that $X \geq Y$, we prove that a reversible machine is the most efficient. Now, suppose $Y > X$. We run the machine A forwards, then lower $W$ from $Y$ to $X$ to run another machine. Then we run the machine B backwards to restore the system to the original state. The net result is to lift $W$ a distance $Y - X$; this is contradictory to the principle that there is no perpetual motion. Thus, $X \geq Y$.

The next step is to calculate the exact value of $X$. For simplification, we can suppose $W$ equals three unit weights. Then Feynman builds a reversible weight-lifting machine like this:

![Figure 4-2](fig-4-2.jpeg)

If we run this machine forwards, we can see that $3X \leq 1$, otherwise, we can lower the unit ball from $3X$ to $1$ so that to restore the machine to the original state, but obtain a perpetual motion. Similarly, if we run the machine backwards, we have $1 \leq 3X$. Thus, $3X = 1$, i.e. $X = 1/3$.

We call the multiplication of the weight and its height its *gravitational potential energy*. From the above discussion, we can conclude that, in a reversible weight-lifting machine, the whole gravitational potential energy is conservative.

Feynman gives us some examples of applying this law.

![Figure 4-3](fig-4-3.jpeg){: w="300" }

We want to know how heavy $W$ must be to balance the system. If it is balanced, obviously, it is a reversible weight-lifting machine. Thus, the gravitational potential energy of (a) must be equal to that of (b).

$$
W \times 3 = W \times (-2) + 1 \times 3 \Rightarrow W = \frac{3}{5}
$$

![Figure 4-6](fig-4-6.jpeg){: w="300" }

We want to know how heavy $W$ must be to balance the system. If it is balanced, obviously, it is a reversible weight-lifting machine. Actually, we can't move $W$ up and down, but we can imagine doing that. This approach is called the principle of virtual work, because in order to apply this argument we have to imagine that the structure moves a little—even though it is not really moving or even movable. Now, suppose we pull $W$ down a unit distance, then the middle point of the rod moves up $1/2$, and the quarter point moves up $1/4$. The gravitational potential energy is conservative, thus, we have

$$
0 = W \times (-1) + 60 \times \frac{1}{2} + 100 \times \frac{1}{4} \Rightarrow W = 55
$$

## Chapter 5. Time and Distance

### 5–2 Time

> What really matters anyway is not how we *define* time, but how we measure it.

Time is the most basic concept, so we can't define it based on other more basic concepts.

---

> One way of measuring time is to utilize something which happens over and over again in a regular fashion—something which is *periodic*.

How can we know that a periodic event is regular? We can't, but we can assume that it is regular. If we have two periodic events, we can always use one to measure the other one, and then we pick the one that seems more regular as the standard.

### 5–3 Short times

> What about still smaller times? Does “time” exist on a still smaller scale? Does it make any sense to speak of smaller times if we cannot measure—or perhaps even think sensibly about—something which happens in a shorter time?

By the very definition of time, it is very hard to speak to the meaning of time in an extremely short duration when nothing happens. Can we really say that time is continuous? Maybe time is also quantumized.

## Chapter 6. Probability

### 6–3 The random walk

Consider a particle that can walk randomly forward and backward in each unit time, and the distance in each step is the same. Let $N$ be the number of steps and $D_N$ be the distance at the $N$ step. Obviously, the expected distance $\left< D_N \right>$ is zero. However, we are more interested in how far the particle has moved in $N$ steps, i.e., we want to calculate $\left< D_N^2 \right>$.

If we know $D_{N-1}$, we have $D_N = D_{N-1} + 1$ or $D_N = D_{N-1} - 1$. Thus, we have

$$
D_N^2 = \begin{cases}
    D_{N-1}^2 + 2D_{N-1} + 1 \\
    D_{N-1}^2 - 2D_{N-1} + 1 \\
\end{cases}
$$

Thus, we have $\left< D_N^2 \right> = \left< D_{N-1}^2 \right> + 1$. The solution is $\left< D_N^2 \right> = N$. We define the root-mean-square distance

$$
D_{rms} = \sqrt{\left< D_N^2 \right>} = \sqrt{N}
$$

It can be a measure of the “progress made away from the origin” in a random walk.

---

The random walk is related to the game of tossing a coin. If we imagine that the direction of each step is decided by the the appearance of head or tail in a coin toss, we have

$$
\begin{gather*}
D_N = N_H - N_T = 2N_H - N \\
\Downarrow \\
N_H - \frac{N}{2} = \frac{D_N}{2}
\end{gather*}
$$

$N_H - N/2$ is the *fluctuation*. Its rms value is

$$
(N_H - \frac{N}{2})_{rms} = \frac{\sqrt{N}}{2}
$$

The larger the $N$, the larger the rms fluctuation. However, if we consider the relative rms fluctuation:

$$
(N_H - \frac{N}{2})_{rms} / N = \frac{1}{2\sqrt{N}}
$$

It's tendency to zero.

Now we are back to consider what it means we say the probability $P(H)$ of getting a head in a coin tossing is equal to $0.5$. It means that the experimental result of $N_H/N$ could not be exactly $0.5$, but the more we toss a coin, the smaller the "error".

Probability is subjective. Lacking precise knowledge of an event, we assign it a numerical value. Based on this value, we construct a calculation process; the final result, within a certain margin of error, conforms to the statistical results of the experiment. This is a startling phenomenon: the subjective can describe the objective world. However, this is something humanity has always been doing; aren't geometric concepts like points, lines, and planes, and the concept of numbers, also forms of subjective imagination?

## Chapter 7. The Theory of Gravitation
