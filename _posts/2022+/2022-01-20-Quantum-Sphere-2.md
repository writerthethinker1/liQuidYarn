---
layout: post
title: "Seeing the Sphere: Part II"
tags: Sphere
preview: "Going deeper and completing the way to travel on the sphere! You can now see a vector and know where it is by pointing on the sphere. Easy."
contents: true
footnotes: false
published: true
---

## Seeing the Sphere II

We now are going to add some depth into the sphere and see it in 3 dimensions using complex numbers.

We already know to see

$$
\vec{\varphi} = \pmatrix{\alpha \\ \beta}
$$

for real $\alpha, \beta$.

Now we are just going to talk about the vector

$$
\vec{\gamma} = \pmatrix{e^{i\delta} \\ e^{i\omega}}
$$

which is purely imaginary. The elements are all complex numbers and we are using Euler's identity $e^{i\theta} = \cos(\theta) + i\sin(\theta)$ to simplify some of the hard work.

### Coordinates: What are they?

Now, when we think of coordinates, we often think of location or orientation, words like 'north', 'south', 'tilted' and so on come up. All of these are on the right track, but one thing we can do in addition is to note the *placement* of the enclosing object that defines the coordinate system.

For example, a square defines the cartesian coordinate system, a cube for it in three dimensions, and so on. Looking at vectors in quantum physics, they are defined by the Bloch or quantum sphere. So, all vectors are 'inside' the sphere.

What complex numbers do is allow us to *rotate them*. Now, how do we rotate vectors? In the sphere, there are 2 main ways:

1. about the centre (giving depth)
2. about the vector's axis (changing 'spin orientation', like the earth rotating about its own axis making day and night)

### Imagining complex vectors

Picture a sphere and trying to move it 2 ways, horizontally or about a stick placed directly through it's center vertically. And then picture moving it about the point where your finger is touching it. If you touched it on the top right edge, imagine spinning it about your finger.

These are 2 ways to describe rotation on the sphere. We express them using complex numbers in vector form for easy reading:

$$
\vec{\gamma} = \pmatrix{e^{i\delta} \\ e^{i\omega}}
$$

The top one rotates it about your finger and the bottom one rotates it about the stick in the sphere, horizontally. We always rotate anti-clockwise for *increasing* $\delta, \omega$ and clockwise for *decreasing* $\delta, \omega$.

### How do we rotate about the center?

We'll focus on the vector

$$
\vec{\epsilon} = \pmatrix{\times \\ e^{i\omega}}
$$

All we are doing is focusing on the bottom imaginary number, don't worry about the top one, it's arbitrary for now. Now with complex numbers, $e^{i\omega}$ specifies the location of a complex number on the complex circle. When, $\omega$ changes, we *rotate* on the circle. We already have a vector for the circle's coordinates on the circle, $\vec{\varphi}$ and we need to move it horizontally. Because we are defining a new coordinate system, we note it as the bottom imaginary number to keep the coordinates valid. *Negative numbers on the quantum circle imply rotation about a horizontal axis, so the bottom imaginary number is for the horizontal rotation.*

So, reading something like

$$
\vec{\eta}_1 = \pmatrix{\sqrt{0.9}\\ \sqrt{0.1}e^{i\pi}}
$$

means we started on the quantum circle near the top right part and then rotated 180 degrees about the horizontal axis. Similarly, a vector like

$$
\vec{\eta}_2 = \pmatrix{\sqrt{0.9}\\ \sqrt{0.1}e^{i\pi/4}}
$$

means we were on the same location for the quantum circle but rotated 45 degrees only.

### How do we rotate about the vector's axis?

This has to be the top coordinate and is visualized as a 'hidden' circle located on the top of the vector. It spins the vector about it's own axis and represents coordinate (location) change in orientation.

> Imagine yourself walking on the sphere's surface and turning around, but keeping your position the same. Your location has changed and the coordinates reflect this. This is exactly what the top complex number in the vector means for the sphere. You just turned a little to see around you.

The vector

$$
\pmatrix{\sqrt{0.9}e^{i\pi} \\ \sqrt{0.1}}
$$

means you are on the top right part of the quantum circle, but turned around 180 degrees to see what's behind you.

The vector

$$
\pmatrix{\sqrt{0.9}e^{i\pi/3} \\ \sqrt{0.1}}
$$

Means you were at the same position as before but turned only 60 degrees to see what's there.

### Putting them together

Now we can put the rotational vector and positional vectors together to get coordinates like

$$
\vec{\epsilon} = \pmatrix{\alpha e^{i\delta} \\ \beta e^{i\omega}}
$$

We just made the quantum circle into a sphere!

For example,

$$
\pmatrix{\sqrt{0.3}e^{i\pi/3} \\ \sqrt{0.7}e^{i\pi/2}}
$$

means we are on the top right part of the quantum circle and then rotated 90 degrees horizontally and turned 60 degrees clockwise. On the sphere, this means we are behind the front nearly on the top part of the sphere and angled ourselves 60 degrees to see what's there.

## Wrapping up...

We talked about adding depth via rotations on the sphere. We used complex numbers on a vector to show two types of rotations that we could do on a sphere, horizontally and about the vector's axis. What we do is move along an axis like with earth rotating about it's axis and then turn around to see things. Then, we joined our position on the quantum circle with the rotations to give *depth* and make the Bloch sphere. Thanks for reading and I hope this makes looking at complex vector's easy!
