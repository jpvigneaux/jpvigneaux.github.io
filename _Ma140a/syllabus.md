---
layout: page
title: Ma140a Probability - Syllabus
description: 
importance: 1
category: caltech
related_publications: 
toc:
  sidebar: left
---

## Introduction 

Probability theory provides a mathematically justified way of quantifying uncertainty. It was axiomatized by Kolmogorov in the 30s using measure theory, first introduced by Lebesgue, Borel, and others to formalize the process of integration within the framework of set theory (sets were a novelty then).  Hence "modern" probability theory, developed after Kolmogorov, is fundamentally set-theoretical (as much of XXth century mathematics) and in this course you'll surely develop new skills at manipulating sets. 

This course is not meant to be a first exposure to probability: that role is already played by Ma3 Introduction to Probability and Statistics. You can still get something out of it if you're new to the subject, but it will require some additional effort from your part. Moreover, Ma140a is meant to have a theoretical orientation; the Institute already offers courses in applied probability such as ACM116 Introduction to Probability Models, which emphasizes "probabilistic thinking" and an "intuitive feel" rather than measure-theoretic proofs. 

Our course will have three modules: 

1. Measure-theoretic foundations of probability theory: a set-theoretic interpretation of terms such as event, random variable, probability, and expectation. Construction of conditional probability and expectation.

2. Limit laws of randomness (Law of Large Numbers, Central Limit Theorem, Large Deviations...) and some nonasymptotic concentration inequalities. The limit laws are deterministic regularities that appear when combining (e.g. adding) an arbitrarily big number of random variables; the nonasymptotic effects are quantified by concentration inequalities. 

3. Stochastic processes (random walks, martingales, branching processes, Markov chains, stationary processes). These model random variables that evolve over time under certain constraints. 

There is overlap between this course and ACM117 Probability Theory and Computational Mathematics (which is also a rigorous introduction to probability theory), especially concerning the measure theoretic foundations. But things get different concerning points 2 and 3 above; notably, limit laws and stochastic processes are absent in ACM117. 

The course will be reasonably self-contained but requires previous exposure to rigorous mathematical proofs and familiarity with modern analysis (at least with the so-called "naïve" set theory. and with the formal definitions of limits of sequences and functions). Previous knowledge of Lebesgue integration, as taught in Ma 108b, is desirable but not necessary. That said, the course will feel fast paced during the first three or four weeks if you are not already familiar with measure theory; in this case, some extra effort will be required form your part. 

## Methodology: Guiding principles

Concerning methodology, I want to make explicit some guiding principles behind the design of this course:

