---
layout: post
title: "A New Way of Thinking: My Introduction to Database Systems"
date: 2025-11-01
author: "Alim Anwar"
categories: [DB]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, DatabaseSystems, DB, SQL, DataModeling]
read_time: 5
excerpt: "After a semester of telling computers what to do step by step, Database Systems introduced a completely different question: how do you store, organize, and retrieve information at scale?"
---

Coming off the back of Programming Fundamentals, I had started to develop a particular way of thinking — sequential, procedural, step by step. Write an instruction. Execute it. Write the next one.

Database Systems asked me to think differently.

## The First Lecture — A Different Kind of Problem

The opening lecture of DB did not start with syntax or commands. It started with a question: *how do large organizations manage their data?*

Think about a university. Thousands of students. Hundreds of courses. Dozens of departments. Exam results, fee records, attendance — all of it interconnected. How does it all stay organized? How does a single query pull up a specific student's result in a specific course in a specific semester, instantly, from among millions of records?

That is the problem databases solve. And the moment I understood the scale of that problem, I understood why an entire course was dedicated to it.

## What Is a Database — Actually?

We established early on that a database is not just a collection of files. It is a structured, organized collection of data managed by a **Database Management System (DBMS)** — software that handles storing, retrieving, and manipulating that data efficiently and reliably.

The DBMS we would be working with was **MySQL**. But more important than the specific tool was the model behind it — the **relational model**, where data is organized into tables, and tables are connected to each other through defined relationships.

This was the conceptual foundation everything else would build on.

## Tables, Rows, and Columns

The basic unit of a relational database is a **table**. Each table represents one type of entity — a Student table, a Course table, an Enrollment table. Each row in the table is one record. Each column is one attribute of that record.

```
Students Table:
| StudentID | Name         | RegNo          | Department |
|-----------|--------------|----------------|------------|
| 1         | Alim Anwar   | 2025-BSCPE-168 | CE         |
| 2         | Sara Ahmed   | 2025-BSCPE-169 | CE         |
```

Simple enough on the surface. But the questions this raised were immediately interesting: What if a student enrolls in multiple courses? What if a course has multiple students? How do you represent that relationship without duplicating data everywhere?

Those questions led us directly into the next topics — keys, relationships, and eventually normalization. But on day one, just seeing data organized this way — clean, structured, queryable — felt like a revelation after the chaos of unstructured files.

## Why This Felt Different From PF

In PF, I was telling the computer *how* to do something. Write a loop. Call a function. Move through the logic step by step.

In DB, I was telling the computer *what* I wanted. "Give me all students enrolled in this course." "Show me every result above 70." The database engine figured out *how* to retrieve it. My job was to describe the result I needed, not the process of finding it.

This distinction — **imperative** thinking in PF versus **declarative** thinking in DB — was one of the most interesting intellectual shifts of my first year. Two courses, two completely different relationships between the programmer and the machine.

## The Role of Structure

What struck me most about database design was how much thought goes into structure *before* you write a single query. The schema — the definition of your tables, columns, data types, and relationships — has to be designed carefully upfront. A poorly designed schema causes problems that compound over time. A well-designed one makes everything else easier.

This emphasis on thinking carefully before acting is something I have seen come up again and again in technical fields. It is also a principle that runs through rigorous research — the kind [Dr. Bilal Ahmad](https://www.linkedin.com/in/drbilalphd/) conducts in AI and Machine Learning, where data quality and structure are foundational. You can follow his published work on [Google Scholar](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en) to see how seriously the field takes data as a discipline in itself.

## What I Was Looking Forward To

By the end of the first week of DB, I had a list of things I wanted to understand:

- How do you design a database schema from scratch?
- What makes a relationship between tables efficient?
- How does SQL actually work under the hood?
- What happens when a database gets very large?

These were not questions I was assigned. They were questions that came naturally from being genuinely curious about a new subject.

That curiosity — the feeling of encountering a field that opens more questions than it closes — is one of the best signs that you are in the right place.

## First Impressions

Database Systems, in its first week, felt like learning a new language for organizing knowledge. Not just data — knowledge. The difference between a spreadsheet and a well-designed relational database is the difference between a pile of notes and a library.

I was ready to learn how to build the library.

---

*Following this journey? Track it with* ***#MLwithDrBilalAhmad*** *and* ***#DrBilalAhmad****. Connect with* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *to see how data and AI intersect at the research level.*
