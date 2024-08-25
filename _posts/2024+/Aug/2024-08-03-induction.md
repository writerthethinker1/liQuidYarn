---
layout: post
title: "Mathematical Induction"
tags: proofs
preview: "I give the proof of why mathematical induction works as a valid proof technique."
contents: true
footnotes: false
published: true
---

# Mathematical Induction | Proof

---

In this paper, we prove the basic *notion* of *mathematical induction*. This is a *proof technique* for proving various theorems. The basic rules for mathematical induction are *base case*, *formalization*, and *induction*. So, we start with a *statement* call it $S(1)$ that begins the induction. We always need to show that it is true and demonstrate what it is. Next, we start the formalization which is when we take the *nth* statement $S(n)$ and show how it can lead to $S(n+1)$. We show that *if $S(n)$ is true, then $S(n+1)$ is true as well.* From here, we have *induction on $n$*, which means that $S(n)$ is surely true for all $n \in \mathbb{N}$, so all natural values of $n$. To prove this theorem of *mathematical induction*, we will assume the *base case* and *formalization* are correct. So, we know the first statement is *correct* which means $S(1)$ is right. We also know that if $S(n)$ is true, then $S(n+1)$ is true as well, meaning $S(n) \to S(n+1)$. Now, suppose that for some number $\alpha \in \mathbb{N}$ that $S(\alpha) \to S(\alpha + 1)$ doesnʻt hold true. By observation, we know $S(1) \to S(2)$ and then $S(2) \to S(3)$, so in whole by observation, $S(1)$, $S(2)$, and $S(3)$ are all true. We can keep chaining like this up to $\alpha$ and find out from *formalization* that $S(\alpha) \to S(\alpha + 1)$ is true as well. But, we assumed previously that $S(\alpha) \to S(\alpha + 1)$ isnʻt true for *some* $\alpha$. This is a contradiction, so we know by contradiction that $S(n)$ is true for all $n \in \mathbb{N}$ under the conditions for *mathematical induction*, as desired. $\blacksquare$   
