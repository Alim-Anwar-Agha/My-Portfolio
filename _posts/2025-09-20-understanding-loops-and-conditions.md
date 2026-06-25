---
layout: post
title: "When Code Started Making Sense: Loops and Conditions"
date: 2025-09-20
author: "Alim Anwar"
categories: [PF]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, ProgrammingFundamentals, Loops, Conditions, CPlusPlus]
read_time: 5
excerpt: "Loops and conditions were the moment programming stopped feeling like typing and started feeling like actual thinking. Here is how that shift happened for me."
---

There is a specific moment in every programmer's early life when the subject stops feeling like a foreign language and starts feeling like a tool. For me, that moment came in the third week of Programming Fundamentals, when we reached **loops and conditions**.

Before this, code felt like typing. After this, it started feeling like *thinking*.

## What Are Conditions — Really?

We had been introduced to `if`, `else if`, and `else` statements. On the surface, they are simple: if something is true, do this. Otherwise, do that.

But what took me a moment to appreciate was how powerful that simple idea is. Almost every decision a computer makes — every recommendation algorithm, every login system, every game mechanic — is built on some version of this:

```cpp
if (condition is true) {
    do this;
} else {
    do something else;
}
```

Our first exercise was a grade checker. Enter a number between 0 and 100, and the program tells you your grade. Simple enough. But writing it forced me to think about **every possible case** — what if the number is below 0? What if it is above 100? What if it is exactly 50?

That kind of exhaustive thinking — making sure your logic covers every scenario — is something I still use constantly.

## The Loop That Changed Everything

Then came loops. The `for` loop, the `while` loop, the `do-while` loop.

The concept is straightforward: repeat a block of code a certain number of times, or until a condition is no longer true. But the implications of that idea are enormous.

My favourite early exercise was printing a multiplication table:

```cpp
int num;
cout << "Enter a number: ";
cin >> num;

for (int i = 1; i <= 10; i++) {
    cout << num << " x " << i << " = " << num * i << endl;
}
```

Ten lines of output from six lines of code. I remember staring at that output and thinking — *this is why programming is powerful.* You write the logic once, and the machine does the repetition for you.

## Nested Loops — My First Real Challenge

Things got harder when we introduced **nested loops** — loops inside loops. The classic example is printing a pattern of stars:

```cpp
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= i; j++) {
        cout << "* ";
    }
    cout << endl;
}
```

Output:
```
*
* *
* * *
* * * *
* * * * *
```

This took me longer than I want to admit. The outer loop controls the rows, the inner loop controls the columns — but visualizing how they interact required a kind of spatial thinking I had not used before. I drew it out on paper, traced through it step by step, and eventually it clicked.

That process — slowing down, tracing through code manually, drawing it out — became one of my most used study techniques.

## Conditions Inside Loops

The real power came when we combined the two: conditions *inside* loops. Check every number from 1 to 100 and print only the even ones. Find the largest number in a list. Count how many times a condition is true across a range of values.

These exercises felt like puzzles. And I genuinely enjoyed solving them.

## What This Was Teaching Me Beyond Syntax

Looking back, loops and conditions were not just programming concepts. They were teaching me a way of thinking:

- **Break problems into cases.** Not everything has one answer — identify the different scenarios.
- **Think about repetition.** If you are doing the same thing more than twice, there is probably a loop hiding in there.
- **Trace before you run.** If your logic is not clear in your head, it will not be clear to the compiler either.

These habits — which started forming in week three of PF — have stayed with me through every course since. I later learned that this kind of structured, logical thinking is also the foundation of much more advanced fields. The algorithms behind [Dr. Bilal Ahmad's](https://www.linkedin.com/in/drbilalphd/) research in Machine Learning and AI, which you can explore on his [Google Scholar](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en), are built on the same fundamental logic — just applied at a much larger scale.

## The Feeling at the End of Week Three

I went home that Friday genuinely excited about a homework assignment for the first time. The task was to write a program that checked whether a number was prime. I sat with it for an hour, figured it out, and felt the kind of satisfaction that is hard to describe.

That feeling — the small victory of making a machine do exactly what you intended — is addictive. And it started here, with a `for` loop and a star pattern.

---

*Following my journey? Use* ***#MLwithDrBilalAhmad*** *and* ***#DrBilalAhmad*** *to track these posts. You can also connect with* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *to follow his work in AI and Machine Learning.*
