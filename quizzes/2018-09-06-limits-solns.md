---
title: More Limits (Solutions)
author: Colton Grainger (MATH 1300)
date: 2018-09-05
repo: https://github.com/coltongrainger/pro19ta
bibliography: /home/colton/Downloads/coltongrainger.bib
---

- We call a function $f$ left continuous on an open interval $I$ if, for all $a \in I$, $\lim_{x \to a^-} f(x) = f(a)$. Which of the following is an example of a function that is left continuous but not continuous on $(0,1)$?

  (A) $f(x) := \bigg\lbrace\begin{array}{rl}x, & 0 < x \le 1/2 \\ 2x, & 1/2 < x < 1 \\\end{array}$
  (A) $f(x) := \bigg\lbrace\begin{array}{rl}x, & 0 < x < 1/2 \\ 2x, & 1/2 \le x < 1 \\\end{array}$
  (A) $f(x) := \bigg\lbrace\begin{array}{rl}x, & 0 < x \le 1/2 \\ 2x - (1/2), & 1/2 < x < 1 \\\end{array}$
  (A) $f(x) := \bigg\lbrace\begin{array}{rl}x, & 0 < x < 1/2 \\ 2x - (1/2), & 1/2 \le x < 1 \\\end{array}$
  (A) All of the above

*Answer*: Option (A). *Explanation* from Vipul Naik [@Na12]: Note that in all four cases, the two pieces of the function are continuous. Thus, the relevant questions are: (i) do the two definitions agree at the point where the definition changes (in all four cases here, $1/2$)? and (ii) is the point (in all cases, $1/2$) where the definition changes included in the left or the right piece? 

For options (C) and (D), the definitions on the left and right piece agree at $1/2$. Namely the function $x$ and $2x - (1/2)$ both take the value $1/2$ at the domain point $1/2$. Thus, options (C) and (D) both define continuous functions (in fact, the same continuous function). This leaves options (A) and (B). For these, the left definition $x$ and the right definition $2x$ do not match at $1/2$: the former gives $1/2$ and the latter gives $1$. In other words, the function has a jump discontinuity at $1/2$. Thus, (ii) becomes relevant: is $1/2$ included in the left or the right definition? For option (A), $1/2$ is included in the left definition, so $f(1/2) = 1/2 = \lim_{x \to 1/2^-} f(x)$. On the other hand, $\lim_{x \to 1/2^+} f(x) = 1$. Thus, the $f$ in option (A) is left continuous but not right continuous. For option (B), $1/2$ is included in the right definition, so $f(1/2) = 1$ and $f$ is right continuous but not left continuous at $1/2$.

- Suppose $f$ and $g$ are functions $(0,1)$ to $(0,1)$ that are both left continuous on $(0,1)$. Which of the following is *not* guaranteed to be left continuous on $(0,1)$? 

  (A) $f + g$, i.e., the function $x \mapsto f(x) + g(x)$
  (A) $f - g$, i.e., the function $x \mapsto f(x) - g(x)$
  (A) $f \cdot g$, i.e., the function $x \mapsto f(x)g(x)$
  (A) $f \circ g$, i.e., the function $x \mapsto f(g(x))$
  (A) None of the above, i.e., they are all guaranteed to be left continuous functions

*Answer*: Option (D). *Explanation* again, from Vipul Naik [@Na12]: We need to construct an explicit example, but we first need to do some theoretical thinking to motivate the right example. The full reasoning is given below.

