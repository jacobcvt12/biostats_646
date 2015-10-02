---
title: "Homework 4"
author: "Jacob Carey"
date: \today
header-includes:
    - \usepackage{amsthm}
    - \usepackage{mathtools}
    - \usepackage{tikz}
output: pdf_document
---

1. 
    $$
    \begin{aligned}
    (\limsup E_n)^C = \{x | x \notin \limsup E_n\} \\
    = \{x | x \notin \cap_{n=0}^{\infty} \cup_{k=n}^{\infty}E_k\} \\
    = \{x | x \in \cup_{n=0}{\infty}(\cap_{k=n}^{\infty}E_k)^C\} \\
    = \{x | x \in \cup_{n=0}{\infty}\cap_{k=n}^{\infty}E_k^C\} \\
    = \boxed{\liminf E_n^C}
    \end{aligned}
    $$

2. 
    (a)
        $$
        \begin{aligned}
        f_S(s) &= \int_{-\infty}^{\infty} f_X(s-y) f_Y(y) dy \\
        &= \int \lambda e^{-\lambda(s-y)}\lambda e^{-\lambda y} dy \\
        &= \lambda^2 s e^{-\lambda s}
        \end{aligned}
        $$
    (b) $\text{Gamma}(2, \lambda)$
    (c) **The base case has been established in part (a). Then suppose $X=Z_1 + ... + Z_{n-1} \sim \text{Gamma}(n-1, \lambda)$ and $Y \sim \text{exp}(\lambda)$.** 
        $$
        \begin{aligned}
        f_S(s) &= \int_0^s f_X(x) f_Y(s-y) dx \\
        &= \int \frac{\lambda^{n-1}x^{(n-1)-1}e^{-\lambda x}}{\Gamma(n-1)}\lambda e^{-\lambda(s-x)}dx \\
        &= \frac{\lambda^ns^{n-1}e^{-\lambda s}}{\Gamma(n)} \\
        &= \boxed{\text{Gamma}(n, \lambda)}
        \end{aligned}
        $$
    (d) 
        $$
        \begin{aligned}
        P(X>x+t|X>t) &= \frac{P(X>x+t,X>t)}{P(X>t)} \\
        &= \frac{P(X>x+t)}{P(X>t)} \\
        &= \frac{1-(1-e^{-\lambda(x+t)})}{1-(1-e^{-\lambda x)})} \\
        &= \frac{e^{-\lambda(x+t)}}{e^{-\lambda x}} \\
        &= e^{-\lambda x} \\
        &= 1-(1+e^{-\lambda x}) \\
        &= \boxed{P(X>x)}
        \end{aligned}
        $$
        **The interpration is that the exponential distribution is memoryless**
3. **Note that** 
    $$
    E \setminus D = \{x|x\in E \land x \notin D\} =
    \{x|x\in D^C \land x \notin E^C\} = D^C \setminus E^C
    $$
    **Then**
    $$
    E \Delta D = (E \setminus D) \cup (D \setminus E) = (D^C \setminus E^C) \cup (E^C \setminus D^C) = (E^C \setminus D^C) \cup (D^C \setminus E^C) = E^C \Delta D^C \qedsymbol
    $$

4. 
    (a)
        $$
        P(Y \leq y) = \frac{\arctan(y/s)-(-\pi/2)}{\pi/2-(-\pi/2)} = 
        \frac{\arctan(y/s)+\pi/2}{\pi}
        $$
        $$
        f_Y(y) = d/dy P(Y\leq y) = \frac{1}{\pi}\frac{s}{y^2+s^2}
        $$
    (b) 
        $$
        \begin{aligned}
        F_X(x) &= P(\mu + \sigma Y \leq x) = P(Y \leq \frac{x-\mu}{\sigma} \\
        &= \int_{-\infty}^{\frac{x-\mu}{\sigma}}\frac{dy}{\pi(1+y^2)} \\
        &= 1/\pi \arctan(y) \big|_{-\infty}^{\frac{x-\mu}{\sigma}} \\
        &= \frac{\arctan(\frac{x-\mu}{\sigma})}{\pi} + \frac{1}{2} \\
        &= F_X(x) \\
        f_X(x) &= \frac{d}{dx} F_X(x) = \frac{1}{(\sigma\pi)(1+(\frac{x-\mu}{\sigma})^2}
        \end{aligned}
        $$