---
layout: post
title: "Mid-Semester: When Everything Felt Too Hard"
date: 2025-10-15
author: "Alim Anwar"
categories: [Journey]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, MidSemester, Struggles, Breakthroughs, StudentLife]
read_time: 6
excerpt: "There was a point mid-semester where I genuinely wondered if I had chosen the wrong field. This is the honest account of hitting that wall — and what happened after."
---

Nobody talks about this part enough. The part where university stops being exciting and starts being exhausting. Where the content piles up faster than you can absorb it, where your confidence quietly shrinks, and where you start asking yourself questions you did not expect to be asking so soon.

For me, that moment came around week six of the first semester.

## The Wall

It happened gradually and then all at once.

In Programming Fundamentals, we had moved into **arrays and pointers** — two topics that many CE students quietly agree are where things get genuinely difficult. Arrays I could handle. Pointers were another story entirely.

The idea that a variable could store not a value but the *address* of another variable — and that you could then manipulate the original value through that address — felt abstract in a way nothing before it had. I read the notes. I watched explanations. I wrote the code. And still, something about it refused to sit properly in my brain.

```cpp
int x = 10;
int* ptr = &x;

cout << x << endl;    // prints 10
cout << &x << endl;   // prints the memory address of x
cout << ptr << endl;  // also prints the memory address of x
cout << *ptr << endl; // prints 10 — the value AT that address
```

I could read that code. I could even reproduce it. But *why* it worked the way it did — why this was useful, what problem it was solving — did not feel clear to me yet.

## Everything at Once

The pointer confusion would have been manageable on its own. But it was not on its own. Assignments were stacking up. There was a lab report due. There were other courses with their own demands. And the mid-semester assessment was approaching.

I remember a specific evening where I sat down to study and just... stared at my notes. Not reading. Not thinking. Just staring. That feeling — a kind of mental paralysis where everything feels too large to approach — was new to me. I had always been able to push through difficulty before. This was different.

## What I Did About It

I did not have a dramatic breakthrough moment. What I had instead was a series of small, deliberate steps.

**First**, I stopped trying to understand everything at once. I picked one thing — pointers — and decided I would not move on until that specific concept made sense. Not everything. Just that one thing.

**Second**, I went back to basics. Instead of staring at complex pointer examples, I went back to the simplest possible case: one variable, one pointer, trace through it line by line on paper. Then add one more step. Then one more.

**Third**, I asked for help. This sounds obvious but it took me longer than it should have. A classmate who had grasped pointers faster than me sat with me for an hour and explained it using a metaphor I still remember: *"The variable is the house. The address is the house number. The pointer stores the house number. The dereference operator goes to the house and tells you what is inside."*

That metaphor unlocked it for me. Completely.

## The Breakthrough

Once pointers clicked, something else happened. The confusion I had been carrying — that general fog of *I might not be cut out for this* — lifted. Not because everything was suddenly easy, but because I had proven to myself that I could work through something genuinely hard.

That is the thing about difficult concepts in technical subjects. They do not just teach you the concept. They teach you that you are capable of learning difficult things. And that knowledge compounds.

## What I Learned About Learning

The mid-semester wall taught me more about *how I learn* than any single topic in the course:

- **Isolation works.** When overwhelmed, pick one thing and go deep on it rather than skimming everything.
- **Metaphors matter.** Abstract concepts become concrete when you find the right real-world comparison.
- **Asking for help is a skill.** Knowing when you have spent long enough struggling alone — and then actually asking — is something you have to practice.
- **Consistency beats intensity.** An hour of focused study every day is worth more than one panicked all-nighter before the exam.

These are lessons I have carried into every semester since. They also resonate with something I have come to understand about research and advanced study. The kind of deep, structured problem-solving that underpins [Dr. Bilal Ahmad's](https://www.linkedin.com/in/drbilalphd/) work in AI and ML — which you can explore on his [Google Scholar profile](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en) — requires exactly this kind of patient, methodical approach to hard problems.

## The Assessment

The mid-semester assessment came. I was not perfectly prepared — I do not think anyone ever is — but I was prepared enough. The pointer questions showed up. I answered them. Not brilliantly, but correctly.

Walking out of that room, I felt something I had not felt in weeks: steady.

## For Anyone Reading This Who Is There Right Now

If you are in that wall moment — the one where everything feels too hard and you are quietly wondering if you belong here — I want to say this plainly: that feeling is not evidence that you do not belong. It is evidence that you are doing something genuinely difficult.

The wall is not the end of the road. It is just part of it.

---

*Tracking this journey under* ***#MLwithDrBilalAhmad*** *and* ***#DrBilalAhmad****. Follow* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *to see the kind of research that waits on the other side of these fundamentals.*
