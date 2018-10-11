---
title: Derivatives II (Solutions)
author: Colton Grainger (MATH 1300)
date: 2018-10-11
repo: https://github.com/coltongrainger/pro19ta
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

True-false questions from [@Ro18]; multiple choice from [@Na12].

1. If $f(x)$ is a differentiable function, then $f(x)$ is a continuous function.

    - TRUE
    - FALSE


    *Answer*: TRUE

    *Explanation*: The derivative of $f(x)$ at $x =a$ is defined as $f'(a) = \lim_{h\to 0} \frac{f(a+h)-f(a)}{h}$ or equivalently $f'(a) = \lim{x \to a}\frac{f(x) - f(a)}{x-a}$. Assume $f(x)$ is differentiable at $x =a$. Then $$\lim{x \to a}\left(f(x) - f(a)\right) = \left( \lim_{x \to a}(x-a)\right)\left(\lim_{x\to a} \frac{f(x) - f(a)}{x-a}\right) = \lim_{x\to a}(x-a)\cdot f'(a) = 0$$ (verify last equality). What falls out is that $\lim_{x \to a} \left( f(x) - f(a)\right) = 0$, hence $\lim_{x\to a} f(x) = f(a)$, hence $f$ is continuous at the point $a$.


2. If $g$ is differentiable at $x = a$ and $f$ is differentiable at $x = g(a)$, then $f \circ g$ is differentiable at $x = a$.

    - TRUE
    - FALSE


    *Answer*: TRUE

    *Explanation*: Apply the chain rule! Let $h(x) = f(g(x))$. By the chain rule, $h'(x) = f'(g(x))g'(x)$. Can we evaluate $h'(a)$? Yes, since $g$ is differentiable at $x = a$, the derivative $g'(a)$ exists. Moreover, $f$ is differentiable at $x = g(a)$, so $f'(g(a))$ also exists. We conclude that $h'(a) = f'(g(a))g'(a)$ exists, and so $h = f \circ g$ is differentiable at $x =a$.


3. If $f''(c) = 0$, then $f(x)$ has an inflection point at $x=c$.
    

    - TRUE
    - FALSE


    *Answer*: FALSE

    *Explanation*: Recall that an inflection point is defined as a point at which a function changes concavity. That $f''(c) = 0$ is a necessary --- yet not sufficient --- condition for to have an inflection point at $(c, f(c)$. Do consider some counter examples here. Take the polynomial $f(x) = k$ for some fixed constant $k \in \RR$. Then $f''(x) = 0$ for all $x$, but none of these points correspond to points inflection, for $f$ is constant.


4. True or false: The following function is differentiable at $x =0$, $f(x) := \begin{cases} x+1, & x \le 0\\ 1- x^2, & x > 0.\end{cases}$

    - TRUE
    - FALSE

    *Answer*: FALSE

    *Explanation*: Check for continuity with left and right sided limits:
    $$\lim_{x \to 0^+} f(x) = \lim_{x \to 0^+} (1-x^2) = 1 = \lim_{x\to 0^-} (x+1) = \lim_{x\to 0^-} f(x).$$
    So $\lim_{x \to 0} f(x) = 1 = f(0)$. We've shown that $f$ is continuous. Is it differentiable? Consider the limit of difference quotient $\frac{f(h) - f(0)}{h}$ as $h \to 0$ from the left and right. 
    $$\text{from the left}\quad \lim_{h \to 0^-} \frac{f(h) - f(0)}{h} = \lim_{h \to 0^-}\frac{h+1-1}{h} = 1;$$
    $$\text{from the right}\quad \lim_{h \to 0^+} \frac{f(h) - f(0)}{h} = \lim_{h \to 0^+} \frac{1-h^2 -1}{h} = 0.$$
    The left and right limits approach $1$ and $0$, respectively. Graphically, we'd have a sharp cusp at $x =0$ (Note the $f$ behaves linearly when $x\le 0$ and quadratically when $x \ge 0$). Therefore $f$ is not differentiable at $x=0$.


5.  Suppose $f$ is a function defined on a closed interval $[a,c]$.
    Suppose that the left-hand derivative of $f$ at $c$ exists and
    equals $\ell$. Which of the following implications is **true in
    general**?

    (A) If $f(x) < f(c)$ for all $a \le x < c$, then $\ell < 0$.
    (B) If $f(x) \le f(c)$ for all $a \le x < c$, then $\ell \le 0$.
    (C) If $f(x) < f(c)$ for all $a \le x < c$, then $\ell > 0$.
    (D) If $f(x) \le f(c)$ for all $a \le x < c$, then $\ell \ge 0$.
    (E) None of the above is true in general.


    *Answer*: Option (D)

    *Explanation*: If $f(x) \le f(c)$ for all $a \le x < c$, then all
    difference quotients from the left are nonnegative. The limiting
    value, which is the left-hand derivative, is thus also nonnegative.

    *The other choices*: Options (A) and (B) predict the wrong sign. Option (C) is incorrect because even though the difference quotients are all strictly positive, their limiting value could be $0$. For instance, $\sin x$ on $[0,\pi/2]$ or $x^3$ on $[-1,0]$. It is likely that the people who chose option (B) made a sign computation error.

6.  Suppose $f$ and $g$ are increasing functions from $\RR$ to $\RR$. Which of the following functions is *not* guaranteed to be an increasing function from $\RR$ to $\RR$?

    (A) $f + g$
    (B) $f \cdot g$
    (C) $f \circ g$
    (D) All of the above, i.e., none of them is guaranteed to be
        increasing.
    (E) None of the above, i.e., they are all guaranteed to be
        increasing.

    *Answer*: Option (B)

    *Explanation*: The problem with option (B) arises when one or both functions take negative values. For instance, consider the case $f(x) := x$ and $g(x) := x$. Both are increasing functions on all of $\RR$. However, the pointwise product is the function $x \mapsto x^2$, which is a decreasing function for negative $x$. Formally, the issue is that we cannot multiply inequalities of the form $A < B$ and $C < D$ unless we are guaranteed to be working with positive numbers.

## References
