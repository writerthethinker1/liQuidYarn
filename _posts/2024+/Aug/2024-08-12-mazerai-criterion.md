---
layout: post
title: "Mazeraiʻs Criterion"
tags: proofs
preview: "I give Mazeraiʻs criterion to show if the body is the right fit for using Xenaʻs powers in a dead-zone."
contents: true
footnotes: false
published: true
---

# Mazeraiʻs Criterion

---

> This note deals with *mazeraiʻs criterion* which is all about whether the body is the "right fit" for a *dead-zone*. A *dead-zone* is a place or location with a lot of *lead* to block *cosmic experience*. It basically makes you feel *alone* rather than *one with the cosmos*.

## Mazeraiʻs Criterion (Leviathan)

We want to show that integration for $f(x) = e^x$ is *not the same* via *partial integration* of the parts of the *Taylor Series.* So, first, since we know

$$
\frac{d}{dx}e^x = e^x
$$

we can immediately infer that...

$$
\int e^x dx = e^x + C
$$

so we know the *solution*. In terms of the infinite *Taylor Series*, we have

$$
f(x) = e^x = \sum_{i=0}^\infty \frac{x^i}{i!} = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \dots
$$

so, what we end up with when we take *partial integration* as...

$$
\int f(x)dx = \int e^x dx = \int \sum_{i = 0}^\infty \frac{x^i}{i!} dx \\ = \sum_{i = 0}^\infty \frac{1}{i!}\int x^i dx = \sum_{i=0}^\infty \frac{1}{i!}\left[\frac{x^{i+1}}{i+1} + C\right] = \sum_{i = 0}^\infty \frac{x^{i+1}}{(i+1)!} + C \\ = e^x - 1 + C = e^x + C^\prime
$$

So, what the integration with the *Taylor Series* tells us is that it should be regraded as "*partial integration*" due to the $C^\prime$ constant. So, when we integrate with respect to a Taylor Series, we call it a "*partial-integration*." We know,

$$
\int e^x dx \neq \int_{\partial} e^x dx
$$

for this case! This is as desired. $\blacksquare$

> *Time heals all wounds!*
