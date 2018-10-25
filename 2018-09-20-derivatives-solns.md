---
title: Derivatives I (Solutions)
author: Colton Grainger (MATH 1300)
date: 2018-09-20
repo: https://github.com/coltongrainger/pro19ta
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

Both the quiz and these solutions were written by Vipul Naik [@Na12] at the University of Chicago.

1.  Consider the expression $x^2 + t^2 + xt$. What is the derivative of
    this with respect to $x$ (with $t$ assumed to be a constant)?

    (A) $2x + 2t + x + t$
    (B) $2x + 2t + 1$
    (C) $2x + 2t$
    (D) $2x + t + 1$
    (E) $2x + t$

    *Answer*: Option (E)

    *Explanation*: When we differentiate with respect to $x$, keeping
    $t$ constant, the $x^2$ differentiates to $2x$, the $t^2$
    differentiates to $0$ (because it is constant) and the $xt$
    differentiates to $t$.

    Note that there's something else called *implicit differentiation*
    where we do not assume $t$ to be a constant but rather an *unknown
    function of $x$*. In that case, we differentiate the functions of
    $t$ with respect to $t$ and tag along a $dt/dx$. With that
    interpretation, the derivative would be $2x +
      2t(dt/dx) + x(dt/dx) + t$. However, we're assuming $t$ constant,
    so $dt/dx = 0$, and so the $dt/dx$ terms vanish and we are just left
    with $2t + x$.

    *The other choices*:

    Option (A) is what you get if you just differentiate each thing with
    respect to its own variable naively: $x^2$ gives $2x$, $t^2$ gives
    $2t$, $xt$, by the product rule, gives $x + t$. This is *completely
    wrong* because we are differentiating only with respect to $x$. (See
    the note on implicit differentiation right above this).

    Options (B), (C) and (D) are also possible results of incorrect
    differentiation.

2.  Which of the following verbal statements is **not valid as a general rule**?

    (A) The derivative of the sum of two functions is the sum of the
        derivatives of the functions.
    (B) The derivative of the difference of two functions is the
        difference of the derivatives of the functions.
    (C) The derivative of a constant times a function is the same
        constant times the derivative of the function.
    (D) The derivative of the product of two functions is the product of
        the derivatives of the functions.
    (E) None of the above, i.e., they are all valid as general rules.

    *Answer*: Option (D)

    *Explanation*: The correct replacement of option (D) is the product
    rule for derivatives, which, in words, states that: "the derivative
    of the product of two functions is the sum of the product of the
    derivative of the first function with the second function and the
    product of the first function with the derivative of the second
    function." If that seems cumbersome to you, feel grateful for the
    power of algebraic symbols to capture this compactly:

    $$(f \cdot g)' = (f' \cdot g) + (f \cdot g')$$

3.  Which of the following statements is **definitely true** about the
    tangent line to the graph of an everywhere differentiable function
    $f$ on $\RR$ at the point $(a,f(a))$ (Here, "everywhere
    differentiable" means that the derivative of $f$ is defined and
    finite for all $x \in \RR$)?

    (A) The tangent line intersects the curve at precisely one point,
        namely $(a,f(a))$.
    (B) The tangent line intersects the $x$-axis.
    (C) The tangent line intersects the $f(x)$-axis (the $y$-axis).
    (D) Any line through $(a,f(a))$ other than the tangent line
        intersects the graph of $f$ at at least one other point.
    (E) None of the above need be true.

    *Answer*: Option (C)

    *Explanation*: If the function is differentiable, then the tangent
    line has finite slope, and hence cannot be vertical. Thus, it is not
    parallel to the $y$-axis, and hence must intersect the $y$-axis.

    *The other choices*:

    Option (A) is not true, as discussed in class. For instance, for the
    $\sin$ function, the tangent line through any of the peak points is
    $y = 1$, and passes through all the peak points, hence it intersects
    the graph infinitely often. We can graphically construct a lot of
    examples where the tangent line at one point in the graph intersects
    the graph elsewhere. There are certain classes of functions for
    which the statement of option (A) *is* true, and we'll talk more
    about this when we discuss concave up and concave down.

    Option (B) is not true. The tangent line to $(\pi/2,1)$ for the
    $\sin$ function is $y = 1$ -- a horizontal line. Thus, it does not
    intersect the $x$-axis. In general, the tangent line does not
    intersect the $x$-axis iff it is horizontal, which happens iff the
    derivative at the point is zero.

4.  For a function $f: (0,\infty) \to (0,\infty)$, denote by
    $f^{(k)}$ the $k^{th}$ derivative of $f$. Suppose $f(x) := x^r$ with
    domain $(0,\infty)$, and $r$ a rational number. What is the
    **precise set of values** of $r$ satisfying the following: there
    exist a positive integer $k$ (dependent on $r$) for which $f^{(k)}$
    is identically the zero function.

    (A) $r$ should be an integer.
    (B) $r$ should be a nonnegative integer.
    (C) $r$ should be a positive integer.
    (D) $r$ should be a nonnegative rational number.
    (E) $r$ should be a positive rational number.

    *Answer*: Option (B)

    *Explanation*: If $r$ is $0$, then the derivative of the function is
    zero. For $r$ a positive integer, the $(r + 1)^{th}$ derivative is
    $0$. See also Routine Problem 14 of Homework 3 (Exercise 3.3.64 of
    the book, Page 129).

    For any other value of $r$, the power of $x$ keeps going down by $1$
    each time we differentiate. However, since we didn't start with a
    nonnegative integer, the power of $x$ never becomes $0$, so we keep
    going down and never stop. For instance, if $r = 5/3$, we have:

    $$f(x) = x^{5/3}, f^{(1)}(x) = (5/3)x^{2/3}, f^{(2)}(x) = (10/9)x^{-1/3}, \dots$$

    Note that the powers of $x$ in $f$ and its derivatives are $5/3$,
    $2/3$, $-1/3$, $-4/3$ and so on, going down by $1$ each time. Note
    that going down from $2/3$ to $-1/3$, the power skips right past
    $0$.

## References
