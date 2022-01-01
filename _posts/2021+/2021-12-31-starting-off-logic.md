---
layout: post
title:  "Starting Off! Quantum Ideas..."
date: "2021-12-31"
tags: Qlogic
preview: "Some cool logical ideas and basic relation to ideas taken from quantum mechanics. Read on!"
footnotes: false
contents: true
published: true
---

# Beginning Quantum Logic...

Hello and welcome to **calm, happy, and peaceful quantum computing!** We hope you're relaxed and comfortable. We're going to be talking about other ways to approach old logical settings all from using ideas used in quantum mechanics. So-called *quantum logic*. Rather than start with the basics and give you notation, how to write statements, and truths, we're going to embed them all in this article. There's a separate article for the notation, so if you're stuck, give it a read! This page will be right here waiting...Let's go!

## First lesson: $(\vec{\varphi} \oplus \circ\vec{\varphi})$ the sentence "p or not p"

For any proposition $\vec{\varphi}$ we write

$$
\vec{\varphi} = \pmatrix{\alpha \\ \beta}
$$

where $\alpha, \beta$ are complex numbers. To find the truth of $\vec{\varphi}$ take the norm of $\alpha$. The probability amplitude is 1 by constraint, so we assume $\vec{\varphi}$ always happens, whatever it is. For now, just look at the numbers like they are *chances* of an event happening; the top one is the square root of the chance it happens and the bottom one is the square root of the chance it doesn't happen. So you can think of a proposition written as

$$
\vec{\alpha} = \pmatrix{\sqrt{0.7} \\ \sqrt{0.3}} = \text{roll 3}
$$

As there is a 70% chance to roll a 3 and a 30% chance you won't roll a 3. Later, we'll explain what the complex numbers mean and how to navigate yourself on the sphere using them. Just focus on the basics for now.

## Measurement

What makes us know if $\vec{\varphi}$ happens? *Measurement*, or the $m(\cdot)$ operator. For example, we write:

$$
m\left(\vec{\varphi}\right) = \pmatrix{1 \\ 0}
$$

to show that $\vec{\varphi}$ did happen and we know so. When we measure, we can get only 1 of two things:

$$
m(\cdot) = \pmatrix{1 \\ 0 } \text{ or } \pmatrix{0 \\ 1}
$$

and never both. The first one with the 1 on top means that the event happened and the second one means that the event didn't happen.

## NOT

In classical probability for disjoint events $p$ and $\neg p$, we write:

$$
\mathbb{P}(p \lor \neg p) = \mathbb{P}(p) + \mathbb{P}(\neg p) = 1
$$

All that is true given the assumptions there. We don't do that here. First, we introduce the basic **NOT** or $\circ$ operator:

$$
\circ = \pmatrix{0 & 1 \\ 1 & 0}
$$

*It just flips the top and bottom entries; that's all it does.* This means we are *inverting* the probabilities, so how much we think something happens is now how much we think it won't happen and vice versa. If we want to write "not p" we write $\circ \vec{\varphi}$ to say our mind's beliefs about the opposite of $\vec{\varphi}$.

To write the sentence 'p or not p' we write $\vec{\varphi} \oplus \circ\vec{\varphi}$ using the $\oplus$ logical symbol for 'or' the operation 'or' is defined using Euler notation $\alpha = r_1e^{i\theta}$ $\gamma = r_2e^{i\theta_2}$ a basic or operator takes the average of the real entries and the angles. It gives us $\alpha \oplus \gamma = \bar{r}e^{i\bar{\theta}}$ For vectors it is slightly modified but more later in this work. The key idea is *mixture*, since we don't know the real truth of a proposition (no measurement) we have to mix the worlds together and then normalize to keep the new proposition in the sphere. If you notice:

$$
\vec{\psi} = \vec{\varphi} \oplus \circ\vec{\varphi}
$$

