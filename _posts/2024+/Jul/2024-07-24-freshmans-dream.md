---
layout: post
title: "Freshmanʻs Dream"
tags: proofs
preview: "I explain the proof for Freshmanʻs dream in an abstract algebra setting."
contents: true
footnotes: false
published: true
---

# Freshmanʻs Dream | Proof

---

This article is all about freshmanʻs dream in the modern day. I will be mentioning it in the sense of the *prime characteristic* not regular binomial expansion. So, the setting we will be discussing is over the defined ring $R$. We define the *commutative ring* to be $R \equiv (S, +, \cdot)$ over a set of the real numbers, $S$. Further, we define the ring to be of *characteristic* $p$ so any multiple of $p$ evaluates to $0$. Thereʻs really no restriction so if we really want, $S$ could be $\mathbb{R}$, the entire set of reals. So, now for the conditions. We have the number $p$ which is always a prime number and $x,y \in R$ which means that $x$ and $y$ are inside the ring $R$. We are interested in the expression

$$
\begin{equation}
(x + y)^p
\end{equation}
$$

in this setting of $(1)$. This isnʻt the same as regular algebra, really this is *abstract algebra*. Binomial expansion of $(1)$ gives the $n$th coefficient given as...

$$
\begin{equation}
\binom{p}{n} = \frac{p!}{n!(p-n)!} \\ = p \left[\frac{(p-1)!}{n!(p-n)!}\right]
\end{equation}
$$

Now, each coefficient in the expansion is a multiple of $p$, so they will all evaluate to $0$ for some $n$. If we only look at the terms for $n$ when $n \in \lbrace1,...,p-1\rbrace$ we notice that these donʻt evaluate to $1/p$, the inverse of $p$. This is because we are choosing items from a set of $p$. They can never be fractional. These terms when $n \in \lbrace1,...,p-1\rbrace$ would all be $0$. The resulting binomial terms $x^{\alpha}y^{p-\alpha}$ would all be finite numbers but when multiplied with the coefficient in $(2)$ we get $0$. Hence, the only terms we would be left with would be when $n = 0$ and $n = p$ since they evaluate to 1 by direct inspection. In other words...

$$
\begin{equation}
\binom{p}{0} = \frac{p!}{0!(p - 0)!} = \frac{p!}{p!} = 1 \\ \binom{p}{p} = \frac{p!}{p!(p - p)!} = \frac{p!}{p!0!} = \frac{p!}{p!} = 1
\end{equation}
$$

The terms that match these coefficients are $x^p$ and $y^p$ which leaves us with...

$$
\begin{equation}
(x + y)^p = x^p + y^p
\end{equation}
$$

Which is what we sought to show. $\blacksquare$
