---
title: Integration (Attendance quiz)
author: Colton Grainger (Math 1300)
date: 2018-11-15
bibliography: /home/colton/Downloads/coltongrainger.bib
---

Print your **full name** and **three digit section number** in the top right corner and attempt each problem. You are free to discuss these questions with others while making your attempt. (Questions due to Vipul Naik [@Na12].)

\newcommand{\R}{\mathbf{R}}

1.  Consider the function(s) $[0,1] \to \R$. **Identify the function**s
    for which the integral (using upper sums and lower sums) is not
    defined.

    (A) $f_1(x) := \lbrace\begin{array}{rl} 0, & 0 \le x < 1/2 \\ 1, &
            1/2 \le x \le 1\end{array}$.
    (B) $f_2(x) := \lbrace\begin{array}{rl} 0, & x \ne 0 \text{ and } 1/x \text{ is an
            integer } \\ 1, & \text{otherwise} \end{array}$.
    (C) $f_3(x) := \lbrace\begin{array}{rl} 0, & x \text{ rational }\\
            1, & x \text{ irrational}\end{array}$
    (D) All of the above
    (E) None of the above

<!---
    *Answer*: Option (C)

    *Explanation*: For option (C), the lower sum for any partition is
    $0$ and the upper sum is $1$. Thus, the integral is not
    well-defined.

    For option (A), the function is piecewise continuous with only jump
    discontinuities, hence the integral is well-defined: in fact, it is
    $1/2$.

    For (B), the integral is zero. We can see this by noting that the
    points where the function is $0$ are all isolated points, so if in
    our partition the intervals surrounding each of these points is
    small enough, we can make the upper sums tend to zero. (This is hard
    to see. You should, however, be able to easily see that (A) has an
    integral and (C) does not. This forces the answer to be (C)).

    *Performance review*: $4$ out of $12$ got this correct. $3$ each
    chose (B) and (D), $2$ chose (E).

    *Historical note (last year)*: Everybody got this correct.
--->

2.  Suppose $a < b$. Recall that a *regular partition* into $n$
    parts of $[a,b]$ is a partition $a = x_0 < x_1 < \dots <
      x_{n-1} < x_n = b$ where $x_i - x_{i-1} = (b - a)/n$ for all
    $1 \le
      i \le n$. A partition $P_1$ is said to be a *finer partition* than
    a partition $P_2$ if the set of points of $P_1$ contains the set of
    points of $P_2$. Which of the following is a **necessary and
    sufficient condition** for the regular partition into $m$ parts to
    be a *finer partition* than the regular partition into $n$ parts?
    (Note: We'll assume that any partition is finer than itself).

    (A) $m \le n$
    (B) $n \le m$
    (C) $m$ divides $n$ (i.e., $n$ is a multiple of $m$)
    (D) $n$ divides $m$ (i.e., $m$ is a multiple of $n$)
    (E) $m$ is a power of $n$

<!---
    *Answer*: Option (D)

    *Explanation*: If $n$ divides $m$, then the partition into $m$
    pieces is obtained by further subdividing the partition into $m$
    parts, with each part divided into $n/m$ parts.

    *The other choices*: Option (B) is a *necessary* condition but is
    not a sufficient condition. For instance, the regular partition of
    $[0,1]$ into two parts corresponds to $\{ 0, 1/2, 1 \}$ and the
    partition into three parts corresponds to $\{ 0, 1/3, 2/3, 1
      \}$. These partitions are incomparable, i.e., neither is finer
    than the other.

    *Performance review*: $7$ out of $12$ got this correct. $4$
    chose(C), $1$ chose (B).

    *Historical note (last year)*: $5$ out of $15$ people got this
    correct. $6$ people chose (B), which is necessary but not
    sufficient, as indicated above. $2$ people chose (C), which is the
    reverse option. $1$ person chose (A) and $1$ chose (A)+(D).

    *Action point*: If you chose option (B), please make sure you
    understand the distinction between the options. Also review the
    concept of regular partitions and finer partition till you find this
    question obvious.
--->

3.  *Consumption smoothing (or, advice for Thanksgiving)*: A certain measure of happiness is found to
    be a logarithmic function of consumption, i.e., the happiness level
    $H$ of a person is found to be of the form $H = a +
      b \ln C$ where $C$ is the person's current consumption level, and
    $a$ and $b$ are positive constants independent of the consumption
    level.
    The person has a certain total consumption $C_{tot}$ to be split
    within two years, year 1 and year 2, i.e., $C_{tot} = C_1 +
      C_2$. Thus, the person's happiness level in year 1 is $H_1 = a + b
      \ln C_1$ and the person's happiness level in year 2 is
    $H_2 = a + b
      \ln C_2$. How would the person choose to split consumption between
    the two years to maximize average happiness across the years?

    (A) All the consumption in either one year
    (B) Equal amount of consumption in the two years
    (C) Consume twice as much in one year as in the other year
    (D) Consumption in the two years is in the ratio $a:b$

<!---
    *Answer*: Option (B)

    *Explanation*: Basically, happiness is logarithmic in consumption,
    so if consumption is unequal, then it can be distributed from the
    higher consumption year to the lower consumption year. The
    *fractional* loss in the higher consumption year is lower than the
    *fractional* gain in the lower consumption year. The nature of
    logarithmis means that the *absolute* loss in the higher consumption
    year is lower than the *absolute* gain in the lower consumption
    year. The process continues till consumption in both years is
    exactly equal.

    We can also do this formally. We are basically using the fact that
    the logarithm function is concave down.

    *Performance review*: Everybody got this correct.
--->
