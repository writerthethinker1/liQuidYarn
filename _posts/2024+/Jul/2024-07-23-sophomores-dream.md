---
layout: post
title: "Sophomoreʻs Dream"
tags: proofs
preview: "I explain the two proofs for sophomoreʻs dream and the solutions for the integrals."
contents: true
footnotes: false
published: true
---

# Sophomoreʻs Dream | Proof

---

This article is all about proving the two forms of *sophomoreʻs dream* and giving examples of their computation. So, letʻs begin and get with the proofs. The forms for the dream are...

$$
\begin{equation}
\int_{0}^{1} x^{-x} dx = \sum_{i = 1}^{\infty}i^{-i}
\end{equation}
$$

$$
\begin{equation}
\int_{0}^{1}x^xdx = -\sum_{i = 1}^{\infty}(-i)^{-i}
\end{equation}
$$

respectively. Meaning $(1)$ is the first form and $(2)$ is the second form. We will be explaining the second form first and then the first form. From here, we will compute the integrals using the resulting series and computation. These are the examples for this text.

---

## Form 2

This is the proof for the second form of sophomoreʻs dream, equation $(2)$. We begin with the formula $z = x^x$, using the exponential form, we can rewrite this as $z = e^{\log(x^x)}$ where $\log$ is the *natural logarithm*. In the entirety of this text, $\log$ means the natural logarithm. Now, we keep simplifying $z$ to get $z = e^{x\log(x)}$. We will be using the Taylor series representation for $e^x$ to gext a form we can integrate. We know as reference that...

$$
\begin{equation}
e^x = \sum_{i = 0}^{\infty} \frac{x^i}{i!}
\end{equation}
$$

This is valid for all $x \in (-\infty, \infty)$. So, using the form $e^{x\log(x)}$ we easily can see...

$$
\begin{equation}
e^{x\log(x)} = \sum_{i = 0}^{\infty} \frac{[x\log(x)]^i}{i!} \\ = \sum_{i = 0}^{\infty} \frac{x^i[\log(x)]^i}{i!}
\end{equation}
$$

Now, the question is what are the range of values that $x\log(x)$ can take? For this, we set $y = x\log(x)$ and need to find extrema. We are only curious about $x \in (0,1)$ since these is the bounds of integration in the original integral. We will compute the first and second derivatives directly as...

$$
\begin{equation}
y^\prime = \log(x) + 1 \\ y^{\prime\prime} = \frac{1}{x}
\end{equation}
$$

We now use the first derivative test to find any extrema. To do this, we will set the first derivative to zero and compute the resulting value of $x$. When we do this, we get...

$$
\begin{equation}
y^\prime = \log(x) + 1 = 0 \\ \implies \log(x) = -1 \\ \implies x = e^{-1}
\end{equation}
$$

So, one extrema was found. The resulting value for $y$ is $y = e^{-1}\log(e^{-1}) = -e^{-1}$. The point $(e^{-1}, -e^{-1})$ is an *extreme point.* Now, we just need to know if it is a *minimum* or *maximum*. To do this, we use the second derivative test by evaluating the second derivative at the extreme point and checking the sign...

$$
\begin{equation}
y^{\prime\prime} = \frac{1}{e^{-1}} = e
\end{equation}
$$

We know that $e$ is positive, so by the second derivative test, this would be a minimum. Now, is this a *global minimum*? That is, is this the smallest value for the functionʻs range? To answer this, we will look at the first derivative. So, before $x = e^{-1}$ we have that $y^\prime$ is negative and always after $x = e^{-1}$ we have that $y^\prime$ is positive. This is enough for us to conclude that the point $(e^{-1}, -e^{-1})$ is a *global minimum*. Now, we just need to find the *global maximum* of $y = x\log(x)$. An easy way is to just take the limit to infinity...

$$
\begin{equation}
\lim_{x \to \infty} x\log(x) = \infty \cdot \infty = \infty
\end{equation}
$$

So, the global maximum is $(\infty, \infty)$ and this gives the range as $R: [-1/e, \infty)$ for $y = x\log(x)$ over $x \in (-\infty, \infty)$. For our interests, we only use $x \in (0,1)$ due to the bounds of integration on $z = x^x$. This is enough to guarantee *uniform convergence* of

$$
\begin{equation}
e^{x\log(x)} = \sum_{i = 0}^{\infty} \frac{x^i[\log(x)]^i}{i!}
\end{equation}
$$

So, we know that $(9)$ converges for $x \in (0,1)$. Now, we can start computing the integral...

$$
\begin{equation}
\int_{0}^{1}x^x dx = \int_{0}^{1} \sum_{i = 0}^{\infty} \frac{x^i [\log(x)]^i}{i!}dx \\ = \sum_{i = 0}^{\infty} \int_{0}^{1}\frac{x^i [\log(x)]^i}{i!}dx \\ = \sum_{i = 0}^{\infty} \frac{1}{i!}\int_{0}^{1}{x^i [\log(x)]^i}dx
\end{equation}
$$

Where we are allowed to exchange the integral with the sum due to *uniform convergence*. Now, all we have to do is compute...

