---
layout: post
title: "Pythagorean Theorem"
tags: proofs
preview: "I give the proof of the pythagorean theorem in words and formulae."
contents: true
footnotes: false
published: true
---

# Pythagorean Theorem | Proof

---

In this paper, I prove the *pythagorean theorem.* Formally, the *pythagorean theorem* is all about right triangles. So, for any *right triangle* with sides $a, b$, and $c$ where $a, b$ are the *legs* and $c$ is the *hypotenuse*. We know by the *pythagorean theorem* that $a^2 + b^2 = c^2$. Our goal is to prove this fact. Consider a *square* made from the sum of the legs $a+b$. We know the area would be the square of this term, which is $(a + b)^2$, expanding it gives $\ell_0 = (a + b)^2 = a^2 + b^2 + 2ab$. This is the area of the square, we know this as true. Now if we join the points between $a$ and $b$ together along all the sides, we end up with *4 similar right triangles* inside the square. Alongside this, we create a 4-figure in the interior. In the triangles, we know that two legs are *congruent* (sides $a$ and $b$ respectively) and the interior angle is a *right angle* amongst all triangles. This is sufficient to show that all 4 triangles are *congruent* in the square. The third side, then, must be the same amongst all the triangles, we will call it $c$. Now, since all the sides of the 4-figure are equal and one angle is *right* (this is due to the fact that the complementary angles of a *right triangle* sum to $\pi/2$), we know that the 4-figure is a *square*. In terms of area then, if we break up the big square into the sum of the interior square and 4 congruent right triangles, we get $\ell_1 = 2ab + c^2$ as the area as well. But, both forms of the area $\ell_0$ and $\ell_1$ are the same since they are about the same object. So, we get...

$$
\ell_0 = \ell_1 \\ \implies a^2 + b^2 + 2ab = 2ab + c^2 \\ \implies a^2 + b^2 = c^2
$$

which gives the *pythagorean theorem*, as desired. $\blacksquare$
