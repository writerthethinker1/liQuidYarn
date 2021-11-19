---
layout: post
title: "Statistics Macros"
date: "2021-04-04"
tag: Intro
preview: "Stats typing tips!"
footnotes: false
contents: true
---

All other macros are given in this post, just check the .md file for this musing to see what to type to render them in mathjax. Happy typing, hope it's relaxing. Macros make life easier. These are the macros used often in statistics but not included in mathjax.

### Random variables

If you want to declare random variables as independent, use the `\ind` macro to give $\ind$ and if two random variables are not independent, then you can use the `\nind` macro to give $\nind$. To specify the distribution of any random variable, use the `\distas{..}` macro, for example, if you want and 'iid' sample you can have formatted as `\distas{iid}` or $\distas{iid}$.

If you want to describe a sample of random variables from $1$ to $n$, then you can use the `\sample{..}{..}` macro to give things like $\sample{X}{100}$. To add random variables of the same letter, you can use the `\add{..}{..}` macro to make the sum, for example, $\add{X}{90}$. Same with multiplying, use the `\mult{..}{..}` macro to give things like $\mult{Y}{8}$.

### Associations

For random variable associations, you can use the macros `\cov{..}` to give a covariance form of $\cov{X, Y}$, `\cor{...}` for correlations $\cor{X, Z}$.

### Operators

For probability statements, you can use the `\P{..}` to make a probability statement $\P{X = 1}$, it also works in display mode too! You don't have to manually add `\left(..\right)` to have things appear fine:

$$
\P{\sum X_i = 2}
$$

Similarly, for expectations, fisher information, variance, likelihoods, and log-likelihoods  there's `\E{..}`, `\I{..}`, `\Var{..}`, `\Li{..}`, `\li{..}` that does the same thing as the probability statement to give things like $\E{X^2}$, $\I{\ta}$, $\Var{X}$, $\Li{\ta \up X}$, and $\li{\ta \up X}$  and in display mode:

$$
\E{\int Xy^2dy} \ \ \I{\ta^2 + \sum \ta_i} \ \ \Var{X^8 + \frac{1}{4}} \\ \Li{\ta^2 + \frac{4}{3} \bigup X} \ \ \li{\ta^6 + \frac{2}{3} \bigup X}
$$


**Note on vertical conditioning bar '$\up$': the macro for it is `\up` and `\bigup` if you want a larger size. The one on the keyboard will be treated as part of a markdown table, so don't use it, the page won't be made correctly.**

### Distributions and Summary Statistics

Many of the commonly used distributions in statistics are there in macro form to make typing easy. There's `\bern` for the bernoulli distribution, `\Bin` for binomial distribution, `\dunif` for the discrete uniform distribution, `\geom` for the geometric distribution, `\hypgeo` for the hypergeometric distribution, `\nbin` for the negative binomial distribution, `\pois` for the poisson distribution, `\Beta` for the beta distribution, `\cauchy` for the Cauchy distribution, `\chisq{..}` for the chisquare distribution, `dexp` for the double exponential (laplace) distribution, `\expo` for the exponential distribution, `\F` for the F distribution, `\gam` for the gamma distribution, `\logis` for the logistic distribution, `\lognorm` for the log-normal distribution, `\N` for the normal distribution, ,  `\bern` for the Bernoulli distribution, `\gam` for the gamma distribution,`\paret` for the Pareto Distribution, `t` for the $t$-distribution, `\unif` for the continuous uniform distribution, and `\weib` for the Weibull Distribution. The distributions are given in form below as they appear in a post or page...

$$
\bern \ \ \Bin \ \ \dunif \ \ \geom \ \ \hypgeo \\ \nbin \ \ \pois \ \ \Beta \ \ \cauchy \ \ \chisq{\alpha} \ \ \dexp \ \ \expo \ \ \F \\ \gam \ \ \logis \ \ \lognorm \ \ \N \ \ \paret \ \ t \ \ \unif \ \ \weib
$$

There are also included macros for **pdfs, expected values, variance, moment generating functions, and (some) cdfs** for the 21 distributions named. The general form to access them is using the distribution macro name given above and adding the suffixes `d`, `ex`, `var`, `mgf`, and `cd` and inputing both the variable as well as function parameters for the form. For a function written as $f(x\up \alpha, \beta, \gamma)$ as a pdf, we input first $x$, then in order the other letters after the conditional sign. We leave an example for the exponential distribution below, for each entry we used `\expo`, `\expod`, `\expoex`, `\expovar`, `\expomgf`, `\expocd` as well the the parameters `x`, `t`, and `\beta`:

#### Exponential function (example)

$$
\text{Name: } \expo \ \ \ f(x|\beta) = \expod{x}{\beta} \ \ \ \E{X} = \expoex{\beta} \ \ \ \Var{X} = \expovar{\beta} \ \\ M_{X}(t) = \expomgf{t}{\beta} \ \ \ F(x|\beta) = \expocd{x}{\beta}
$$

with the latex code as

```latex
$$
\text{Name: } \expo \ \ \ f(x|\beta) = \expod{x}{\beta} \ \ \
\E{X} = \expoex{\beta} \ \ \ \Var{X} = \expovar{\beta} \
\\ M_{X}(t) = \expomgf{t}{\beta} \ \
\ F(x|\beta) = \expocd{x}{\beta}
$$
```

For functions that don't have moment generating functions but do have n-th moments, we illustrate the n-th moment macro below for the log-normal distribution, simply put a `nm` after the distribution name:

#### Log-norm n-th moment example

$$
\E{X^n} = \lognormnm{n}{\mu}{\sig}
$$

with code `\lognormnm{n}{\mu}{\sig}`. If we know the values given, we can write

$$
\E{X^n} = \lognormnm{n}{\cdot 1}{2}
$$

**Using numerical input:** If you want to use numerical input, make sure you specify all multiplication operations to make things eaiser to read. In the above we used `\lognormnm{n}{\cdot 1}{2}` and had to input for the moment number `\cdot 1` to make things easier to read.

when $\mu = 1$ and $\sigma = 2$.

Most information of the distributions is given from [this](http://www.stat.rice.edu/~dobelman/courses/texts/distributions.c&b.pdf) handout. Check it out if you want to verify the formulas.

---

In addition the error functon (in integral form) is also included...

$$
\erf{x}
$$

with latex as `\erf{x}`.

For summary statistics like those in the Tukey's 5 number summary, we have the macros `\fqt`, `\iqr`, `\Min`, `\Max`, `\tqt`, `\Med` as well as the mode with `\mode` and general quantile `\qt{..}{..}`. All of which give respectively:

$$
\fqt \ \ \iqr \ \ \Min \ \ \Max \ \ \tqt \ \ \med \ \ \mode \ \ \qt{\chisq{3}}{,0.4} \ \ \qt{X}{0.75}
$$

For order statistics, there is `\ord{..}{..}` that gives $\ord{Y}{5}$.

---

### Wrapping Up...

This wraps up the statistics macros for the site. These aren't part of any latex packages so only for here using jekyll blogs or the mathjax macros given here. There might be a giant .js file that works much like the physics.js file to load all the macros for the physics stuff. It doesn't change functionality, but makes the configuration nicer to read.

{% include signature.html %}
