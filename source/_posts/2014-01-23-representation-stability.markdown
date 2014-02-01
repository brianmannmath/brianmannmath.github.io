---
layout: post
title: "Representation Stability Part 1"
date: 2014-01-23 18:40:25 -0700
comments: true
published: true
categories: 
---

At the Joint Math Meetings in January 2014, I saw [Benson Farb][farb] give a talk about some very beautiful, very cutting-edge mathematics called *representation stability.* It's still very new (the [first paper][CF13] is from 2013), but it's a very powerful tool that should prove useful in both purely mathematical and applied settings (namely physics). 

Before I talk about respresentation stability, I should talk about the notion of *stability.* The word stability is used in many different settings, but I will define precisely what I mean here. 

### Stability

Let $X$ be a sequence of spaces 

$$X_0 \rightarrow X_1 \rightarrow X_2 \rightarrow \cdots$$

For our purposes, they will normally be groups or manifolds and the maps will be group homomorphisms (usually injective) or continuous maps. Any category will do though. Let's call the category where $X$ lives $\mathcal{C}$.

Let $F$ be a functor from $\mathcal{C}$ to another category $\mathcal{D}$. We say that $X$ is *stable* with respect to $F$ if, for some $n > 0$, we have $F(X_i) \cong F(X_{i+1})$ for all $i > n$. In other words, the maps in the sequence $F(X) = $

$$F(X_0) \rightarrow F(X_1) \rightarrow F(X_2) \rightarrow \cdots$$

are eventually isomorphisms. This is a very general concept, and there isn't much one can say about general stability (there are just too many categories and functors!). However, there are some very special functors that mathematicians care about. 

### Homology

Homology, in general, is an advanced topic more suited to a graduate course in algebraic topology. The wonderful thing about homology, though, is that while the technical details are opaque to those without the required background, one can give a fairly complete intuitive definition without too much pain and suffering. I'm writing this section for the reader who knows little-to-nothing about homology - if you've taken an algebraic topology course, feel free to skip it. 

#### Okay, so what it is?

(Very) roughly speaking, homology is a measurement of a toplogical space's inability to be collapsed to a point. Before I get into any details, let's look at some examples:

Consider $S^1$, the circle. I encourage the reader not to think about the circle as "living in" the the plane or any larger space, but to think about it as an object on its own. $S^1$ cannot be collapsed to a point - intuitively speaking, one cannot  deform $S^1$ to a point without cutting it somewhere (remember, $S^1$, is not living in the plane. It *is* true that one can collpase the circle in $\mathbb{R}^2$ to a point in $\mathbb{R}^2$). 

(Actually, for the industrious reader, if one thinks of $S^1$ at the unit interval $[0,1]$ with $0$ and $1$ identified, the result that $S^1$ is not homotopy equivalent to a point can be made precise using only freshman calculus!) 

Similarly, the 2-sphere $S^2$ cannot be deformed to a point. But if we look more closely, we see that the "holes" in these two spaces are different. Indeed, any 1-dimensional loop on $S^2$ *can* be deformed to a point, but nevertheless, there is still a "hole" in $S^2$ which prevents us from continuously deforming it to a point.

We need a way to measure these differences quantitatively; after all, this is mathematics! That's what homology does. 

The homology of a space $X$ is a collection of $\mathbb{Q}$-vector spaces $H_i(X,\mathbb{Q})$ for $$i = 0,1,2, \ldots$$. The $\mathbb{Q}$ isn't really important here; indeed, it's possible to replace $\mathbb{Q}$ with any other field or ring (in which case, you get a module instead of a vector space). But I assume most of my readers are comfortable with vector spaces at least, so we'll work over $\mathbb{Q}$. 

Furthermore, if $$f: X \rightarrow Y$$ is a continuous map, then it induces a linear map $$f_*: H_i(X,\mathbb{Q}) \rightarrow H_i(Y,\mathbb{Q})$$ for all $i$. In other words, each $H_i(--,\mathbb{Q})$ is a functor from the category of topological spaces to the category of vector spaces over $\mathbb{Q}$! The nice thing about this is that homology is an invariant: that is, if $X \cong Y$, then $$H_i(X,\mathbb{Q}) \cong H_i(Y,\mathbb{Q})$$. So, if we want to tell if two spaces are different, we can (in theory) compute their homology and see if they are different dimensions! 

Let's return to our examples to see what homology does. I haven't told you how one actually defines the vector spaces $H_i(X,\mathbb{Q})$ yet, so we can't do any computations, but I can tell you the answers.

For a point,

$$H_i(pt,\mathbb{Q}) = 0$$

for all $i$. For $$S^1$$,

$$H_1(S^1, \mathbb{Q}) = \mathbb{Q}$$

which tell us that $$S^1$$ cannot be deformed to a point. What about $S^2$? One can compute 

$$H_1(S^2,\mathbb{Q}) = 0$$

which tells us that $S^2$ cannot be deformed to $S^1$. Furthermore 

$$H_2(S^2,\mathbb{Q}) = \mathbb{Q}$$

so $S^2$ cannot be deformed to a point.  

### What about stability?

Remember, stability is a property of a sequence of spaces with respect to a functor, and now we have a handful of functors to play with! Let's go back to the original setting: a sequence $X =$

$$X_0 \rightarrow X_1 \rightarrow X_2 \rightarrow \cdots$$

of spaces. We say that $X$ is *homologically stable* if for every $i > 0$, $X$ is stable with respect to $H_i(-,\mathbb{Q})$. Note that the point at which the seqeunce

$$H_i(X_0,\mathbb{Q}) \rightarrow H_i(X_1, \mathbb{Q}) \rightarrow H_i(X_2, \mathbb{Q}) \rightarrow \cdots$$

stabilizes might depend on $i$.

### That's enough for one sitting. Next time?

In part 2, I want to discuss a motivating example where homological stability fails but "should" hold, and explain what respresentation stability is, and how it solves our problem.


[farb]: http://www.math.uchicago.edu/~farb/
[CF13]: http://arxiv.org/pdf/1008.1368.pdf