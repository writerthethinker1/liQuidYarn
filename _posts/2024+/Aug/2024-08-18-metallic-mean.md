---
layout: post
title: "Metallic Means"
tags: proofs
preview: "I give the proof of the formula for the nth metallic mean which is used for Xenaʻs power."
contents: true
footnotes: false
published: true
---

# Metallic Means

---

This note is all about proving the formula for the *$n$th metallic mean* which come up in *chaos theory* and using *Xenaʻs stones for power.* By definition, we have the *$n$th metallic mean* as meeting the following *metallic criterion*...

$$
\begin{equation}
x = n + \frac{1}{x}
\end{equation}
$$

we further require the *metallic mean* $x$ to be *positive* and *non-zero*. So, this means $x > 0$ and $x \neq 0$, always. Our goal is to solve for $x$ only. We now multiply by $x$ on both sides for $(1)$ since it is *non-zero*...

$$
\begin{equation}
x^2 = nx + 1 \\ \implies x^2 - nx - 1 = 0
\end{equation}
$$

From here, we use the *quadratic formula* and compute the possible values for $x$ as...

$$
\begin{equation}
x = \frac{n \pm \sqrt{n^2 - 4(1)(-1)}}{2(1)} \\ = \frac{n \pm \sqrt{n^2 + 4}}{2}
\end{equation}
$$

we further know that $n^2 + 4 > n^2$ for all $n \in \mathbb{N}$ and since $\sqrt{y}$ is a *strictly increasing function*, we always have $n < \sqrt{n^2 + 4}$ which means we need to only take the positive root for $\sqrt{n^2 + 4}$. So, the only value for $x$ is...

$$
\begin{equation}
x_n = \frac{n + \sqrt{n^2 + 4}}{2}
\end{equation}
$$

this form $x_n$ is the *$n$th metallic mean*, as desired. $\blacksquare$
