---
layout: post
title: "Second Semester: Same Campus, Different Student"
date: 2026-02-01
author: "Alim Anwar"
categories: [Journey]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, MLProject, SecondSemester, OOP, NewChallenges]
read_time: 5
excerpt: "Walking back into UET for the second semester felt different from the first day. The campus was the same. I was not."
---

There is something quietly significant about the first day of second semester. You walk through the same gate, sit in the same kind of classroom, open a new notebook. But everything you carry into that room is different from what you carried four months ago.

I was no longer arriving at university for the first time. I was returning — with a semester's worth of experience, mistakes, and hard-won understanding behind me.

## What Was Different From Day One

The nervousness of the first semester had mostly gone. Not completely — new courses, new expectations, new material always carry some uncertainty. But the specific anxiety of not knowing how university works, not knowing how to study at this level, not knowing whether I could keep up — that was gone.

I knew how to read a timetable and actually plan around it. I knew how to approach a topic I did not understand yet. I knew when to push through alone and when to ask for help. These sound small. They are not small.

## The New Courses

Second semester brought a new set of subjects, and the one I was most curious — and cautious — about was **Object-Oriented Programming (OOP)**.

After a semester of procedural C++ in PF, OOP asked me to think about programs in an entirely new way. Instead of functions acting on data, the data and the functions that act on it are bundled together into **objects**. Instead of procedures, you have **classes**. Instead of calling functions, you send **messages to objects**.

```cpp
class Student {
private:
    string name;
    string regNo;

public:
    Student(string n, string r) {
        name = n;
        regNo = r;
    }

    void display() {
        cout << "Name: " << name << ", Reg: " << regNo << endl;
    }
};

int main() {
    Student s1("Alim Anwar", "2025-BSCPE-168");
    s1.display();
    return 0;
}
```

Reading that code on the first day of OOP, I could follow it — the PF foundation made it legible. But thinking in it, designing with it, was a different challenge entirely.

## The Foundation Underneath

What second semester made immediately clear was how much the first semester mattered.

OOP in C++ is not a separate language — it is an extension of the same C++ I had learned in PF. The syntax, the data types, the control structures — all of it carried over. The new concepts (classes, objects, inheritance, polymorphism) were built on top of what I already knew, not instead of it.

The same was true of any data work in second semester. Database concepts — schema design, relationships, query logic — showed up as background knowledge that did not need to be re-learned, just applied in new contexts.

First semester had felt like laying bricks one by one without seeing the building. Second semester was the first time I could see what those bricks were becoming.

## A Harder Kind of Difficult

The challenges in second semester were different in character from first semester challenges.

In PF, difficulty usually meant: *I do not understand this concept yet.* The solution was to study it more carefully until it clicked.

In OOP, difficulty sometimes meant: *I understand the concept but I am not sure how to apply it here.* That is a harder problem. It requires judgment, design sense, and experience — things that come more slowly than conceptual understanding.

**Inheritance**, for example — the idea that one class can inherit the properties and methods of another — is not a difficult concept to grasp. But deciding *when* to use inheritance versus when to use composition, how deep an inheritance hierarchy should go, what belongs in a base class versus a subclass — those are design decisions that require thinking I was only beginning to develop.

## What Carried Over From Last Semester

Beyond the technical knowledge, the habits I had built in first semester were the most valuable things I brought into second semester:

The habit of **breaking problems into smaller pieces** before writing any code — now applied to class design before writing any methods.

The habit of **drawing before building** — now applied to class diagrams the same way I had applied ERDs to database design.

The habit of **reading error messages carefully** — still as relevant in OOP as it had been in the first week of PF.

And the habit of **looking at the bigger picture** — understanding where what I was learning connected to the wider field. [Dr. Bilal Ahmad's](https://www.linkedin.com/in/drbilalphd/) research, which I had explored on his [Google Scholar profile](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en), is built on exactly the kind of object-oriented, modular, structured thinking that OOP was teaching me. Systems that process medical data, pipelines that feed ML models — these are built with classes, objects, and the design principles I was now beginning to learn properly.

## The Honest State of Things

Second semester is harder than first semester. The material is more complex, the expectations are higher, and the honeymoon period of being a new student is over.

But it is also more interesting. The connections between subjects are more visible. The work is starting to feel less like exercises and more like actual engineering. The distance between where I am and where I want to be is still large — but for the first time, I can see the path between them more clearly than just the destination.

That clarity is its own kind of motivation.

---

*Still documenting this journey under* ***#MLwithDrBilalAhmad***, ***#DrBilalAhmad*** *and* ***#MLProject****. Connect with* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *and follow his work as you follow mine.*
