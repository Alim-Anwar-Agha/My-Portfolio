---
layout: post
title: "Drawing Before Coding: ERDs and Data Modeling"
date: 2025-11-10
author: "Alim Anwar"
categories: [DB]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, DatabaseSystems, ERD, DataModeling, Schema]
read_time: 5
excerpt: "Before writing a single line of SQL, we spent an entire week drawing diagrams. At first it felt like a detour. It turned out to be the most important foundation of the course."
---

When our DB instructor told us we would be spending a full week drawing diagrams before touching any actual database software, I did not fully understand why. It felt like a detour. I wanted to get into the actual work — the queries, the tables, the commands.

By the end of that week, I understood completely. That week of drawing was the work.

## What Is an ERD?

An **Entity-Relationship Diagram** — ERD — is a visual blueprint of a database. Before you create a single table or write a single query, you draw out:

- **Entities** — the things you are storing data about (Students, Courses, Teachers)
- **Attributes** — the properties of each entity (a Student has a Name, a RegNo, a Department)
- **Relationships** — how entities connect to each other (a Student *enrolls in* a Course)

The diagram gives you a complete picture of your data structure before you commit to anything. It is the architectural plan before the construction begins.

## My First ERD — A University System

Our first exercise was to design an ERD for a simplified university management system. I started with three entities:

```
[Student] ----enrolls in---- [Course] ----taught by---- [Teacher]
```

Each entity had its own attributes:

**Student:** StudentID, Name, RegNo, Department  
**Course:** CourseID, CourseName, CreditHours  
**Teacher:** TeacherID, Name, Specialization  

Simple enough. But the moment I started thinking about the *relationships* between these entities, things got interesting.

## Cardinality — The Detail That Changes Everything

The relationship between Student and Course is not just *"student enrolls in course."* It is: *one student can enroll in many courses, and one course can have many students.* This is called a **many-to-many** relationship.

In an ERD, we represent this with cardinality notation:

```
[Student] ----M--------N---- [Course]
```

That M and N look small. But they carry enormous implications for how the database is actually built. A many-to-many relationship cannot be represented directly in two tables — you need a third table in between, called a **junction table** or **associative entity**:

```
[Student] ----1--------M---- [Enrollment] ----M--------1---- [Course]
```

The Enrollment table holds the StudentID and CourseID together, turning one complex relationship into two simpler ones.

That insight — that the diagram forces you to think about structure before it becomes a problem — was one of the clearest moments of understanding I had in the whole course.

## Primary Keys and Foreign Keys

ERDs also introduced two concepts that would run through everything in DB:

- **Primary Key** — a unique identifier for each record in a table. No two students can share the same StudentID.
- **Foreign Key** — a column in one table that references the primary key of another table, creating the link between them.

```
Enrollment Table:
| EnrollmentID | StudentID (FK) | CourseID (FK) | Grade |
|--------------|----------------|---------------|-------|
| 1            | 101            | CS201         | A     |
| 2            | 101            | DB301         | B+    |
```

The foreign keys here — StudentID and CourseID — are what connect the Enrollment table back to the Student and Course tables. Remove those connections and you have three isolated tables of useless data. Keep them and you have a working relational database.

## Why Designing Before Building Matters

The lesson I took from ERDs went beyond databases. It was about the value of planning before executing.

In programming, I had learned to think through logic before writing code. In database design, I learned to think through structure before creating tables. The principle is the same: time spent on a clear plan before implementation saves far more time during implementation.

This is a principle that applies at every level of technical work. Research in AI and ML — like the work [Dr. Bilal Ahmad](https://www.linkedin.com/in/drbilalphd/) publishes, which you can read on his [Google Scholar profile](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en) — requires careful data modeling and schema design before any model is trained. The quality of the data structure directly affects the quality of everything built on top of it.

## The ERD I Was Most Proud Of

Midway through the week, we were given a free exercise: design an ERD for any system of our choice. I chose a library management system — books, members, loans, authors, categories.

It took me two drafts. The first had several relationship errors — I had made some many-to-many connections that should have been one-to-many, and I had missed a junction table. The second draft was clean. Every entity had a clear purpose. Every relationship had correct cardinality. Every key was in the right place.

My instructor looked at it and said it was well structured. That was enough.

## What ERDs Gave Me

Beyond the technical knowledge, ERDs gave me a habit: **before building anything, draw it first.** Whether it is a database, a program, or a project plan — a clear visual structure reveals problems that words and code hide.

I did not expect to spend a week drawing boxes and arrows in a database course. I am glad I did.

---

*Following this learning journey under* ***#MLwithDrBilalAhmad*** *and* ***#DrBilalAhmad****. Connect with* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *— his research shows exactly where careful data modeling leads.*
