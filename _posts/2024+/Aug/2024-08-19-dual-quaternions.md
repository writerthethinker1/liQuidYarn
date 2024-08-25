---
layout: post
title: "Dual Quaternions"
tags: proofs
preview: "I give proofs and outline the theory for dual quaternions so we can use them for complex motion of Xenaʻs powers."
contents: true
footnotes: false
published: true
---

# Dual Quaternions

---

In this paper, we talk about *dual quaternions*, what they are, and how we can use them to quickly describe *complex motion of Xenaʻs powers.* A dual quaternion is an *ordered pair* $(A, B)$ such that $A, B \in \mathbb{H}$ meaning that both $A$ and $B$ are quaternions. We represent them algebraically as...

$$
\hat{A} = (A, B) \equiv A + \epsilon B
$$

where $\epsilon$ is an *infinitesimal number* such that $\epsilon^2 = 0$. We are here restricting the root we take of $\epsilon$ as *positive*. We will now define *addition* and *multiplication* over these special types of numbers. We canʻt define *division* for them since this implies some form of *dividing by zero*, which isnʻt *well formed*. Hereʻs what addition looks like when we use plain algebra...

$$
\hat{A} + \hat{C} = (A + \epsilon B) + (C + \epsilon D) \\ = A + C + \epsilon(B + D) \\ \equiv (A + C, B + D)
$$

Now, we will define *multiplication* for *dual quaternions* using plain algebra...

$$
\hat{A} \cdot \hat{C} = (A + \epsilon B)(C + \epsilon D) \\ = (AC + \epsilon AD + \epsilon BC + \epsilon^2BD) \\ = (AC + \epsilon(AD + BC)) \\ \equiv (AC, AD+BC)
$$

The last thing we will do is represent them in *polar form*...

$$
\hat{A} = (A, B) = a_0 + a_1i + a_2j + a_3k + \epsilon(b_0 + b_1i + b_2j + b_3k)\\ = ||A|| e^{\hat{n}\varphi_0} + \epsilon||B||e^{\hat{n}\varphi_1} \\ = ||A|| e^{\hat{n}\varphi_0} + ||B||\epsilon e^{\hat{n}\varphi_1}
$$

This is all as desired. $\blacksquare$
