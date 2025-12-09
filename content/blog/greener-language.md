---
published: true
title: 'Is there a greener programming language?'
description: "There should be a programming language more suitable to the environment, right?"
date: '2022-09-09'
disclaimer: false
---

## Computers and energy

Computers are general-purpose hardware — therefore they are not the most efficient way to perform certain tasks. By definition, using FPGAs or building specific hardware for a given operation will almost always be more efficient than running code for that operation on a general-purpose CPU.
## How to measure how much energy a programming language consumes?

Well, in the attempt to measure it, researchers from the *Universidade do Minho* wrote this <a target="_blank" rel="noopener" href="https://repositorium.sdum.uminho.pt/bitstream/1822/69044/1/paper.pdf">article</a>. 

To summarize it, they basically run lot's of different algorithms in various programming language. And of course, I really encourage you to read the <a target="_blank" rel="noopener" href="https://repositorium.sdum.uminho.pt/bitstream/1822/69044/1/paper.pdf">article</a> and see the actual methodology.

Here is what they found:

![image](/images/ple.png)

I saw a lot of people talking about this - awesome - research, which is pretty cool. But they were using it to show that some programming languages are greener than others, which is just wrong.

I've seen a lot of people citing this — great research — to claim some languages are greener than others. That's an oversimplification.

1. We can always change compilers and runtimes to be more efficient, so it's hard to attribute energy use to the language alone. OK, that's me being pedantic.
2. Is the faster one also the most energy-efficient? Well... *Energy = Time × Power*. This suggests energy will decrease if execution time decreases, but only if power remains constant. Power can vary between runtimes, compilers, and hardware. The paper highlights C as among the most efficient languages in their tests, but that doesn't always mean it's the fastest in every scenario.
3. Hardware. Results may vary depending on the hardware, OS, middleware, drivers, and so on. It's tricky to point to a single "greener" language because a language is only one part of the whole system.

What would be the environmental impact of rewriting every application in C? It could be huge — and it's hard to predict.
4. Erlang uses concurrency by design. That language/runtime design made it resilient and practical for telecom applications in the 1980s. Even if both Erlang and C are fully optimized, reimplementing the same resilient applications in C might not yield the same results.

We can use this paper to inform our choices, but we should be careful not to oversimplify the conclusions or reinvent the wheel every time. The study is nuanced and shouldn't be reduced to "let's use C because it's the most efficient." Drawing that single conclusion would be misleading.

In short: there is no single "greener" programming language. Energy use depends on algorithms, compiler and runtime behavior, hardware, and system design. When energy matters, measure the whole stack, choose the right tool for the job, and prioritize algorithmic efficiency and appropriate hardware.

---

Talk soon,

Victor Fulgêncio


