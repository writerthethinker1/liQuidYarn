---
layout: post
title: "Seeing the Sphere: Part I"
tags: Sphere
preview: "How can we navigate the Bloch Sphere? Know where we are at just by looking at the vector? The real numbers are explained here!"
contents: true
footnotes: false
published: true
---

# Seeing the Sphere: Part I 🗡🔥

How do we know where we are on the Bloch Sphere? What does something like

$$
| \varphi \rangle = \pmatrix{\cos(\pi/4) \\ \sin(\pi/4)e^{i\pi}}
$$

mean? Are we closer to the top? bottom? sides?

Quantum computing would be easier if we just knew where we were all the time at a glance, right? I agree! So much that this article was written. It was very hard for me in the beginning, so it can be rough if you don't know your way. You could get lost.

I'm going to skip most of the physics stuff and derivations that, while helpful, can be *confusing to most people.* We won't be going over the axes nor looking at it mathematically. Just *geometrically*, something you can use immediately without having to think too much.

## Plain Spheres: What are they?

When we talk about spheres, we usually write them as

$$
\vec{\varphi} = \pmatrix{a \\ b \\ c} \\  a^2 + b^2 + c^2 = 1
$$

The set of all $a,b,c\in \mathbb{R}$ where the constraint holds true. This gives a unit sphere. The coordinates for $a,b,c$ are intuitive and are

$$
a = \cos(\theta) \\ b= \sin(\theta)\cos(\phi) \\ c = \sin(\theta)\sin(\phi)
$$

You can verify it yourself by plugging in the numbers in the constraint. This has to do with projections and is using cartesian coordinates, if you don't get it, *it's fine because we're not using it anyway* and are going to be dealing with 2D complex vectors which are easier once you get used to it! They are easier with practice and hold more path information about the particle's orientation. You'll find over and over again that spins, charges, and so on have a context. How you approached or measured takes this away. We'll sometimes write

$$
\pmatrix{0 \\ -1} = \vec{\varphi}
$$

or

$$
\pmatrix{-0 \\ 1} = \vec{\varphi}
$$

To preserve how the path taken prior to measurement. It came from an operation using a gate. Don't worry if it's confusing right now, by the end of the article it will make more sense, I hope.

## Moving onto the Quantum Sphere...

Now, spheres don't have to be described by real coordinates, if you want, many types of numbers 'trace' out a sphere. The sphere is just the geometric object that describes the set of numbers that belong to a set. Nothing more.

With different types of numbers, you can do different types of operations and this gives different numerical behavior within the sphere. The Bloch sphere is a set of complex vectors that fill in a unit sphere.

We write it as

$$
\vec{\varphi} =
\pmatrix{\alpha \\ \beta} \\ ||\alpha||^2 + ||\beta||^2 = 1
$$

where $\alpha,\beta \in \mathbb{C}$.

The axes have changed a little, but *we still have a sphere.* In fact, the rectangular grid is still present, but we have complex vectors on the surface. These behave differently than 3D real vectors.  

The form for any complex number is

$$
\gamma = \cos(\theta) + i\sin(\theta)
$$

And in this form we have

$$
||\gamma||^2 = 1
$$

Notice what happens when we allocate an entire vector using only complex coordinates. We have the norm of the vector as unit. And, this would imply:

$$
||\alpha||^2 \leq 1 \\ ||\beta||^2 \leq 1
$$

The only real way we could have the two numbers $\alpha,\beta$ work would be to use

$$
\alpha = r_1(\cos(\eta) + i\sin(\eta)) \\ \beta = r_2 (\cos(\zeta) + i\sin(\zeta)) \\ r_1^2 + r_2^2 = 1
$$

For free $\eta,\zeta$. This gives us a sphere. The coordinates aren't $x,y$ in this setting, *they work together and aren't independent!* Once you pick one, the other is made a little. Why?

$$
r_2^2 = 1 - r_1^2
$$

For now, let's just focus on $\eta = \zeta = 0$. Sounds easy, right? It will be.

The form for the vector when $\eta = \zeta = 0$ is

$$
\vec{\varphi} =\pmatrix{r_1 \\ \sqrt{1-r_1^2}} = \pmatrix{\cos(\theta) \\ \sin(\theta)}
$$

and in the same way we have a unit circle, this makes a unit circle too. We just describe it differently, like a different language. The top is when the weight goes all to $r_1$ and the bottom is when the weight goes all to $r_2$, just like with the equation

$$
\cos^2(\theta) + \sin^2(\theta) = 1
$$

We fill in the circle two ways, clockwise and anti-clockwise. This gives $\theta \in [-\pi/2, \pi/2]$

The positive values give clock wise and negative values give anti-clockwise.

So, we have a circle using

$$
\vec{\varphi} = \pmatrix{\cos(\theta) \\ \sin(\theta)} \\ \theta \in [-\pi/2, \pi/2]
$$

If you want to keep the period, you can do a transformation to have

$$
\vec{\varphi} = \pmatrix{\cos(\theta/2) \\ \sin(\theta/2)} \\ \theta \in [-\pi, \pi]
$$

That's it! If you got the above, you can describe a *quantum circle* or a sphere without any depth.

For example, if we write

$$
\vec{\varphi} = \pmatrix{\sqrt{0.3} \\ \sqrt{0.7}}
$$

we know we are in the lower right portion of the circle with the arrow form the center pointing southeast. Then, if we write

$$
\vec{\psi} = \pmatrix{0 \\ -1}
$$

We know we are at the bottom of the sphere, directly south and took the opposite way to arrive there, anti-clockwise. *The negative preserves the path taken!*

# Wrapping up...

The quantum sphere is not like a regular sphere we usually learn in plain geometry and can be easier once we know how to use the quantum circle. We use complex numbers to preserve information about the path a person took to walk on it and they come in handy. Later, in part II we will add complex numbers to give *depth* to the sphere and arrive that the notation we use today in quantum mechanics:

$$
|\varphi \rangle = \cos(\theta/2)e^{i \gamma}\ket{0} + \sin(\theta/2)e^{i(\gamma + \delta)}\ket{1}
$$

we just explained

$$
\ket{\varphi} = \cos(\theta/2)\ket{0} + \sin(\theta/2)\ket{1}
$$

which is a two dimensional quantum circle.

{% include signature.html %}
