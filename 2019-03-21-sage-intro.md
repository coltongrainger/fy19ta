---
title: Project Solutions à la SageMath (Week 10)
author: Colton Grainger (Math 1300)
date: 2019-03-20
revised:
---

One goal today is to be able to plot *with and without* Sage^[Sage is a family of free open-source mathematics software packages, first released in 2005 by William Stein (among others) at the University of Washington.]. You will need *some sort* of computer to access $$\texttt{sagecell.sagemath.org}.$$ (If you have trouble, these links are all posted at `quamash.net/math1300`.) You can also scan this QR code.

![<https://sagecell.sagemath.org/?q=ilvouj>](2019-03-21-qr-intro.png){height=5cm}

## Sage commands to get started

To define a *symbolic* function.

    f(x) = x^3 + 4*x^2 - 2*x + 1

To differentiate $f(x)$ *with respect to* $x$, i.e., to find $\dv{f}{x}$.

    diff(f(x), x)

To differentiate twice, i.e., to find $\dv[2]{f}{x}$.

    diff(f(x), x, 2)

To differentiate $xy + \sin(x^2) + e^{ -x }$ with respect to $x$ (notice the **asterisk** for multiplication).

    diff(x*y + sin(x^2) + e^(-x), x)

To plot a parabola on the domain $-1 < x< 1$.

    plot(x^2)

To plot $g(x) = x^2 \sin(1/x)$ on the domain $[-5, 5]$.

    g(x) = x^2 * sin(1/x)
    plot(g(x), -5, 5)

\newpage

To plot the function $h(x) = \abs{x}\sin(1/x)$ and its first derivative $\dv{h}{x}$ on the domain $[-2, 2]$.

    h(x) = abs(x)*sin(1/x)
    hprime(x)= diff(h(x), x)
    plot( h(x),-2,2 ) + plot( hprime(x),-2,2, color='red' )

Notice that I defined `hprime(x)` as the *symbolic* derivative of `h(x)`. In the last line, I *concatenated* the `plot` command so that Sage will *superimpose* the plots. That is, `plot(h) + plot(diff(h,x))` tells Sage to plot $h$, then to plot $\dv{h}{x}$ in the same pane.

## Project solutions

Please *make a complete attempt* at problem 1 before looking at this solution.

![<https://sagecell.sagemath.org/?q=kcogeo>](2019-03-21-qr-prob1.png){height=4cm}

Again, *make a complete attempt* at problem 2 before looking at this solution.

![<https://sagecell.sagemath.org/?q=xezxqf>](2019-03-21-qr-prob2.png){height=4cm}

## (Optional) Reading material

If you like Sage, I have posted a Gregory Bard's *Sage for Undergraduates* along with two other guides at `quamash.net/math1300`. Bard's introduction (pages 1--20) and access to `sagecell.sagemath.org` is legit the best place to start.

## Enjoy your Spring Break!
