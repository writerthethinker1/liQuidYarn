---
layout: post
title: "Gradient Theorem"
tags: proofs
preview: "I give proof of the gradient theorem which lets you use Xenaʻs powers using Majoraʻs energy."
contents: true
footnotes: false
published: true
---

# Gradient Theorem | Proof

---

In this paper I *prove the gradient theorem* which is all about calculating the net work done (energy used) in any *dimensional field*. So, in any physical setting $U$ with start point $\mathbb{p}$ and end point $\mathbb{q}$ as vector positions, the net work done along *path* $\gamma$ defined in terms of *time* as $\mathbb{r}(t)$ for $t \in (a,b)$ we always have...

$$
\begin{equation}
\int_{\gamma} \nabla\varphi(\mathbb{r}) \cdot d\mathbb{r} = \varphi(\mathbb{q}) - \varphi(\mathbb{p})
\end{equation}
$$

this is a generalization of *greenʻs theorem*. It allows us to calculate really hard *line integrals* in a fast way. So, letʻs prove it. We begin with the *composite function*...

$$
\begin{equation}
\frac{d}{dt}(\varphi \circ \mathbb{r})(t)
\end{equation}
$$

we know how to compute this derivative using the *multivariate chain rule*, in this case $\mathbb{r}(t) = f(u_0,u_1,...,u_n)$ and $u_i = u_i(t)$ for all $i \in \{0,...,n\}$. We also know that $\varphi(\mathbb{r}(t)) = \varphi{(f(u_0,...,u_n)})$ as well. We can write now the derivatives of these two functions as...

$$
\begin{equation}
\mathbb{r}^\prime(t) = \pmatrix{f_{u_0}(t) \\ f_{u_1}(t) \\ \vdots \\ f_{u_n}(t)}
\end{equation}
$$

and

$$
\begin{equation}
\nabla\varphi(\mathbb{r}(t)) = \pmatrix{\varphi_{u_0}(\mathbb{r}(t)) \\ \varphi_{u_1}(\mathbb{r}(t)) \\ \vdots \\ \varphi_{u_n}(\mathbb{r}(t))}
\end{equation}
$$

By the *multivariate chain rule*, we can now write out what $(2)$ evaluates to as...

$$
\begin{equation}
\frac{d}{dt}(\varphi \circ \mathbb{r})(t) = \nabla\varphi(\mathbb{r}(t)) \cdot \mathbb{r}^\prime(t)
\end{equation}
$$

At this point, we can compute the first integral in $(1)$ as...

$$
\begin{equation}
\int_{\gamma} \nabla(\varphi(\mathbb{r})) \cdot d\mathbb{r} = \int_{\gamma} \nabla(\varphi(\mathbb{r}(t))) \cdot d\mathbb{r}(t)
\end{equation}
$$

to do this part, we used the fact that we parametrized $\mathbb{r}$ with *time* $t$. Now, we can use the *definition of the derivative* to get...

$$
\begin{equation}
\int_{a}^b \nabla(\varphi(\mathbb{r}(t))) \mathbb{r}^\prime(t)dt \\ = \int_{a}^{b} \frac{d}{dt}(\varphi \circ \mathbb{r})(t)dt \\ = \left[(\varphi \circ \mathbb{r})(t)\right]_a^b = \varphi(\mathbb{r}(b)) - \varphi(\mathbb{r}(a)) = \varphi(\mathbb{q}) - \varphi(\mathbb{p})
\end{equation}
$$

where $\mathbb{r}(b) = \mathbb{q}$ and $\mathbb{r}(a) = \mathbb{p}$ by definition. All of this gives the end result which is the *gradient theorem*, as desired. $\blacksquare$
