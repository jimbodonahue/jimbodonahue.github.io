---
title: "Bayesian vs Frequentist 2.0
"
# excerpt_separator: "<!--more-->"
categories:
  - Blog
  - Education
  - Statistics
tags:
  - data science
  - education
  - nerdy
---
 
# Where we left off

Last week I was busy ranting about how much easier it is to interpret Bayesian outputs, both for statisticians and normal people (understanding that "normal" is simply a setting on the washing machine). But that gets in front of a bigger, and often overlooked, question: what are these outputs about, anyway?

We are not nearly clear enough about explaining what a statistical model is. We give the linear regression formula  y = mx + b, or worse,  y = β0 + β1 x_1 + ... + βn x_n  without proper explanation. The problem with the latter is that it is not at all intuitive. A friend drove this point home after their recent trip to Greece, complaining about not understanding the signs in the Greek alphabet. My response? "You simply haven't done enough statistics!"

The point is that much of the notation is opaque, and statistics educators often fail to thoroughly describe conecpt of modeling. I have worked with students who could feed back definitions of mean and variance, parrot what basic tests to use with discrete or continuous data, and give a decent interpretation of the confidence interval. But when I asked them, "What does  β2  tell us?" they stared blankly. While this may seem laughable to those of use with advanced mathematics credits, I find it the single hardest, and most important, concept, possibly in all of statistics.

The failing is twice logical. First, there is the logical fallacy called the [curse of knoxledge](https://en.wikipedia.org/wiki/Curse_of_knowledge). This is where one forgets how hard it was to learn the things that they know. For myself, I probably understood the math behind the basic linear model in my 7th grade Algebra 1 course. This is not a flex, as it was a standard course for my middle school. It is simply to say that it has probably been 27 years since I struggled in connecting the math to the intuition. Those who did not grow up with the expectations to be math people may only be confronted with this when they take a college-level stats course.

This is no problem. Not all of us were born for economics degrees. The point is that we should be spending as much time teaching what a model is, and how to interpret it, as we spend trying to push these learners through tedious derivations of calculating OLS by hand (admittedly, I view this as a rite of passage). Whether you find your  β2  through frequentist methods or a Gibbs sampler, asking Whether it is significant is irrelevant if the student views the outcome simply as, "Did I pass?" rather than, "What does this variable say about my outcome?"

The further advantage of this thinking is that one can move on to the (also overlooked) idea of practical significance. For example, my model returned a  β2  of 4.5, with p = 0.0032. Is that significant? Statistically, very. Practically? If we are talking about annual income in dollars, no. If we are talking about years of life from a medical intervention, very. Critical to the distinction is a thorough understanding of what our model is.

A final thought: the most recent lecture I've seen which included a variance derivation was from MIT's [Dr. Gilbert Strang](https://ocw.mit.edu/courses/18-065-matrix-methods-in-data-analysis-signal-processing-and-machine-learning-spring-2018/resources/lecture-13-randomized-matrix-multiplication/). Teaching engineering students, he finds it necessary to go back to statistical basics, going as far as to define mean. If he takes the time to explain these rather simple operations ("simple" compared to the numerical eigenvalue calculations for large matrices from the previous lecture), I think we could spend more time on defining a model in statistics courses.