*Motivation for example*: Left hand limits split under addition, subtraction and multiplication, so options (A)-(C) are guaranteed to be left continuous, and are thus false. This leaves the option $f \circ g$ for consideration. Let us look at this in more detail. For $c \in (0,1)$, we want to know whether: $\lim_{x \to c^-} f(g(x)) \stackrel{?}{=} f(g(c))$. We do know, by assumption, that, as $x$ approaches $c$ from the left, $g(x)$ approaches $g(c)$. However, we do not know whether $g(x)$ approaches $g(c)$ from the left or the right or in oscillatory fashion. If we could somehow guarantee that $g(x)$ approaches $g(c)$ from the left, then we would obtain that the above limit holds. However, the given data does not guarantee this, so (D) is false. We need to construct an example where $g$ is *not* an increasing function. In fact, we will try to pick $g$ as a decreasing function, so that when $x$ approaches $c$ from the left, $g(x)$ approaches $g(c)$ from the right. As a result, when we compose with $f$, the roles of left and right get switched. Further, we need to construct $f$ so that it is left continuous but not right continuous. 

*Explanation with example*: Consider the case where, say: $f(x) := \bigg\lbrace\begin{array}{rl}1/3,& 0 < x \le 1/2 \\ 2/3, & 1/2 < x < 1 \\\end{array} \text{ and } g(x) := 1 - x.$ Note that both functions have range a subset of $(0,1)$. Composing, we obtain that: $f(g(x)) = \bigg\lbrace\begin{array}{rl}2/3,& 0 < x < 1/2\\ 1/3, & 1/2 \le x < 1 \\\end{array}.$ Note that $f$ is left continuous but not right continuous at $1/2$, whereas $f \circ g$ is right continuous but not left continuous at $1/2$. 

- Consider the function $$f(x) := \bigg\lbrace\begin{array}{rl} x, & x \text{ rational }\\1/x, & x \text{ irrational }\\\end{array}$$ 
  What is the set of all points at which $f$ is continuous?

  (A) $\{ 0, 1 \}$
  (A) $\{ -1,1 \}$
  (A) $\{-1,0 \}$
  (A) $\{ -1,0,1 \}$
  (A) $f$ is continuous everywhere

*Answer*: Option (B). *Explanation* one more time from [@Na12]: In this interesting example, instead of a *left* versus *right* split, we are splitting the domain into rationals and irrationals. For the overall limit to exist at $c$, we need that: (i) the limit for the function as defined for rationals exists at $c$, (ii) the limit for the function as defined for irrationals exists at $c$, and (iii) the two limits are equal. Note that regardless of whether the point $c$ is rational or irrational, we need *both* the rational domain limit and the irrational domain limit to exist and be equal at $c$. This is because rational numbers are surrounded by irrational numbers and vice versa -- both rational numbers and irrational numbers are dense in the reals -- hence at any point, we care about the limits restricted to the rationals as well as the irrationals. The limit for rationals exists for all $c$ and equals the value $c$. The limit for irrationals exists for all $c \ne 0$ and equals the value $1/c$. For these two numbers to be equal, we need $c = 1/c$. Solving, we get $c^2 = 1$ so $c = \pm 1$.

- Define the base $e$ of the "natural" exponential function. Hint: The derivative of every exponential function of the form $f(x) := a^x$ with $a>0$ is equal to a multiple of itself $f'(x) = \lim_{h\to 0}\frac{a^{x+h} -a^x}{h} = a^x \lim_{h\to 0}\frac{a^h-1}{h}$.

  (A) $e = \lim_{h\to 0} e^h$
  (A) $e$ is the number that satisfies $\log(1) = e$
  (A) $e = \lim_{h \to 0} \frac{e^h}{h}$
  (A) $e$ is the number that satisfies $e^{x+y} = e^xe^y$ for all $x,y \in \mathbf{R}$
  (A) $e$ is the number that satisfies $\lim_{h\to 0}\frac{e^h-1}{h} = 1$

*Answer*: Option (E). *Explanation* from Stephen Leduc [@Le10]: If we can find the value of $a$ such that $\frac{a^h-1}{h} = 1$, then $f'(x) = f(x)$. So let's define $e$ such that $$\lim_{h\to 0}\frac{e^h-1}{h} = 1.$$ Options (A), (B) and (C) are fallacious. Option (D) is not unique to $e$.

## References