$$
\begin{equation}
\int_{0}^{1} x^i [\log(x)]^idx
\end{equation}
$$

to find out the answer. We can do this by substitution with $x = e^{-u/(i+1)}$. First, we need to rewrite the bounds of integration. We have right now that $x \in (0,1)$ and we just need to find out the corresponding values for $u$. To do this, we will back-solve for $u$ given the bounds for $x$. We can do this because the function $e^{-u/(i+1)}$ is *strictly decreasing*. This is because it has the form $e^{-\alpha}$ which we know is always strictly decreasing in $\alpha$. So, letʻs find out the transformed bounds...

$$
\begin{equation}
x = 0: 0 = e^{-u/(i+1)} \implies u = \infty \\ x = 1: 1 = e^{-u/(i+1)} \implies \log(1) = -u/(i+1) \implies 0 = -u/(i+1) \\ \implies u = 0
\end{equation}
$$

So, we know that when $x \in (0,1)$, we have $u \in (0, \infty)$ which means all we have to do now is use the substitution and change the bounds. Now, we need an equivalent for $dx$ in the integration. Using the fact $dx = f^{\prime}(u)du$ from calculus, we have...

$$
\begin{equation}
dx = -\frac{e^{-u/(i+1)}}{i + 1} du
\end{equation}
$$

by the chain rule. Now, we just rewrite the integral...

$$
\begin{equation}
\int_{0}^{1}x^i[\log(x)]^i dx = \int_{0}^{\infty} \left[e^{-u/(i+1)}\right]^i \left[-\frac{u}{i+1}\right]^i \left[\frac{-e^{-u/(i+1)}}{i + 1}\right] du
\end{equation}
$$


Now, we do some simplifying and take out any constants...

$$
\begin{equation}
\frac{(-1)^{i + 1}}{(i+1)^{i+1}} \int_{0}^{\infty} u^i \left[e^{-ui/(i+1)} e^{u/(i+1)}\right]du
\end{equation}
$$

We now solve for the bracketed term in $(15)$...

$$
\begin{equation}
e^{-u/(i+1)} \cdot e^{-ui/(i+1)} = e^{- \left[\frac{u}{i+1}(i+1)\right]} = e^{-u}
\end{equation}
$$

This gives us the final form of the integral as...

$$
\begin{equation}
\frac{(-1)^{i + 1}}{(i+1)^{i+1}} \int_{0}^{\infty} u^i e^{-u}du
\end{equation}
$$

We know that the integral in $(17)$ is the gamma function as given by Bernoulli. So, we can rewrite $(17)$ as...

$$
\begin{equation}
\frac{(-1)^{i + 1}}{(i+1)^{i+1}} (i!)
\end{equation}
$$

Which means...

$$
\begin{equation}
\int_{0}^{1} x^i [\log(x)]^idx = \frac{(-1)^{i + 1}}{(i+1)^{i+1}} (i!)
\end{equation}
$$

as we wanted. Going back to $(10)$, we can substitute our value for the integral in $(20)$ for the last equation, we arrive at...

$$
\begin{equation}
\sum_{i = 0}^{\infty} \frac{1}{i!}\int_{0}^{1}{x^i [\log(x)]^i}dx \\ = \sum_{i = 0}^{\infty} \frac{1}{i!}\frac{(-1)^{i + 1}}{(i+1)^{i+1}} (i!) \\ = \sum_{i = 0}^{\infty} \frac{(-1)^{i + 1}}{(i+1)^{i+1}} = \sum_{i = 0}^{\infty} (-1)^{i + 1} (i+1)^{-(i+1)}
\end{equation}
$$

So, by $(10)$ and $(20)$, we know...

$$
\begin{equation}
\int_{0}^{1}x^x dx = \sum_{i = 0}^{\infty} (-1)^{i + 1} (i+1)^{-(i+1)}
\end{equation}
$$

as fact. For computation, we want to rewrite the form so it is easy to read. We will now rewrite the sum on the right hand side of $(21)$...

$$
\begin{equation}
\sum_{i = 0}^{\infty} (-1)^{i + 1} (i+1)^{-(i+1)} = -\sum_{i = 1}^{\infty} (-1)^{i -1} i^{-i} \\ = -\sum_{i=1}^{\infty} (-1)^{i}i^{-i} = -\sum_{i=1}^{\infty}(-1)^{-i}i^{-i} \\ = -\sum_{i = 1}^\infty (-i)^{-i}
\end{equation}
$$

To make this equivalence, we used the fact that the reciprocal of negative one is negative one. In sum, we just proved...

$$
\begin{equation}
\int_{0}^{1}x^x dx = -\sum_{i = 1}^\infty (-i)^{-i}
\end{equation}
$$

as desired. $\blacksquare$

---

## Form 1

Now, we will prove the first form of sophomoreʻs dream, equation $(1)$. We will begin similarly with $z = x^{-x}$ and rewrite it using the exponential form. This gives us $z = e^{-x\log(x)}$ and we know...

$$
\begin{equation}
e^x = \sum_{i = 0}^{\infty} \frac{x^i}{i!}
\end{equation}
$$

