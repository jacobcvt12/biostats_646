---
title: "Homework 2"
author: "Jacob Carey"
date: \today
header-includes:
    - \usepackage{amsthm}
    - \usepackage{mathtools}
output: pdf_document
---

1. Suppose that $\mathbb{P}_1$ and $\mathbb{P}_2$ are probabilities on the same $\sigma$-field $\mathcal{W}$. Prove that 
$$
\mathbb{P} = \alpha\mathbb{P}_1+(1-\alpha)\mathbb{P}_2\;\;0 \leq \alpha \leq 1
$$ 
is also a probability on $\mathcal{W}$  
    i) $P(\Omega) = 1$  
        $$
        \begin{aligned}
        P(\Omega) &= \alpha P_1(\Omega) + (1-\alpha) P_2(\Omega) \\
        &= \alpha \times 1 + (1-\alpha) \times 1 \\
        &= \boxed{1}
        \end{aligned}
        $$
    ii) $P(E) \geq 0 \text{ for all } E \in W$  
        Let $E \in W$. Then
        $$
        P(E) = \alpha P_1(E) + (1-\alpha) P_2(E)
        $$
        By designation, $\alpha$ and $1-\alpha$ are all $\geq 0$. Since $P_1$ and $P_2$ are both probabilities on $W$, $P_1(E)$ and $P_2(E)$ are also both $\geq 0$. Then $P(E) \geq 0$.
    iii) If $E_1, E_2, ...$ is a countable collection of mutually exclusive events, $P(\cup_1^{\infty}E_i) = \sum_1^{\infty} P(E_i)$.
        Let $E_1, E_2, ...$ be a countable collection of mutually exclusive events. Then
        $$
        \begin{aligned}
            P(\cup_1^{\infty}) &= \alpha P_1(\cup_1^{\infty}) + (1-\alpha) P_2(\cup_1^{\infty}) \\
            &= \alpha \sum P_1(E_i) + (1-\alpha) \sum P_2(E_i) \\
            &= \sum \alpha P_1(E_i) + (1-\alpha) P_2(E_i) \\
            &= \boxed{\sum P(E_i)} \\ \qedsymbol
        \end{aligned}
        $$

2. Show that for events $E$ and $F$  
$$
\mathbb{P}(E \cap F) \geq \mathbb{P}(E)+\mathbb{P}(B) -1
$$
3. In how many ways can 3 novels, 2 mathematics books, and 1 chemistry book be arranged on a bookshelf if
    (a) the books can be arranged in any order.
    (b) the mathematics books must be together and the novels must be together.
    (c) the novels must be together but the other books can be arranged in any order.
4. Show that
$$
{n \choose r-1} + {n \choose r} = {n+1 \choose r}\;\;\mbox{for integers $n$ and $r$}
$$
    $$
    \begin{aligned}
    {n \choose r-1} + {n \choose r} &= \frac{n!}{(n-r+1)!(r-1)!} + \frac{n!}{(n-r)!r!} \\
    &= \frac{n!}{(n+1-r)!(r-1)!} + \frac{n!}{(n-r)!r!} \\
    &= \frac{n!}{(n+1-r)(n-r)!(r-1)!} + \frac{n!}{r(n-r)!(r-1)!} \\
    &= \frac{n!r + n!(n+1-r)}{r(n+1-r)(n-r)!(r-1)!} \\
    &= \frac{n!r + n!(n+1) -n!r)}{(n+1-r)!r!} \\
    &= \frac{(n+1)!}{(n+1-r)!r!} \\
    &= \boxed{{n+1 \choose r}} \\
    \qedsymbol
    \end{aligned}
    $$
5. You can't remember which of $n$ keys fits your file drawer. You try each without replacement so that you will get the right key on the first, second,...,$n$ try. Show that each of these outcomes has the same probability, namely $1/n$.
6. If $n$ balls are placed at random into $n$ cells find the probability that exactly one  cell remains empty.
7. Show that it is more probable to get at least one ace (one) with four dice that it is to get at least one double ace in 24 thows of two dice.
8. A box contains ninety good screws and ten defective screws. If ten screws are used what is the probability that none is defective?