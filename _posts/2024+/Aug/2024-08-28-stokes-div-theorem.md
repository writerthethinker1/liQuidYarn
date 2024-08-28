---
layout: post
title: "Stokes and Divergence Theorem"
tags: proofs
preview: "I give proof of Stokes and Divergence theorem using differential forms and line integration."
contents: true
footnotes: false
published: true
---

# Stokes and Divergence Theorem | Proof

---

In this paper, I prove *Stokes Theorem* and the *Divergence Theorem* for functions of the form $\mathbf{F}: \mathbb{R}^3 \to \mathbb{R}^3$ which is abstractly written as...

$$
\begin{equation}
\mathbf{F} = \pmatrix{F_x \\ F_y \\ F_z}
\end{equation}
$$

under the bases $\mathbb{e}_1, \mathbb{e}_2, \mathbb{e}_3$ abstractly in *any orientation* so long as all of them are *unit* and *orthogonal* to each other. By definition of *differentials*, we can identify the *differential 1-form* mapping as

$$
\begin{equation}
F_x\mathbb{e}_1 + F_y\mathbb{e}_2 + F_z\mathbb{e}_3 \to F_xdx + F_ydy + F_zdz
\end{equation}
$$

for our reference, we *always have*...

$$
\begin{equation}
\omega_\mathbf{F} = F_x\mathbb{e}_1 + F_y\mathbb{e}_2 + F_z\mathbb{e}_3 \\ \text{d}\omega_{\mathbf{F}} = F_xdx + F_ydy + F_zdz
\end{equation}
$$

So, $\omega_{\mathbf{F}}$ is always the *1-form* and $\text{d}\omega_{\mathbf{F}}$ is always the *differential 1-form*. The derivative we have taken for the *differential 1-form* is the *exterior derivative* and uses the regular *rectangular infinitesimal bases* under no orientation. We note in Stokes formulation that $\omega_{\nabla \times \mathbf{F}}$ is the form for the *circulation* around *any defined point* in $\mathbf{F}$. If we take the *Hodge star* of this, we end up with $\star \omega_{\nabla \times \mathbf{F}}$ which is the *resultant* of the *normal vectors* to the circulation. This ends up measuring the *differential 1-form* again due to orthogonality, so we always have...

$$
\begin{equation}
\star\omega_{\nabla\times \mathbf{F}} = \text{d}\omega_{\mathbf{F}}
\end{equation}
$$

Now, we can write the full derivation of *Stokes Theorem*...

$$
\begin{equation}
\oint_{\partial \Sigma} \mathbf{F} \cdot d\gamma = \oint_{\partial \Sigma} \omega_{\mathbf{F}} = \int_{\Sigma} \text{d}\omega_{\mathbf{F}} = \int_{\Sigma} \star\omega_{\nabla \times \mathbf{F}} = \oint_{\gamma} (\nabla \times \mathbf{F})\cdot d\gamma \\ =  \iint_\Sigma (\nabla \times \mathbf{F}) \cdot d\Sigma
\end{equation}
$$

which is *Stokes Theorem*. In the first two equalities, we used *Greenʻs Theorem* and from here, we used $(4)$ for the next one. The last two equalities come from understanding that we are looking at *net circulation* over the *surface* $\Sigma$. Now, using similar reasoning, we can derive the  *Divergence Theorem* as well...

$$
\begin{equation}
\oint_{\gamma} (\nabla \cdot \mathbf{F}) \cdot d\gamma = \oint_{\partial \Sigma} \omega_{\mathbf{F}} = \int_{\Sigma} \text{d}\omega_{\mathbf{F}} = \int_{\Sigma} \omega_{\mathbf{F} \cdot \mathbb{n}} = \oint_{\gamma} (\mathbf{F}\cdot \mathbb{n})\cdot d\gamma \\ = \iiint_{V} (\mathbf{F}\cdot \mathbb{n}) \cdot dV
\end{equation}
$$

In the first two equalities, we used *Greenʻs Theorem* and from here, we used the fact that $\text{d}\omega_{\mathbf{F}} = \omega_{\mathbf{F} \cdot \mathbb{n}}$ due to divergence being the same regardless of *orientation* so long as we always have a *normal vector*. The last two equalities come from understanding that we are looking at *net divergence* over the surface $\Sigma$. This derives both *Stokes Theorem* and *Divergence Theorem*, as desired. $\blacksquare$

> These two proofs for the theorems are tributes for Madagascar for more ability to use Xenaʻs power!
