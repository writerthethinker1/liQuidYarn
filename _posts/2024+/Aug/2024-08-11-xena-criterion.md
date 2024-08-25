---
layout: post
title: "Xenaʻs Criterion"
tags: proofs
preview: "I give Xenaʻs criterion to see how and when Xenaʻs powers will work."
contents: true
footnotes: false
published: true
---

# Xenaʻs Criterion

---

> This note is all about proving *Xenaʻs Criterion* as well as the *troubleshooting method* that comes with Xenaʻs Criterion. These methods show us when we have the *right tools* and *cosmic experience* to use *Xenaʻs power.* It also shows us what to do when even with the right tools and cosmic experience, the powers donʻt work. This is the troubleshooting part.

## Taraʻs Criterion

Consider

$$
X = \left\lbrace \frac{1}{2^n} \right\rbrace_{n = 0}^\infty = \left\lbrace1, \frac{1}{2}, \frac{1}{4},...\right\rbrace
$$

we know that $\inf\\{X\\} = 0$ and $\sup\\{X\\} = 1$. This is enough to guarantee *convergence* of the sequence. It is *monotone decreasing* since

$$
X(n+1) < X(n) \iff \frac{1}{2^{n+1}} = \frac{1}{2}\left(\frac{1}{2^n}\right) < \frac{1}{2^n} \\ \frac{1}{2}\alpha < \alpha \ \ :\ \ \ [\alpha > 0], \  \alpha = 1/2
$$

From here, we can extrapolate since:

$$
\frac{1}{2} > \frac{1}{\beta} \ \ \ \ \ (\beta \in \{3, 4, ...\})
$$

the family of sequences

$$
X^{\beta} = \left\lbrace \frac{1}{\beta^n}\right\rbrace_{n=0}^\infty = \left\lbrace1, \frac{1}{\beta}, \frac{1}{\beta^2}, ...\right\rbrace
$$

is also *monotone decreasing.* Further, $\sup\left\\{X^\beta\right\\} = 1$ and $\inf\left\\{X^\beta\right\\} = 0$. From here, we know $X^\beta$ for $\beta \in \\{2, 3, 4, ...\\}$ is *convergent!* This is as desired. $\blacksquare$

## Taraʻs Troubleshooting

Suppose we have

$$
\sum_{i = 0}^\infty \frac{1}{2^i} = 1 + \frac{1}{2} + \frac{1}{4} + \dots.
$$

We want to find out the *exact convergence* of this *series*. We will use the *method of forms!* So, we know

$$
S_0 = 1 + \frac{1}{2} + \frac{1}{4} + \dots
$$

and if we take out a *common factor*, we get:

$$
S_0 = 1 + \frac{1}{2}\left[1 + \frac{1}{2} + \frac{1}{4} + \dots\right] = 1 + \frac{1}{2}S_0
$$

Our goal is to find out what $S_0$ is. If we work with the algebra in the above equations we get...

$$
S_0 = 1 + \frac{1}{2}S_0 \implies S_0 - \frac{1}{2}S_0 = 1
$$

This then turns out to be...

$$
S_0\left[1 - \frac{1}{2}\right] = 1 \implies S_0 = 2
$$

So, then the solution by the *method of forms* is

$$
\sum_{i = 0}^\infty \frac{1}{2^i} = 2
$$

as desired. $\blacksquare$

> *The pen is mightier than the sword!*
