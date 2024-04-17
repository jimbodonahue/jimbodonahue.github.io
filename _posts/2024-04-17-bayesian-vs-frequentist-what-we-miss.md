---
title: "Bayesian vs Frequentist: what we (often) miss?"
# excerpt_separator: "<!--more-->"
categories:
  - Blog
  - Meta
tags:
  - data science
  - education
---

# Bayesian vs Frequentist: what we (often) miss?

After a semester of coaching a friend through their stats course for a non-mathy degree, I found myself in the tired position of explaining again what a confidence interval means. At some point, I realized that my friend was just looking for, "Is it significant™?" Really, the underlying question was, "What number can I find to make my teacher not yell at me?"

Of course, this question is not specific to teachers. It could be coworkers, managers, or even customers who are demanding the idea of statistical significance. And even if you find it, you wither risk getting called out for p-hacking or present some Bayesian posterior which confuses most audiences. I know what you're thinking: do I a better way?

Honestly, not really. In an academic framework, we are stuck in the Fisherian world of confidence intervals, at least for now. The data science world is quickly converting to Bayesian, but their methods (and interests) are almost purely applied. However, I want to take a step back and ask a more meta question: what is the "it" we are looking for when we ask if "it" is significant?

This points to the often under-loved idea of a model, and an anecdote about another friend. For their computer science program, the data analytics module's exam included calculating a least squares model by hand, including variance, for about ten data points. While I think this should be a rite of passage for anyone using OLS, it has no place on a timed exam (particularly with so many numbers). My conclusion: this well-meaning teacher was too focused on the cookbook method of calculations and had lost focus on teaching a model.

Understanding the model is important for two reasons. First, explicitly writing out the model gives an idea of how the variables interact. When one is more mathematically inclined, they can intuit the implications of nonlinearities, such as exponential or power functions. However, anyone should be able to look at a linear model $$ y = \beta x + \epsilon $$ and interpret the coefficients. I would much prefer a colleague who blindly relies on SPSS or Python to provide stars for significance levels but can quickly explain the model.

This is arguably even more important for the Bayesian, who comes back with a number of posterior distributions or credible intervals. The advantage of Bayesian analysis is that it gives a posterior per parameter, each of which is a proper probability distribution. The disadvantage is that, even for a relatively basic linear model, this is a lot of information. For the layperson, having an explicit model gives these some context, a place to plug in the most salient outcomes.

As this is already longer than expected, I will continue next week with what I consider the key points of model interpretation. Dear reader, I look forward to seeing you then!