Which means that the statement 'p or not p' is another one. This is enough to give an idea about the $\oplus$ operation. The key part needed to understand is that when we do vector probability $\vec{\mathbb{P}}(\cdot)$ the statement

$$
\left(\vec{\varphi} \oplus \circ \vec{\varphi}\right) \neq \pmatrix{1 \\ 0}
$$

When things evaluate to $$\pmatrix{1 \\ 0}$$ it means certainty, which we can't have because *we never measured the proposition*. It's a lot like opening a box, measuring. When we don't know, we can't have $$\pmatrix{1 \\ 0}$$. Instead, we have:

$$
\left(\vec{\varphi} \oplus \circ \vec{\varphi}\right) = \pmatrix{\sqrt{0.5}e^{i\bar{\theta}} \\ \sqrt{0.5}e^{i\bar{\eta}}}
$$

which always *lands us in the middle of the sphere, somewhere*. Later, we'll see how the orientation is about our minds. But for now the important part is that we are 50% certain about 'p or not p' happening regardless of the orientation and 'not p or p' happening 50% as well. Remember, we never measured, so we can't be 100% certain, we know about $\|\|\vec{\psi}\|\| = 1$ which is that we can know either $\vec{\varphi}$ or $\circ \vec{\varphi}$ happening, the box will be lifted and then you'll know. Right now, it's not, so we give a fair chance of both cases: the top part of the vector means 50% of the worlds in the mind have $\vec{\varphi}$ true and $\circ \vec{\varphi}$ as true as well. We are in between both of them being true but certain 1 will be. That's what happens.

> 50% about it being in there or not and 50% about it not being there or not though. We color the case on top blue and bottom red. Then we reorient the chance for $\circ \vec{\varphi}$ and average them.

If you can wrap your mind around that, you're one step closer to understanding more about quantum logic.

## Note on measuring 'p or not p'

When we measure $\left(\vec{\varphi} \oplus \circ \vec{\varphi}\right)$ we have *both* the following as valid:

$$
m\left(\vec{\varphi} \oplus \circ \vec{\varphi}\right) = \pmatrix{1 \\ 0}
$$

$$
m\left(\vec{\varphi} \oplus \circ \vec{\varphi}\right) = \pmatrix{0 \\ 1}
$$

which is fine because it still means 'either p or not p' happened. Both top and bottom mean the same thing, only the top means 'p or not p' happened and the bottom means 'not p or p' happened! Nothing too terrible happened. So, the thing was definitely either in or not in the box, regardless of which vector we have. *Only 1 of $\vec{\top}$* or $\vec{\bot}$ is observed however. This is just for the special case we have here $\left(\vec{\varphi} \oplus \circ \vec{\varphi}\right)$. When we have different propositions, it's not like this, and there's only 1 vector at the end. For this one, things are special. That's about it. Welcome to quantum logic. Be in zen and temporarily remove what you know about classical logic. It'll all be there when you want. We will compare and contrast old theorems as we go. Right now, we learned

$$
(p \lor \neg p) = 1
$$

in classical and

$$
\left(\vec{\varphi} \oplus \circ \vec{\varphi}\right) = \pmatrix{\sqrt{0.5}e^{i\bar{\theta}} \\ \sqrt{0.5}e^{i\bar{\eta}}}
$$

in quantum.

## OR in a General Setting

OR in general has a different interpretation for things like $\vec{\varphi} \oplus \vec{\chi}$. Given

$$
\vec{\varphi} = \pmatrix{\alpha \\ \beta} \qquad \vec{\chi} = \pmatrix{\gamma \\ \delta}
$$

the statement

$$
(\vec{\varphi} \oplus \vec{\chi}) = \pmatrix{\eta \\ \zeta}
$$

we mean that either $\vec{\varphi}$ or $\vec{\chi}$ are true with chance $\|\eta\|$ but we don't know which one and that either $\vec{\varphi}$ or $\vec{\chi}$ are false with chance $\|\zeta\|$ but we don't know which one. Notice the norm of $\vec{\varphi} \oplus \vec{\chi}$ is always $1$. This means that we are certain of either $\vec{\varphi}$ being true or false or $\vec{\chi}$ being true or false (observed). When

