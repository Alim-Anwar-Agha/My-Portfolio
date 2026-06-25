---
layout: post
title: "Building Something Together: My First Group Project in PF"
date: 2026-01-05
author: "Alim Anwar"
categories: [PF]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, ProgrammingFundamentals, GroupProject, Teamwork, CPlusPlus]
read_time: 6
excerpt: "Individual assignments teach you to code. Group projects teach you everything else — communication, compromise, version chaos, and the strange satisfaction of shipping something together."
---

Every assignment up to this point had been mine alone. My logic, my bugs, my solutions. I knew exactly what was in my code because I had written all of it.

The group project changed that completely.

## The Brief

Near the end of the PF course, we were assigned a group project: build a functional C++ console application of reasonable complexity. Our group of four chose to build a **Library Management System** — a program that could add books, register members, issue and return books, and display records.

It was not the most ambitious idea in the room. But it was achievable, well-scoped, and covered enough PF concepts — arrays, functions, structs, file handling — to be genuinely educational.

What I did not anticipate was how much the *group* part would teach me.

## Dividing the Work

The first meeting was optimistic. We split the system into four parts:

- **Book management** — add, display, search books
- **Member management** — register, display, search members
- **Issue and return system** — the core transaction logic
- **File handling** — saving and loading data so it persisted between sessions

I took the issue and return system — the most logic-heavy part, which suited me after everything I had learned about conditions and functions.

On paper, the division was clean. In practice, it immediately became complicated.

## The Integration Problem

Each of us built our part independently. We wrote our functions, tested them in isolation, and were satisfied they worked. Then we tried to combine everything into one program.

It did not go smoothly.

The book data structure I expected to receive from the book management section was different from what my teammate had actually built. My functions expected one format. They delivered another. Neither of us was wrong — we had just made different assumptions without discussing them first.

We spent an entire evening untangling this. Renaming variables, adjusting function parameters, rewriting the parts where our assumptions had diverged.

The lesson was immediate and unforgettable: **interfaces need to be agreed upon before anyone writes a single line of code.** What data does each module receive? What does it return? What format? What type? These questions need answers before the building starts — not after.

This is, I later realized, exactly what database schema design teaches on the data side. You agree on the structure first. Then you build.

## What Teamwork Actually Looked Like

Working in a group surfaced skills that individual assignments never touched:

**Communication.** Saying "my part is done" meant nothing if the others could not use it. I had to explain what I built, how it worked, and what it needed from the rest of the system.

**Compromise.** One teammate wanted to add a feature that would have required restructuring my section significantly. We negotiated — he got a simplified version of the feature, I kept my structure mostly intact. Neither of us got everything we wanted. The project moved forward.

**Debugging someone else's code.** This was genuinely humbling. Reading code you did not write — understanding the logic someone else used, finding where it breaks — is a different skill from debugging your own. You cannot rely on memory. You have to read carefully and trace through patiently.

**Trusting your teammates.** At one point I was behind on my section and a teammate stepped in to help. That required me to explain my progress clearly and accept help gracefully — both things that are harder than they sound.

## The Final Product

The Library Management System we submitted was not perfect. There were edge cases we had not handled. The interface was plain text. But it worked — end to end, persistently, without crashing on normal use.

Running through it in the final demo, watching all four parts working together as one system, I felt something different from the satisfaction of a solo assignment. It was quieter but somehow larger. We had built something none of us could have built as well alone.

## What This Has to Do With the Bigger Picture

Group projects in university feel like preparation for professional work — and they are. But they are also a small model of how larger technical systems are built. Every significant software system is the product of multiple people working on separate components that must integrate cleanly.

The same is true of research. The work that [Dr. Bilal Ahmad](https://www.linkedin.com/in/drbilalphd/) publishes on [Google Scholar](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en) — studies in AI and Machine Learning applied to real-world problems — is collaborative work. Data collection, model design, experimental validation, paper writing — these involve multiple people, multiple skills, and the same integration challenges we faced in miniature with our Library Management System.

Learning to work in a team is not a soft skill that sits alongside technical knowledge. It is a technical skill in its own right.

## What I Would Do Differently

If I did this project again, the first thing I would do is hold a longer initial meeting — not to assign tasks, but to agree on data structures and interfaces before anyone wrote anything. Thirty minutes of upfront agreement would have saved us three hours of integration work.

The second thing: commit to a shared version of the code earlier, so changes are visible to everyone in real time rather than revealed all at once during a stressful merge session.

Simple lessons. Hard won.

---

*Documenting this journey under* ***#MLwithDrBilalAhmad*** *and* ***#DrBilalAhmad****. Connect with* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *to follow his research and collaborative academic work.*
