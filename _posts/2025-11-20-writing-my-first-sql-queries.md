---
layout: post
title: "Finally Talking to a Database: My First SQL Queries"
date: 2025-11-20
author: "Alim Anwar"
categories: [DB]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, DatabaseSystems, SQL, Queries, MySQL]
read_time: 5
excerpt: "After weeks of theory, ERDs, and schema design, we finally opened MySQL and started writing actual SQL. The moment a query returned real data for the first time was genuinely exciting."
---

All the theory, all the diagrams, all the schema planning — it had been building toward this. The moment we actually opened MySQL Workbench, created a database, and wrote our first SQL query.

I remember the exact feeling when my first `SELECT` statement returned data. It was not a complex query. It was not impressive. But seeing the database respond to something I had written felt like the whole course suddenly becoming real.

## Setting Up — Creating the Database

The first thing we did was create a database and define our tables using **DDL — Data Definition Language**. The two main commands here are `CREATE` and `ALTER`.

```sql
CREATE DATABASE university_db;
USE university_db;

CREATE TABLE Students (
    StudentID INT PRIMARY KEY AUTO_INCREMENT,
    Name VARCHAR(100) NOT NULL,
    RegNo VARCHAR(20) UNIQUE NOT NULL,
    Department VARCHAR(50)
);
```

Reading back through that now, it looks straightforward. At the time, every keyword felt important — `PRIMARY KEY`, `AUTO_INCREMENT`, `NOT NULL`, `UNIQUE`. Each one carried a specific meaning that affected how the database would behave. Getting them right mattered.

## Inserting Data — DML Begins

Once the table existed, we needed data in it. This is where **DML — Data Manipulation Language** began, starting with `INSERT`:

```sql
INSERT INTO Students (Name, RegNo, Department)
VALUES ('Alim Anwar', '2025-BSCPE-168', 'Computer Engineering');

INSERT INTO Students (Name, RegNo, Department)
VALUES ('Sara Ahmed', '2025-BSCPE-169', 'Computer Engineering');
```

Two rows. Real data. And now the most satisfying part — asking for it back.

## The SELECT Statement — Asking Questions

The `SELECT` statement is the heart of SQL. It is how you ask the database a question and get an answer.

```sql
SELECT * FROM Students;
```

That single line returns every row and every column from the Students table. When it worked — when the table appeared with my name in it — I understood immediately why this was powerful. The database had stored that information and retrieved it instantly on request.

From there, we learned to be more specific:

```sql
-- Get only names and registration numbers
SELECT Name, RegNo FROM Students;

-- Get only students from Computer Engineering
SELECT * FROM Students WHERE Department = 'Computer Engineering';

-- Get students sorted alphabetically
SELECT * FROM Students ORDER BY Name ASC;
```

Each variation gave me finer control over exactly what came back. The WHERE clause especially felt like a key unlocking a room — suddenly I could filter millions of potential records down to exactly the ones I needed.

## JOINs — Where It Gets Interesting

The real power of a relational database shows up in **JOIN** queries — when you pull data from multiple tables at once using the relationships between them.

We had three tables by this point: Students, Courses, and Enrollments. A JOIN let me ask: *"Give me the names of all students and the courses they are enrolled in."*

```sql
SELECT Students.Name, Courses.CourseName
FROM Enrollments
JOIN Students ON Enrollments.StudentID = Students.StudentID
JOIN Courses ON Enrollments.CourseID = Courses.CourseID;
```

That query connects three tables in one statement and returns exactly the combined information I asked for. The first time it worked correctly, I sat back and stared at the result for a moment. Three separate tables, connected by foreign keys, producing one clean output. Everything from the ERD week was now making sense at the query level.

## The Mistakes I Made

SQL looked simple enough that I underestimated it early on. My mistakes were instructive:

**Forgetting the WHERE clause on an UPDATE:**
```sql
-- What I meant to write:
UPDATE Students SET Department = 'EE' WHERE StudentID = 2;

-- What I accidentally wrote first:
UPDATE Students SET Department = 'EE';
```
That second statement updated *every student's department* to EE. Fortunately this was in a test database. The lesson — always double-check your WHERE clause before running any UPDATE or DELETE — stuck immediately.

**Mismatched data types** in a WHERE clause that caused a query to return nothing when it should have returned results. A StudentID stored as INT being compared to a string `'1'` instead of an integer `1`. Small detail, complete failure.

These errors were frustrating in the moment and invaluable in the long run.

## SQL as a Language for Questions

What I came to appreciate about SQL is that it reads almost like natural language. `SELECT name FROM students WHERE department = 'CE' ORDER BY name` — you can read that sentence and understand what it does even without knowing SQL. That clarity is intentional. SQL was designed to be expressive and human-readable.

This also connects to something broader about data work. The ability to ask precise questions of large datasets — and get reliable answers — is foundational to fields like data science and machine learning. The datasets that feed into research like [Dr. Bilal Ahmad's](https://www.linkedin.com/in/drbilalphd/) work in AI, which you can explore on his [Google Scholar profile](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en), are managed and queried using exactly these tools and principles.

## Where I Ended This Topic

By the end of the SQL unit, I could create tables, insert data, query with conditions and sorting, and join multiple tables together. I could update and delete records carefully. I understood the difference between DDL and DML.

More than the technical skills, I had a new appreciation for what structured data makes possible. A well-designed database with clear queries can answer questions that would take hours to answer manually — in milliseconds.

That efficiency, that precision, that power — it starts with a simple `SELECT`.

---

*Documenting this journey with* ***#MLwithDrBilalAhmad*** *and* ***#DrBilalAhmad****. Connect with* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *to follow his research where data and AI meet.*