A. Active learning generates better learning outcomes than passive learning (please see: https://www.pnas.org/doi/10.1073/pnas.1821936116Links to an external site.). Hence this course won't be based solely on lectures, but also on discussions and collaborative problem solving. 

B. Grades have detrimental effect on several aspects of learning: creative thinking, long-term retention, interest in learning, and preference for challenging tasks (see https://www.alfiekohn.org/article/risks-rewards/Links to an external site., https://www.alfiekohn.org/article/case-grades/Links to an external site. and references there). I want to minimize the role of grading in this course. Weekly, you'll keep track of your work, submit solutions to exercises, and give feedback on other students' solutions. None of this will be graded, but Jiaxin, our TA, is going to give feedback. At the end of the course, you'll gather all your work in a portfolio, reflect on what you did and the ways feedback affected your learning, and grade yourself accordingly. During the first week, we shall define together the standards for pass/fail and for each letter grade. (Remark that you have the choice of going for letter or pass/fail.) 

C. Autonomy and freedom are key for intrinsic motivation. In this course, you'll have to think about:

* Your own learning goals
* The sources are the most helpful to you
* The problems are more interesting, appealing or challenging, according to your own level.


 The structure within which these decisions are taken is provided by the me, teacher. I have some expert knowledge in the subject (although I don't have all the answers!) and more experience with pedagogy, hence I am well placed to:

* Propose broad learning goals (a starting point for your own)
* Propose a feasible path towards the learning goals
* Summarize and present the main results of the theory
* Guide collective discussions or attempts to solve problems
* Give personalized feedback

However, you remain responsible of your own learning.

## Learning Outcomes
Upon successful completion of this course, I hope you'll be able to:

* Use the basic probabilistic concepts—mainly event, random variable, probability, expectation, density, variance, and independence—precisely and effectively both in mathematical and real-world applications. 
* Manipulate conditional expectations with ease. 
* Recognize the main asymptotic results in probability theory and be able to apply them in mathematical proofs and problem-solving. 
* Recognize some basic stochastic models, list their basic properties, and solve related problems requiring integration of several properties and techniques. 

Moreover, the course should improve your skills at

* Working in groups to solve problems effectively or refine previous solutions.  
* Writing mathematical arguments clearly; in particular, assimilate the conventions of the probabilistic literature.  

During the first week, you'll reflect on how these goals align with your own, and adjust them accordingly. 

 

## References

The main topics of this course are very classic and well represented in many textbooks. You're invited to find your favorite reference. I will be following 

[W] David Williams, Probability with Martingales, Cambridge University Press, 1991. 

[T] Omer Tamuz's notes, available at http://tamuz.caltech.edu/teaching/ma144a/lectures.pdfLinks to an external site.

[GS] Geoffrey Grimmett and David Stirzaker, Probability and Random Processes, Oxford University Press, 2001 (third edition). 

Williams is extremely good at making technical arguments accessible (it’s no coincidence that the book has been reprinted 25 times!). It reviews the parts of measure theory that are most useful for the course and develops in detail the theory of martingales.

Concerning the measure-theoretic foundations of probability theory and the theory of martingales, Omer's notes are an abridged version of Williams' book. (But freely available online.) I expect to follow part of his treatment of stationary processes and random walks too. 

Grimmett and Stirzaker's book avoids most measure-theoretic technicalities, but is extremely rich in examples and applications. It’ll be my main reference for generating functions and stochastic processes, including Markov chains.

The books can be found in the library and have been reserved for this course. [GS] can be found online with a Google search. I have requested a virtual copy of [W] via Course Reserve (request still being processed). Since there are not so many copies available, buying Williams' and/or Grimmett and Stirzaker's books might be a good idea, but this is not mandatory.

Most of the measure theory needed in this course is summarized in Williams’ book; for more details and explanations one must consult a textbook on the subject. My personal favorite is  

Donald L. Cohn, Measure Theory, Birkhäuser, 2013 (second edition), 

but for the most general and lean statements one might use

E. Hewitt, and K. Stromberg,  Real and Abstract Analysis: A modern treatment of the theory of functions of a real variable. Springer Berlin Heidelberg, 1965. 

 

## Coursework 

The first week, you complete Assignment 1. 

On weeks 2 to 10, you upload:

* A weekly report including:
    * Time spent on the course.
    * A brief description of the way that time was spent.
    * Answers to a short questionnaire whose purpose is to motivate a reflection and evaluation of your own learning.
* The solution of the two most challenging problems you solved that week (I'll propose several and  you can choose your own).

There will be a dedicated assignment for each submission. The deadline for both documents is Sunday, 23:59. There’s no expectation of working until then! You upload your documents whenever you’re done with that week’s work. No late submissions accepted.

Over Monday-Wednesday, you give feedback on your peers’ work and the TA gives feedback too. We shall discuss in class the aspects that are important in feedback and the best way of giving feedback.

 
## Grading
At the end of the term, you collect all your written submissions, summarize your participation in class and on Ed Discussion, reflect on your improvements in relation with your learning goals, and give yourself a grade (according to standards we’ll discuss together).

As a teacher, I reserve the right to decide a “breach of contract” (failure to meet minimum criteria to pass the course—to be discussed), or to dissent with your judgement (in which case we'll talk and reach an agreement). But I don't expect this will happen. 

Attendance to lectures is optional and not graded. However, the attendance to the collaborative problem-solving sessions should factor into the final grade. The exact criteria for this will be defined in class. 

That said, I encourage you to attend the lectures and participate actively in class: I'm trying to put students needs at the center of the process and for this interactions and feedback need to happen. 

 

## Collaboration Policy
Full discussion of problems and their solutions is allowed. This includes talking about the concepts relevant to the problem, as well as the details of the solution. And you can consult any reference you want. 

That said, you should write down your own version of the solution, and explicitly cite your collaborators and sources (if this applies).  As a guideline for the collaboration policy, you should be able to reproduce any solution you hand in without help from anyone else and without consulting external sources.

 

## Academic Integrity
Caltech’s Honor Code: “No member of the Caltech community shall take unfair advantage of any other member of the Caltech community.”

Understanding and Avoiding Plagiarism: Plagiarism is the appropriation of another person's ideas, processes, results, or words without giving appropriate credit, and it violates the honor code in a fundamental way. You can find more information at: http://writing.caltech.edu/resources/plagiarism. 

All instances of plagiarism or other academic misconduct will be referred to the Board of Control for undergraduates. For graduate students, contact the Graduate Office

