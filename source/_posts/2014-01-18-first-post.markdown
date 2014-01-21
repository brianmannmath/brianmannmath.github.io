---
layout: post
title: "Who am I?"
date: 2014-01-18 14:41:34 -0700
comments: true
categories: 
---

My name is Brian Mann, and I'm a mathematician turned programmer/computer scientist.

Currently, I'm a doctoral student that the University of Utah doing research in the field of [geometric group theory][ggt] under the advisement of [Mladen Bestvina][mladen]. Specifically, I study the outer automorphism group of finite rank free groups, and also the dynamics of group actions on $\mathbb{R} \mbox{-trees}$. I've written/co-authored two papers: [Hyperbolicity of the Cyclic Splitting Complex][splittingcomplex] and [Constructing Non-uniquely Ergodic Arational Trees][NUE]. (*A word of warning: these papers are not for beginners. They require basic knowledge about standard tools in geometric group theory, especially [Bass-Serre Theory][BST]. I will likely talk more about the background required in later posts.*)

For an overview of what I've been thinking about recently, you might want to look at slides from a recent [talk][JMM] I gave at the Joint Math Meetings.

I love mathematics. But for various reasons (which I will likely write about in the future) I have decided not to pursue a career in academics. I also love computers. I've always been fascinated by them and enjoyed all of the little coding projects I've needed to do in my career as a mathematician, but have never had time to *really* learn to code. Now that I'm graduating, I've decided to change that. I'm teaching myself Python, R, Haskell, and C++ and trying to get a job in the Seattle area which uses my mathmematical knowledge/skills to computer-related applications (data science, crytpography, software development, etc...).

This blog is mainly to document my transformation from pure mathematician to a hybrid mathematician/computer-scientist/programmer. Although I am currently focusing on learning Python and R (which I feel will be most useful in my job hunt), I'm hoping to post a lot about Haskell. Which brings me to my next point...

####I fucking love Haskell.

Look at this:
{% codeblock lang:hs %}
fibs = 1:1:zipWith (+) fibs (tail fibs)
{% endcodeblock %}

I won't lie and say this line of code made me fall in love with Haskell, because that's not true. But it's certainly one of the most beautiful lines of code I've ever seen. I fell in love with Haskell when a good friend (a hacker-turned-algebraic geometer-turned-computer security expert) told me about it. A language based on category theory, you say? Yes please. 

Let me explain. I know *a lot* of category theory. I spent much of my undergrad at the University of Michigan taking graduate level math classes in algebraic geometry. And algebraic geometers *love* category theory. Why? Because it's an *incredibly expressive language* which allows mathematicians to phrase difficult questions in simple, elegant terms. Sound familiar?

When I learned about Haskell, I didn't know much about programming. But I knew enough to guess at the expressive power of a language based on categorical ideas. At the time, I poked around [Learn you a Haskell][lyah] a bit, but never made any real progress; as an undergraduate taking graduate level mathematics and who was *sure* he wanted to go into academics, the only real motivation I had to learn Haskell was curiousity. Now I have quite a bit more. 

I love Haskell for the same reason I love mathematics. It's beautiful. Expressive. Powerful. Working in Haskell teaches me to think in different ways about programming. And perhaps one of the reasons I like it so much is because it's so *familiar*. It feels like mathematics, because it is mathematics.

Anecdote: I was curious about what a monad was, so naturally I went to [the wikipedia page][monad]. Admittedly, I was confused. Programmers think about things a little differently than mathematicians. So I went to [this wikipedia page][monadcat] and learned what a monad was in category theory. And everything made sense. 

#### So what's this blog for anyways?

My goal here is simple. I want to tell people about cool things I've learned and am learning. I want people to know that high-level mathematics isn't scary. It's beautiful and fun, just like Haskell. I want people to be curious and ask questions about what I post. I want to force myself to explain things in simple terms so I understand them better myself.








[ggt]: http://en.wikipedia.org/wiki/Geometric_group_theory
[mladen]: http://en.wikipedia.org/wiki/Mladen_Bestvina
[NUE]: http://arxiv.org/abs/1311.1771
[splittingcomplex]: http://arxiv.org/abs/1212.2986
[BST]: http://en.wikipedia.org/wiki/Bass-Serre
[JMM]:https://github.com/brianmannmath/JointMathMeetings/blob/master/JMM_talk.pdf
[lyah]: http://learnyouahaskell.com/
[monad]: http://en.wikipedia.org/wiki/Monad_(functional_programming)
[monadcat]: http://en.wikipedia.org/wiki/Monad_(category_theory)