$$
m(\vec{\varphi} \oplus \vec{\chi}) = \pmatrix{1 \\ 0}
$$

it means that either the first proposition was true or the second, but we don't know which one or both even (not to awareness of both though). When

$$
m(\vec{\varphi} \oplus \vec{\chi}) = \pmatrix{0 \\ 1}
$$

it means that either the first or the second was false but we don't know which one. We speak of only 1 proposition for sufficiency. Both could have been false but we don't need (nor do we know) that information to have the measure be $$\pmatrix{0 \\ 1}$$. Just 1. When we speak jointly of outcomes, that's where AND or $\otimes$ comes into play. Just know that we'll never know both jointly right now. That's lesson 2!

## Review: tensor products

For any two vectors $\vec{\alpha} = \pmatrix{\alpha_0 & \alpha_1}'$ and $\vec{\beta}= \pmatrix{\beta_0 & \beta_1}'$ the tensor product between them is noted as

$$
\vec{\alpha} \otimes \vec{\beta} = \pmatrix{\alpha_0 \beta_0 \\ \alpha_0 \beta_1 \\ \alpha_1 \beta_0 \\ \alpha_1 \beta_1}
$$

Or in vector element notation: $(\alpha\beta)_{ij} = \alpha_i \beta_j$. Here we reference tensor product elements as $(\alpha\beta)\_{ij}$ all for the elements, if we had more, we write $(\alpha\beta\gamma)\_{ijk}$. These aren't matrices but they are handy to reference elements when we want to. That's basic tensor products. Let's compute 1 just to have a numerical answer:

$$
\vec{\alpha} = \pmatrix{1 \\ 4} \qquad \vec{\beta} = \pmatrix{3 \\ 8}
$$

Then, the tensor product is:

$$
\begin{align}\vec{\alpha} \otimes \vec{\beta} &= \pmatrix{1(3) \\ 1(8) \\ 4(3) \\ 4(8)}
\\ &= \pmatrix{3 \\ 8 \\ 12 \\ 32}
\end{align}
$$

## Lesson 2: $(\vec{\varphi} \otimes \circ\vec{\varphi})$ or AND

The statement 'p and not p' in classical logic is given as $(p \land \neg p)$ and is always false. Or

$$
(p \land \neg p) = 0
$$

In quantum logic, we will proceed by computation and explain the reasoning as we go. Suppose

$$
\vec{\varphi} = \pmatrix{\varphi_0 \\ \varphi_1} \qquad \circ \vec{\varphi} = \pmatrix{\varphi_1 \\ \varphi_0}
$$

The first vector is about the truth of some outcome and the second is about it being false. When the second is true, the first is false.

By direct computation we arrive at for the tensor

$$
(\vec{\varphi} \otimes \circ \vec{\varphi}) = \pmatrix{\varphi_0\varphi_1 \\ \varphi_0\varphi_0 \\ \varphi_1\varphi_1 \\ \varphi_1\varphi_0}
$$

Clearly, only one outcome is true, right? The box either has the item or it doesn't but no one has opened it. What we talk about when we say 'p and not p' in the first element is both p and not p being true. That can't happen right? Well, in some cases it can! Same with not p and p being true. As well as p true and not p false and p false and not p true. All 4 are valid in some cases. Let's have a story to show 'p and not p' as true.

> It's about the day. $\vec{\varphi} = \text{morning}$ and $\circ \vec{\varphi} = \text{evening}$. Knowledge of one means the opposite is false, if morning, then evening. If evening then not morning. But, what happens if we observe during 12:00? Are we 'wrong'? No, it's both morning and evening. Morning and evening is different that evening and morning in order, but in observation and chance they are the same. In the above statement, the first and last elements are morning and evening. The first element is 'morning and evening' and the second one is 'evening and morning'. Think of mentally observing one after the other. The middle 2 are when we observe during day (the second one) the night (the third one).

