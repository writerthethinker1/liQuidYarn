---
layout: post
title: "Math & Physics Macros"
date: "2021-04-04"
tags: Intro
---

{% include toc.html %}

### Item wrapping

If you're interested in wrapping items in parenthesis, no matter how big, use the `\pqty{..}` macro to do so. For example,

$$
\pqty{\int_{0}^{1} e^{-x/2a}dx}
$$

it wraps the largest one for the given expression you have. The same effect happens for brackets as well using `\bqty{..}`, bars for `\abs{..}` and double bars for `\norms{..}` all of which is given below respectively:

$$
\bqty{\sum x^6 + 3} \ \  \ \ % a quantity in brakets
\abs{\int 3x^2y} \ \  \ \ % a quantity in vertical bars
\norm{\int 23} \ \ % a norm ||a||
$$

### Orders & Integrals

When evaluating things like integrals, just use the `\evl^{..}_{..}` macro to make the upper and lower limits shown:

$$
\frac{1}{2x}\evl_{\infty}^{0.9}
$$

If you want to write the order of magnitude of something for example "the order of 30 is $\order{30}$" the `\order{..}` macro gives the way to typeset it.


### Vectors

For various types of vectors, there are many commands. For a simple bolded vector (or symbol in general) use `\vb{..}` to make it bold as in $\vb{a}$ or $\vb{\alpha}$. If you want an arrow above it use `\va{..}` macro to give $\va{a}$ or $\va{\alpha}$ and if you want a hat above your symbol, use `\vu{..}` to give things like $\vu{w}$. For basic vector operations like dot product and cross product to give things like $\va{a} \vdot \va{b}$ or $\va{e} \cp \va{i}$, use `\vdot` and `\cp` respectively.

### Bra-Ket Vectors

If you need to use these vectors, then `\ket{..}` gives $\ket{\phi}$, `\bra{..}` gives $\bra{\psi}$, `\braket{..}{..}` gives $\braket{\alpha}{\beta}$, `\ketbra{..}{..}` gives $\ketbra{\gamma}{\omega}$, `\ev{..}` gives $\ev{\beta}$, and `\mel{..}{..}{..}` for matricies with those vectors to give $\mel{\ze}{A}{\be}$.

### Gradients and Calculus Things

For things like gradients and other calculus things, use `\grad` to yield $\grad$, `\div` to yield $\div$, `\curl` to yield $\curl$, `\laplacian` to yield $\laplacian$. If you're doing matrix operations, you can use `\tr` for $\tr$, `\Tr` for $\Tr$, `\rank` for $\rank$, and `\erf` for $\erf{t}$. If you want to add a functional variation, you can use `\var..` to yield $\var f(x)$. For derivatives, you can use `\dv{..}{..}`, `\pdv{..}{..}`, and `\fdv{..}{..}` to get respectively

$$
\dv{x}{y} \ \ \pdv{f(x,y)}{y} \ \ \fdv{w}{x}
$$

If you have more than one derivative taken, you can use the multi-derivative macro known as `\mdv{..}{..}{..}`, `\mpdv{..}{..}{..}`, and `\mfdv{..}{..}{..}` to get

$$
\mdv{4}{x}{y} \ \ \mpdv{4}{f(x,u)}{u} \ \ \mfdv{9}{x}{y}
$$

**Note: the mult-derivative macros given here are custom for the site, the physics package has other notation, but won't load for this site.**

For things like residues of complex functions you can use `\Res` to get $\Res$, `\pv` or `\PV` for the Cauchy Principle Value to get $\pv$ or $\PV$ respectively. For the real or imaginaary parts of numbers you can use `\Re{..}` ot `\Im{..}` to get $\Re{f(x + yi)}$ and $\Im{q(r + iu)}$. If you have things like in-line text or cases, you can have `\qq{..}` for a quick quad text arguments as in

$$
f(x,y) = \begin{cases}
x^2 & \qq{early} \\
\sin(x) & \qq{afternoon} \\
\cos(y) & \qq{evening}
\end{cases}
$$

For other things like logical phrases and complex conjugates we have other `\q...` macros all given below (check the .md file for the way to write them):

$$
\qc \ \ \qcc \qif \ \ \qthen \ \ \qelse \ \ \qotherwise \ \ \qunless \ \ \\ \qgiven \ \ \qusing \ \ \qassume \ \ \qsince \ \ \qlet \ \ \qfor \ \ \qall \ \ \qeven \ \ \\ \qodd \ \ \qinteger \ \ \qand \ \ \qor \ \ \qas \ \ \qin
$$

### Sets and Things

If you want to write a set use the `\set{..}` macro to give things like $\set{1, 4, 2}$ and if you want to join or find the intersection of the sets, then use the `\sor` and `\sand` macros to give respectively $\sor$ and $\sand$. These are also useful for anti-commutators too! For the opening and ending of a set, you can also use `\lset` and `\rset` to have the opening and closing of set respectively: $\lset$ and $\rset$. and If you want to talk about a set's cardinality, you can have `\card{..}` to give $\card{A} = 4$. For things like minimum and maximum, you can use the `\mn{..}` and `\mx{..}` macros to yield $\mn{g(x)}$ and $\mx{y(s)}$ respectively. If you have domains or constraints, they can be subscripts like `\mn{..}_{..}` for $\mn{x(y)}_D$ over domain $D$. For the logical operation 'implies', you can use `\impl` as a macro for `\Rightarrow` that gives $\impl$. If you like writing definitions symbolically, there is also a `\as` macro that gives $\as$. Writing out a definition is more like $A \as \set{1, 3, 5}$ (see the .md file to see how it flows).

If you want to write a sum easily you can use the `\sum{..}{..}{..}` macro to indicate the variable, starting index, and ending index. It's used to write the formula below:

$$
\bs{x}{1}{\infty} \frac{1}{x} = \infty
$$

Also, if you want to write below any formula you have, you can use the `\bel{..}{..}` to indicate what you want the formula to be as well as what you want underneath it. For example if we wanted to label the sum as a series, we can have:

$$
\bel{\bs{x}{1}{\infty} \frac{1}{x}}{\text{series}} = \infty
$$

For the sets commonly used in mathematics to indicate numbers, we have `\R`, `\Nat`, `\S`, `\O`, `\Q`, `\C`, `\H`, `\Z`. Given below for your convenience.

$$
\R \ \ \Nat \ \ \S \ \ \O \ \ \Q \ \ \C \ \ \H \ \ \Z
$$

### Greek Letters

Greek letters that have been simplified in macro length are all given here. They have, in macro form 2-3 characters, for example `\alpha` is now `\al` and gives $\al$. They are all given below (check the .md file for this page for the ways to write them)...

$$
\al \ \ %alpha
\be \ \ %beta
\ga \ \ %gamma
\de \ \ %delta
\ep \ \ %epsilon
\ze \ \ %zeta
\ta \ \ %theta
\io \ \ %iota
\kap \ \ %kappa
\lam \ \ %lambda
\omc \ \ %omicron
\ups \ \ %upsilon
\om \ \ %omega
\sig \ \ %sigma
\Ga \ \ %Gamma
\De \ \ %Delta
\Ta \ \ %Theta
\Lam \ \ %Lambda
\Ups \ \ %Upsilon
\Om \ \ %Omega
\Sig %Sigma
$$

That's about if for the math and physics related vectors given here! Enjoy the day and have a positive outlook on things.
