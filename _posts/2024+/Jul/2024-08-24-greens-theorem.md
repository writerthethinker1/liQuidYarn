---
layout: post
title: "Greenʻs Theorem"
tags: proofs
preview: "I give proof of Greenʻs Theorem which allows us to use the fierce deity blade and form (the crescent moon and triangle)."
contents: true
footnotes: false
published: true
---

# Green's Theorem | Proof

In this paper I prove *Green's Theorem* which states

$$
\oint_C L dx + \oint_C M dy = \iint_D \left(\frac{\partial M}{\partial x} - \frac{\partial L}{\partial y}\right) dA
$$

for *any curve* $C$ over region $D$. The most abstract case we will use is the *abstract ellipse* since all other curves are derivative from it. The abstract ellipse is given by two curves: $C = C_1 + C_2$ and we will be computing line integrals over these two paths. For $C_1$ we always have $y = g_1(x)$ over $x \in (a,b)$ and for $C_2$ we always have $y = g_2(x)$ over $x \in (a,b)$. We separate the paths based off of $g_i(x)$ so $g_1(x)$ is the *positive direction* (bottom of ellipse) and $g_2(x)$ is the *negative direction* (top of ellipse). We always know that $x \in (a,b)$ and $y \in (c,d)$ since they are the relative extrema for $x$ and $y$ respectively. We can characterize the region $D$ in two ways *in terms of $x$* and *in terms of $y$* which we call $D_x$ and $D_y$ respectively. These two characterizations are the same since we are talking about the *inside of the ellipse* in each case. So, $D = D_x = D_y$ always. These characterizations are written as...

$$
D_x = \{(x,y) | a \leq x \leq b, g_1(x) \leq y \leq g_2(x)\}
$$

$$
D_y = \{(x,y) | g^{-1}_2(y) \leq x \leq g^{-1}_1(y), c \leq y \leq d\}
$$

Now, due to the two paths $C_1$ and $C_2$ we have by choice...

$$
\oint_C L dx = \oint_{C_1} L dx
$$

and

$$
\oint_C M dy = \oint_{C_2} M dy
$$

Now, we compute the double integral in terms of two parts contained in it. We begin with...

$$
\iint_{D_x} -\left(\frac{\partial L}{\partial y}\right) dydx
$$

This can be simplified as...

$$
\int_a^b \int_{g_1(x)}^{g_2(x)} -\left(\frac{\partial L}{\partial y}\right) dydx
$$

$$
= \int_a^b \int_{g_2(x)}^{g_1(x)} \left(\frac{\partial L}{\partial y}\right) dy dx
$$

$$
= \int_a^b L(x, g_1(x)) - L(x, g_2(x)) dx
$$

$$
= \int_a^b L(x, g_1(x)) dx
$$

$$
= \oint_{C_1} L dx
$$

we note that the second integral with $L(x,g_2(x))$ is not defined by *choice of path.* This gives us the simplified line integral. Now, we compute...

$$
\iint_{D_y} \left(\frac{\partial M}{\partial x}\right) dxdy
$$

$$
= \int_c^d \int_{g^{-1}_2(y)}^{g_1^{-1}(y)} \left(\frac{\partial M}{\partial x}\right) dxdy
$$

$$
= \int_c^d M(g_{1}^{-1}(y), y) - M(g_{2}^{-1}(y), y) dy
$$

$$
= \int_d^c M(g_{2}^{-1}(y), y) dy
$$

$$
= \oint_{C_2} Mdy
$$

where the first integral with $M(g_{1}^{-1}(y), y)$ is not defined by *choice of path.* So, putting all of this together, we know that...

$$
\oint_{C_1} L dx + \oint_{C_2} Mdy = \iint_D \left(\frac{\partial M}{\partial x} - \frac{\partial L}{\partial y}\right) dxdy
$$

and by choice of integral we already know...

$$
\oint_{C} L dx + \oint_{C} Mdy = \iint_D \left(\frac{\partial M}{\partial x} - \frac{\partial L}{\partial y}\right) dxdy
$$

which is *Green's Theorem.* This is as desired. $\blacksquare$