Now, when we measure we end up with 1 of 4 for the joint knowledge:

$$
m(\vec{\varphi} \otimes \circ\vec{\varphi}) = \pmatrix{1 \\ 0 \\ 0 \\ 0} \text{or} \pmatrix{0 \\ 1 \\ 0 \\ 0} \text{or} \pmatrix{0 \\ 0 \\ 1 \\ 0} \text{or} \pmatrix{0 \\ 0 \\ 0 \\ 1}
$$

only 1 world is valid and we have *joint knowledge*. The middle two mean 'it's morning and not night' and 'it's night and not morning'. The top and bottom mean 'it's morning and night' and 'it's night and morning'. For this special proposition we have the rule:

$$
m(\vec{\varphi}) \otimes m(\circ\vec{\varphi}) \neq m(\vec{\varphi} \otimes \circ\vec{\varphi})
$$

As soon as we measure *a priori* the cases are as follows:

$$
m(\vec{\varphi}) \otimes m(\circ\vec{\varphi}) = \pmatrix{0 \\ 1 \\ 0 \\ 0}
$$

or

$$
m(\vec{\varphi}) \otimes m(\circ\vec{\varphi}) = \pmatrix{0 \\ 0 \\ 1 \\ 0}
$$

Only those 2 are present when we measure a priori. It's in line a little with classical logic since it makes $\vec{\varphi}$ and $\circ \vec{\varphi}$ disjoint or mutually exclusive.

That's lesson 2, $\otimes$ or 'AND'.

In classical:

$$
(p \land \neg p) = 0
$$

and it doesn't happen at all.

In quantum,

$$
(\vec{\varphi} \otimes \circ \vec{\varphi}) = \pmatrix{\varphi_0\varphi_1 \\ \varphi_0\varphi_0 \\ \varphi_1\varphi_1 \\ \varphi_1\varphi_0}
$$

and is a valid idea. All different ways of seeing 'p and not p'.

## AND in a General Setting

In general for any two propositions about two different outcomes $\vec{\varphi}$ and $\vec{\chi}$ written as

$$
\vec{\varphi} = \pmatrix{\varphi_0 \\ \varphi_1} \qquad \vec{\chi} = \pmatrix{\chi_0 \\ \chi_1}
$$

The tensor reveals the truth about which way things worked out *jointly*. *Was $\vec{\varphi}$ true and what about $\vec{\chi}$?* It tells us '$\vec{\varphi}$ was .. and $\vec{\chi}$ was ..' where the '..' is the truth state or just truth (happened vs. didn't happen). Let's find the tensor:

$$
(\vec{\varphi} \otimes \vec{\chi}) = \pmatrix{\varphi_0 \chi_0 \\ \varphi_0\chi_1 \\ \varphi_1 \chi_0 \\ \varphi_1\chi_1}
$$

The probabilities above are about $\top\top$, $\top\bot$, $\bot \top$, and $\bot \bot$. Only one will be $1$ when we measure. And when it is, we know jointly what happened in both worlds: whatever $\vec{\varphi}$ was talking about and $\vec{\chi}$ was talking about. Assuming both $\vec{\varphi}$ and $\vec{\chi}$ are independent, we have:

$$
m(\vec{\varphi}) \otimes m(\vec{\chi}) = m(\vec{\varphi} \otimes \vec{\chi})
$$

Just make sure to check. If not, then we don't always have the above.

# Wrapping up

That's about it for the basics of quantum logic or q-logic. You learned $\oplus$, $\circ$, and $\otimes$, the quantum ways of seeing 'OR', 'NOT', and 'AND' as well as measurement $m$. If you got through these pages, the rest of the cool things will follow. Take some time and carefully validate things for yourself or with others! Enjoy the day! Meditate and achieve bliss.

{% include signature.html %}
