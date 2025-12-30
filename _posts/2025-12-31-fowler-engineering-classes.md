---
title: "Thoughts on software engineering classes at Chapman University"
layout: post
date: 2025.12.31
---

*This is part of a series detailing my experience at the [Fowler School of Engineering](https://www.chapman.edu/engineering/index.aspx) at Chapman University.*

From first entering the school, the way that classes were organized played an important role in shaping my foundational CS knowledge. My first class was an introduction to object-oriented programming (OOP) in Java. Others may have also taken this first, or taken the Python class before this one.

Even though this class seemed rudimentary at first, I've learned that there is always something to take away if you pay close enough attention. For me, I knew Java but not object-oriented programming; I knew how to trace the execution of a program, but not how to design one that was well thought out. Even with many questions surrounding object oriented programming ([Is it good? Is it bad?](https://alexanderdanilov.dev/en/articles/oop)), this class served its purpose as an introduction. Put another way: without taking this class, I would've been less informed on how to approach the OOP vs. functional programming (FP) discussion, in the first place.

The full introductory track is Python, followed by object-oriented programming, and data structures and algorithms. Beyond the introductory classes, several stood out to me in particular.

## Operating Systems

This class focuses on the theory of operating systems. Concepts were mostly applied in Linux, but there were a few discussions on Windows as well. We covered memory, threading, synchronization, I/O systems, and basics of computer architecture. **To give you a better idea of the contents, I found [my old cheatsheet](/assets/blog/2025-12-31-fowler-engineering-classes/cheatsheet.pdf) for the class's final exam.**

Programming assignments were written in C, covering concepts like threading, CPU scheduling, producers/consumers, and memory management.

For such a content heavy class, it was actually pretty engaging. We had a class quiz at the end of each chapter, which lacked the pressure of a regular quiz but still required students to know the content. Midterm reviews were Jeopardy-style while the final review was a twist on Who Wants To Be a Millionaire. I can't really think of a better way to teach what a mutex lock is, so props to professor Tom Springer.

## Algorithm Analysis

I took this class with professor Jonathan Weinberger. I would split this class into three parts: automata theory, Turing machines, and boolean satisfiability.

[Automata theory](https://en.wikipedia.org/wiki/Automata_theory) covered deterministic finite automata (DFAs) and their non-deterministic variant (NFAs). As someone who's touched game development a few times, it felt like learning the fundamentals of state machines. We learned how to break down a language into accepted and non-accepted words, how to categorize a language as regular, and applications of DFAs and NFAs. I was particularly interested in using NFAs for [pattern matching in regex engines](https://www.abstractsyntaxseed.com/blog/regex-engine/implementing-a-nfa), and to analyze race conditions.

The theory of [Turing machines](https://en.wikipedia.org/wiki/Turing_machine) added an extra dimension to state transitions: the *storage tape*. At this point I had a better understanding of why all programming languages share some similarities.

We didn't actually spend too much time on [boolean satisfiability](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem), but it was significant enough for me to count it as a major part. We were taught the basics of conjunctive normal form (CNF), and then left to develop a Sudoku solver as an assignment. This experience forced many of these abstract concepts to work together. I learned how to represent a Sudoku grid in CNF, and how to "pin" numbers using dynamic programming.

I have to say, this was the most difficult class I took at Chapman, and one where many concepts didn't make sense until the very end of the class. But, this class has helped my skills as well.

## Programming Languages

I took this class with professor Alexander Kurz. Concept-wise, I would split this class into rewriting theory, lambda calculus, and context-free grammars. There was more, but those were the concepts that predominantly lingered.

Rewriting theory covered the basics of abstract reduction systems (e.g. the [MU puzzle](https://en.wikipedia.org/wiki/MU_puzzle), the [Towers of Hanoi](https://en.wikipedia.org/wiki/Tower_of_Hanoi)) and how to represent these systems as trees. We learned what it meant for a system to be terminating and/or convergent, and what a normal form was.

[Lambda calculus](https://en.wikipedia.org/wiki/Lambda_calculus) was where the course really started to get serious. Being the simplest Turing-complete language, we learned that every program written in other Turing-complete languages could be theoretically reduced to this form. In this language, everything is a function, and "execution" is just rewriting theory applied through alpha-reduction and beta-reduction. [Even numbers are functions](https://en.wikipedia.org/wiki/Church_encoding).

[Context-free grammars (CFGs)](https://en.wikipedia.org/wiki/Context-free_grammar) were taught in the context of lambda calculus, but we actually first practiced it by developing a calculator (*not* in [Reverse Polish Notation](https://en.wikipedia.org/wiki/Reverse_Polish_notation), but parsing normal human-readable syntax). Key to this was the concept of **precedence**, the idea that multiplication should be grouped as a sub-expression compared to addition, and exponents being an even tighter group beyond that. For our final assignment, we lifted this calculator grammar definition (written using [Lark](https://lark-parser.readthedocs.io/en/latest/)) and put it into a fully-featured interpreter for lambda calculus.

I found it particularly interesting that lambda calculus was invented *before* modern computers, where it was originally a construct designed for math. In building an interpreter for it, I trained myself on how to work with ASTs, using classic techniques like DFS and backtracking in a new way. Each new syntax feature that was requested by the professor (including lists, variable declarations, and consecutive single-line statements) was a new avenue of potential bugs that could bring the interpreter to a halt. This is not to mention name substitution (alpha-reduction), which felt like a whole other problem space!

In the end, taking this class has made me interested in building an interpreter for a language written in a more modern style. So, in terms of getting me interested in this field, I think the class succeeded.

## Conclusion

I was generally satisfied with the engineering classes at Chapman. Some classes, like Operating Systems, covered the content to such a depth that I felt immediately comfortable in talking about the concepts and applications. Other classes, like Algorithm Analysis and Programming Languages, covered more breadth but still established the foundational building blocks for exploring each respective field further.
