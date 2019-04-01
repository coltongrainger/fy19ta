---
title: Solutions to Attendance Quiz (Week 9)
author: Colton Grainger (MATH 1300)
date: 2019-03-14
bibliography: /home/colton/coltongrainger.bib
---

This was an **ungraded** quiz given on 2019-03-07. I didn't collect statistics, but here's my impression (on a $0$ to $4$ scale with $4/4$ high).

problem number | actual class performance | problem difficulty
--- | --- | ---
1 | 1/4 | 1/4
2 | 0/4 | 4/4
3 | 1/4 | 2/4
4 | 1/4 | 3/4

## Definitions

Let $f$ be a function and $A$ a set of numbers contained in the domain of $f$. (If you like, you may assume $A$ is an interval of real numbers, like $(a,b)$ or $(-\infty, \infty)$ or $[a,b]$. However, these definitions hold for *any set* of numbers $A$ in the domain of $f$.)

1. A point $x_{\text{max}}$ in $A$ is a **maximum point** for $f$ on $A$ if $$f(x_{\text{max}}) \ge f(x)\qq{for every $x$ in $A$.}$$

    i. The number $f(x_{\text{max}})$ is called the **maximum value** of $f$ on $A$. 
    ii. We also say that $f$ "has its maximum value on $A$ at $x_\text{max}$".

2. A particular number $y_\text{above}$ is a **bound** for $f$ on $A$ if $$y_\text{above} \ge \abs{f(x)} \qq{for every $x$ in $A$.}$$

3. A point $x_\text{local}$ in $A$ is a **local maximum point** for $f$ on $A$ if:

> *There is a positive number $\delta > 0$ such that $x_\text{local}$ is a maximum point for $f$ on the set* $$\{\text{points in $A$ whose distance to $x_\text{local}$ is less than $\delta$}\}.$$

## Short answer

1. What part(s) of which definition(s) above should be modified to instead define a **minimum point** and the **minimum value** for a function $f$ on $A$?

    *Correct answer.* In definition 1, amend "max" to "min", "maximum" to "minimum", and "$\ge$" to "$\le$". 
    
    *Other answers.* Please actually *write* "$\le$". It is *not* sufficient to say that the inequalities "flip". For example, is the "flip" of the inequality $$\rho \ge 0$$ the inequality $$\rho \le 0 \qq{ or } \rho < 0?$$ I empathize^["Modern man, writes Foucault, was born in a welter of regulations: meticulous rules and subrules, fussy inspections, 'the supervision of the smallest fragment of life [...] in the context of the school, the barracks, the hospital or the workshop.'" [@Mer87, chapter 9]] with the casual attitude, but it is worth knowing why a *strict* inequality differs from a general inequality. 

2. List five numbers, in decreasing order, that bound the function $\arctan \colon \RR \to (-\frac \pi 2, \frac \pi 2)$.

    *Example answer.* Let's convince ourselves that the absolute value $\abs{\arctan{x}}$ is strictly less than $\pi/2$ for all real numbers $x$. 
    
    - Well, consider some angle $-\pi/2 < \theta < \pi /2$ and suppose that we let this angle $\theta$ gradually increase and decrease. 
    - Then  $\tan{\theta}$  will gradually range between $-\infty$ and $\infty$, because *tangent measures the slope of a ray* that makes an angle of $\theta$ with the $x$-axis. 
    - Because $\arctan$ is the inverse function to $\tan$, if we let the point $-\infty < x < \infty$ gradually increase and decrease, then $\arctan{x}$ should gradually increase and decrease from just above $-\pi/2$ to just below $\pi/2$.
    
    Taking absolute values, we know $\abs{\arctan{x}} < \pi/2$. Then *any number* greater than or equal to $\pi/2$ is a bound for the $\arctan$ function. Here's a list of such numbers in decreasing order.

    - $\frac\pi 2 + 5$
    - $\frac\pi 2 + 4$
    - $\ldots$
    - $\frac\pi 2 +1$
    - $\frac\pi 2$.

3. Suppose the function $$f(x) := \begin{cases} -x^2 &\text{ if $-1< x <1$}\\ 0 & \text{ if $x\le -1$ or $x \ge 1$}\end{cases}$$ represents force (N) in the positive $x$-direction on the head of a pendulum when the pendulum is displaced by $x$ (cm) from equilibrium. If there is a local maximum point for $f$ on $\RR$, find it; else, find a local minimum point for $f$ on $\RR$.

    *Correct answer.* $x= 0$ gives a local maximum point, and in fact *any* point $x \le -1$ or $1 \le x$ is a local maximum point. 
    
    This problem was rendered trivial by a **typo**. The restoring force on a pendulum for small displacements is *not* $-x^2$, but actually (where $k > 0$) $$g(x) := \begin{cases} -kx &\text{ if $-1< x <1$}\\ 0 & \text{ if $x\le -1$ or $1 \le x$}\end{cases}$$

    The function $g(x)$ has neither a local minimum point nor a local maximum point.

4.  Suppose $f$ and $g$ are increasing functions from $\RR$ to $\RR$. (Recall that a function $g$ is **increasing** on an interval if $g(a) < g(b)$ whenever $a$ and $b$ are two numbers in the interval with $a < b$.) Which of the following functions is *not* guaranteed to be an increasing function from $\RR$ to $\RR$?

    (A) $f + g$
    (B) $f \cdot g$
    (C) $f \circ g$
    (D) All of the above, i.e., none of them is guaranteed to be
        increasing.
    (E) None of the above, i.e., they are all guaranteed to be
        increasing.

    *Correct answer.* (B)

    *Explanation.*^[From Vipul Naik's Math 152 quiz solutions.] The problem with option (B) arises when one or both functions take negative values. For instance, consider the case $f(x) := x$ and $g(x) := x$. Both are increasing functions on all of $\RR$. However, the pointwise product is the function $x \mapsto x^2$, which is a decreasing function for negative $x$. Formally, the issue is that we cannot multiply inequalities of the form $A < B$ and $C < D$ unless we are guaranteed to be working with positive numbers.

## References

As usual, question 4 is from Naik [@Nai12] and the definitions are from Spivak [@Spi94].