for all $x \in (-\infty, \infty)$. We can rewrite the exponential form now as...

$$
\begin{equation}
e^{-x\log(x)} = \sum_{i = 0}^{\infty} \frac{[-x\log(x)]^i}{i!} \\ = \sum_{i = 0}^{\infty} \frac{(-1)^i x^i [\log(x)]^i}{i!}
\end{equation}
$$

We are interested in the function $y = -x\log(x)$ and want to know the range over $(0, \infty)$. Note that this function is just the reverse of $x\log(x)$ in output. Meaning, the function takes on the *opposite values* linearly over $x \in (0, \infty)$. Hence, using what we found out about $x\log(x)$ in the proof of Form 2, we know the range will be $R: (-\infty, e^{-1}]$ for $y = -x\log(x)$ over $x \in (0, \infty)$. Really, for our purposes in the integral in $(1)$, we are interested in $x \in (0, 1)$. Now, over $x \in (0,1)$ we know the set of values $-x\log(x)$ takes will be a subset of $(-\infty, e^{-1}]$ and this guarantees that the last equality in $(25)$ converges due to *uniform convergence* over $x \in (0,1)$. We can now start computing the integral in $(1)$...

$$
\begin{equation}
\int_{0}^{1} x^{-x}dx = \int_{0}^{1} \sum_{i = 0}^{\infty} \frac{(-1)^i x^i [\log(x)]^i}{i!} dx \\ = \int_{0}^{1} \sum_{i = 0}^{\infty} \frac{(-1)^i}{i!}x^i [\log(x)]^idx \\ = \sum_{i = 0}^{\infty}\int_{0}^{1} \frac{(-1)^i}{i!}x^i [\log(x)]^idx \\ = \sum_{i = 0}^{\infty} \frac{(-1)^i}{i!} \int_{0}^{1} x^i [\log(x)]^i dx
\end{equation}
$$

Now, using the work from the proof in Form 2, we already know the solution for the integral in the last equation in $(26)$, see $(19)$. By substitution, we arrive at...

$$
\begin{equation}
\sum_{i = 0}^{\infty} \frac{(-1)^i}{i!} \left[(-1)^i(i+1)^{-(i+1)} (i!)\right] \\ = \sum_{i = 0}^{\infty} (-1)^{2i} (i+1)^{-(i+1)} \\ = \sum_{i = 0}^{\infty} (i+1)^{-(i+1)} \\ = \sum_{i = 1}^{\infty} i^{-i}
\end{equation}
$$

In sum, we know...

$$
\begin{equation}
\int_{0}^{1} x^{-x}dx = \sum_{i = 1}^{\infty} i^{-i}
\end{equation}
$$

which is what we sought to show. $\blacksquare$

---

## Examples

We now give example usage of the results of sophomoreʻs dream. The results let us compute the two integrals given in $(1)$ and $(2)$. This would be the application. So, letʻs work on evaluating the first integral, in $(1)$.

$$
\begin{equation}
\int_{0}^{1}x^{-x}dx = \sum_{i = 1}^{\infty} i^{-i} \\ = 1^{-1} + 2^{-2} + 3^{-3} + \cdots \\  = \frac{1}{1^1} + \frac{1}{2^2} + \frac{1}{3^3} + \cdots \\ = 1 + \frac{1}{4} + \frac{1}{27} + \cdots
\end{equation}
$$

This is what the integral really is down to a numerical answer. Even if an integral is hard, as long as there is a visible *area*, there is always a *number*. Sometimes, we just canʻt find it. In this case, we have a solution that always works. Now, to get this number, we just have to keep adding the sums and we will arrive at the solution. A computer in the modern day can do this for us! So, letʻs write down the solution down to 20 iterations, so up to $i = 20$. We will use 7 decimal places for an approximation.

$$
\begin{equation}
\int_{0}^{1} x^{-x}dx \approx \sum_{i = 1}^{20} i^{-i} = 1.2912860
\end{equation}
$$

This is the solution for 20 iterations, the more iterations we take, the better the result. Now, we will compute the second integral in $(2)$. We know...

$$
\begin{equation}
\int_{0}^{1} x^x dx = -\sum_{i = 1}^{\infty}(-i)^{-i} \\ = -\left[-1^{-1} + -2^{-2} + -3^{-3} + \cdots \right] \\ = -\left[\frac{1}{-1^1} + \frac{1}{-2^2} + \frac{1}{-3^3} + \cdots\right] \\ = -\left[-1 + \frac{1}{4} - \frac{1}{27} + \cdots \right] \\ = 1 - \frac{1}{4} + \frac{1}{27} + \cdots
\end{equation}
$$

This would be the numerical answer for the integral. So, letʻs take the sum up to 20 iterations or up to $i = 20$ and round up to 7 decimal places.

$$
\begin{equation}
\int_{0}^{1} x^{x}dx \approx -\sum_{i = 1}^{20} (-i)^{-i} = 0.7834305
\end{equation}
$$

This is the answer for the integral up to 7 decimal places. This is how sophomoreʻs dream works, by using summation and series to evaluate difficult integrals. Thanks for reading! $\blacksquare$


{% include signature.html %}
