---
layout: post
title: "Joint Quaternion Theorem"
tags: proofs
preview: "I give the proof to join the theory of quaternions with complex analysis, so all we need to explore more imaginary numbers is complex analysis."
contents: true
footnotes: false
published: true
---

# Joint Quaternion Theorem

---

> This note proves the *joint quaternion theorem* which connects *complex analysis* with *paradoxical analysis* (theory of quaternions). So, when we study quaternions, we arenʻt going outside the world of *complex analysis* with only *one complex term* $i = \sqrt{-1}$. The two fields are *the same*. It is like a *rosetta stone* between the two, so anything in complex analysis is the same in paradoxical analysis and *vice versa.* Basically, weʻve never really left *complex analysis* for *quaternions*, *octonions*, and so on...it is all the same and included in *complex analysis*. So, really all we need is *complex analysis* to do the same *exact stuff* as with *quaternions* and *higher dimensional variants*. Complex analysis is like a *fusion of everything*, so it does everything all at once.  

## The Proof

We begin with the *general form of a quaternion*, written as...

$$
\begin{equation}
q = q_0 + q_1i + q_2j + q_3k
\end{equation}
$$

Using the multiplication rules for quaternions, we can rewrite this as...

$$
\begin{equation}
q = (q_0 + q_1i) + (q_2 + q_3i)j
\end{equation}
$$

since $ij = k$. Now, we set $\alpha^\ast = q_0 + q_1i$ and $\beta^\ast = q_2 + q_3i$ which is just a *change of variables* to get...

$$
\begin{equation}
q = \alpha^\ast + \beta^{\ast}j
\end{equation}
$$

we know $\alpha^\ast, \beta^\ast \in \mathbb{C}$. Notice how similar this is to just a *plain complex number*, since $j^2 = -1$, we can write a *duality* between *quaternions* and *complex numbers*. All we need to study quaternions is then the behavior of $\alpha^\ast$ and $\beta^\ast$. If we put these two quantities inside a vector, we end up with...

$$
\begin{equation}
\vec{\gamma} = \pmatrix{\alpha^\ast \\ \beta^\ast} = \pmatrix{q_0 + q_1i \\ q_2 + q_3 i}
\end{equation}
$$

Which has $\vec{\gamma} \in \mathbb{C}^2$ and includes vectors *inside the Bloch sphere* as well as them scaled in $\mathbb{C}$. Notice that changing $q_0,...,q_3$ makes a *quaternion*. So, we write out the *conversion factor* using this idea...

$$
\begin{equation}
q_0 \equiv \pmatrix{q_0 \\ 0} \ \ \ \  q_1i \equiv  \pmatrix{q_1i \\ 0} \\ q_2j \equiv \pmatrix{0 \\ q_2} \ \ \ \ q_3k \equiv \pmatrix{0 \\ q_3i}
\end{equation}
$$

Now, when we add all the $q_0,...,q_3$ together we end up with...

$$
\begin{equation}
q_0 + q_1i + q_2j + q_3k \equiv \pmatrix{q_0 + q_1i \\ q_2 + q_3 i}
\end{equation}
$$

which is the most *general form* of *quaternions* expressed in a *complex analysis setting*. Equation $(4)$ is enough to give a *duality* due to *isomorphism* between *complex vectors* and *quaternions*. This is sufficient to complete the proof, as desired. $\blacksquare$
