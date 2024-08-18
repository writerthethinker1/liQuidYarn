---
layout: post
title: "Exponential Quaternion"
tags: proofs
preview: "I give the proof of the polar form for quaternions which lets us switch grids when we analyze them."
contents: true
footnotes: false
published: true
---

# Quaternion Exponential

---

This note is all about proving the statement for any quaternion $q = a + bi + cj + dk$ that $q = \|\|q\|\|e^{\hat{n}\varphi} = \|\|q\|\|(\cos(\varphi) + \hat{n}\sin({\varphi}))$. We can start with the geometrical interpretation of the quaternion and see that that it is made up of two parts: *a real part and an imaginary part*. Simply put, the quaternion can be written as...

$$
\begin{equation}
q = a + \mathbb{v}
\end{equation}
$$

where $\mathbb{v} = bi + cj + dk$. If we look at this, it is a *right triangle* with angle $\varphi$ in between the *hypotenuse* and *real part* $a$. So, by geometry, one way we can write $a$ is $a = \|\|q\|\|\cos(\varphi)$ and the length of the vertical (*imaginary*) part is $\|\|\mathbb{v}\|\| = \|\|q\|\|\sin(\varphi)$. Because the vertical part is pointing *north* always, all we have to do to get the vertical component of the triangle is *scale by the normal vector* which always points north too. The unit vector is

$$
\begin{equation}
\hat{n} = \frac{\mathbb{v}}{||\mathbb{v}||}
\end{equation}
$$

So, we end up getting...

$$
\begin{equation}
\hat{n}||\mathbb{v}|| = \frac{\mathbb{v}}{||\mathbb{v}||}||\mathbb{v}|| = \mathbb{v} = ||q||\hat{n}\sin({\varphi}) \\ \implies \mathbb{v} = ||q|| \hat{n}\sin(\varphi)
\end{equation}
$$

Putting all of this together gives...

$$
\begin{equation}
q = a + \mathbb{v} = ||q||\cos({\varphi}) + ||q||\hat{n}\sin(\varphi) \\ \implies q = ||q||(\cos(\varphi) + \hat{n}\sin({\varphi}))
\end{equation}
$$

which is partially what we want. Now, we will compute the form for $e^q$. Using $(1)$, we arrive at...

$$
\begin{equation}
e^q = e^{a + \mathbb{v}} = e^ae^\mathbb{v}
\end{equation}
$$

We know by Taylor series expansion that anytime we raise an *exponential* to an *imaginary number*, we end up with a *rotation* that puts us in the *unit circle* on the *quaternion plane*, $\mathbb{H}$. By *vector rotation formula*, we end up with...

$$
\begin{equation}
e^{\mathbb{v}} = \cos\left(||\mathbb{v}||\right) + \frac{\mathbb{v}}{||\mathbb{v}||}\sin(||\mathbb{v}||)
\end{equation}
$$

So, when we raise and *exponential by $q$*, we end up with...

$$
\begin{equation}
e^q = e^a\left[\cos\left(||\mathbb{v}||\right) + \frac{\mathbb{v}}{||\mathbb{v}||}\sin(||\mathbb{v}||)\right]
\end{equation}
$$

We want to show, $e^{\hat{n}\varphi} = \cos(\varphi) + \hat{n}\sin({\varphi})$ by intuition from looking at the equations we have so far. We already know $e^q$ from $(7)$ and all we are going to do now is input $\hat{n}\varphi$ instead of $q$ in the exponent. First we note that $\hat{n}\varphi$ has $a = 0$ and is *purely imaginary* due to $(2)$ and the fact that $\varphi \in \mathbb{R}$. In particular, we have...

$$
\begin{equation}
\hat{n}\varphi = \frac{\mathbb{v}}{||\mathbb{v}||}\varphi = \left[\frac{\varphi}{||\mathbb{v}||}\mathbb{v}\right] = \mathbb{v}^\ast
\end{equation}
$$

Now, we can use $(7)$ and compute $e^{\hat{n}\varphi}$...

$$
\begin{equation}
e^{\hat{n}\varphi} = e^0\left[\cos\left(||\mathbb{v}^\ast||\right) + \frac{\mathbb{v}^\ast}{||\mathbb{v}^\ast||}\sin(||\mathbb{v}^\ast||)\right] \\ = \cos\left(\frac{\varphi}{||\mathbb{v}||}||\mathbb{v}||\right) + \hat{n}\sin\left(\frac{\varphi}{||\mathbb{v}||}||\mathbb{v}||\right) \\ = \cos(\varphi) + \hat{n}\sin(\varphi)
\end{equation}
$$

So, $e^{\hat{n}\varphi} = \cos(\varphi) + \hat{n}\sin(\varphi)$. This is what we wanted to show for our intuition. Using $(4)$ and $(9)$, we end up with...

$$
\begin{equation}
q = ||q||e^{\hat{n}\varphi} = ||q||(\cos(\varphi) + \hat{n}\sin({\varphi}))
\end{equation}
$$

for any *quaternion*, as desired. $\blacksquare$
