---
layout: post
title: "Functions: The Day My Code Stopped Being a Mess"
date: 2025-10-01
author: "Alim Anwar"
categories: [PF]
tags: [MLwithDrBilalAhmad, DrBilalAhmad, ProgrammingFundamentals, Functions, ModularThinking, CPlusPlus]
read_time: 5
excerpt: "Before functions, my code was one long block of chaos. After functions, it started having structure, purpose, and something that almost looked like elegance."
---

By the fourth week of Programming Fundamentals, my programs were getting longer. And messier. I had variables scattered everywhere, repeated blocks of code copied and pasted, and a `main()` function that was turning into a wall of text nobody — including me — could easily follow.

Then we reached **functions**. And everything changed.

## What Is a Function?

A function is a named, reusable block of code that does one specific thing. You define it once, and you can call it as many times as you need — from anywhere in your program.

The syntax in C++ looked like this:

```cpp
int add(int a, int b) {
    return a + b;
}

int main() {
    int result = add(5, 3);
    cout << result << endl;
    return 0;
}
```

Simple enough. But the concept behind it — **write once, use many times** — was more powerful than it first appeared.

## The Problem Functions Solved

Before functions, if I needed to calculate something in three different places in my program, I would write the same calculation three times. If I later found a mistake in that calculation, I had to fix it in three places. And I would inevitably miss one.

With functions, I write the logic once. Fix it once. And every place that calls the function gets the corrected version automatically.

This is called the **DRY principle** — Don't Repeat Yourself. I did not know the term at the time, but I felt the truth of it the moment I started using functions properly.

## Parameters, Arguments, and Return Values

The next layer was understanding how information flows into and out of a function:

- **Parameters** are the inputs a function expects
- **Arguments** are the actual values you pass when calling it
- **Return values** are what the function gives back

```cpp
float circleArea(float radius) {
    return 3.14159 * radius * radius;
}

int main() {
    cout << "Area: " << circleArea(5.0) << endl;
    cout << "Area: " << circleArea(7.5) << endl;
    return 0;
}
```

Two different areas, one function, zero repeated logic. It felt clean in a way my earlier code never had.

## Scope — The Concept That Confused Me Most

With functions came the concept of **scope** — the idea that a variable declared inside a function only exists inside that function. It cannot be seen or used outside.

This tripped me up badly at first. I would declare a variable inside a function, try to use it in `main()`, and get a compiler error I did not understand.

```cpp
void myFunction() {
    int x = 10; // x only exists here
}

int main() {
    cout << x << endl; // ERROR — x does not exist here
    return 0;
}
```

Understanding scope required me to mentally model the program as a set of separate, self-contained rooms. Each function is its own room. Variables declared in one room do not exist in another — unless you pass them through the door as parameters or return values.

Once that mental model clicked, scope stopped being confusing and started being useful. It meant functions were truly independent. You could trust them to do their job without interfering with the rest of the program.

## Modular Thinking — The Real Lesson

What functions were really teaching me was **modular thinking** — the habit of breaking a large problem into small, independent, well-defined pieces.

Instead of thinking *"write a program that does X"*, I started thinking:
- What are the distinct tasks this program needs to perform?
- Can I write a function for each task?
- How do these functions connect to each other?

This shift in thinking — from one big solution to many small, composable pieces — is something I still use in every project. It also maps directly onto how larger systems are built. Modular thinking is the foundation of software architecture, of API design, of how Machine Learning pipelines are structured. Looking at the kind of research [Dr. Bilal Ahmad](https://www.linkedin.com/in/drbilalphd/) publishes on his [Google Scholar profile](https://scholar.google.com.au/citations?user=8nZ0jVkAAAAJ&hl=en), you see the same principle at work — complex problems broken into structured, well-defined components.

## My First Properly Structured Program

By the end of this topic, I wrote a menu-driven calculator — a program with a main menu that called separate functions for addition, subtraction, multiplication, and division. Each function did exactly one thing. The `main()` function just handled the menu and called whichever function the user chose.

When I read back through that code, it actually made sense. I could follow it from top to bottom. I knew where to look if something went wrong.

That was the first time I felt genuinely proud of something I had written.

## The Habit That Stuck

Functions gave me a habit I carry into every piece of work I do now: **before writing any code, identify the pieces.** What are the distinct jobs that need to be done? Can each job be isolated? Can I name it clearly?

If you can name a piece of functionality clearly, you can write a function for it. And if you can write a function for it, your program becomes something you can actually manage.

---

*Documenting this journey with* ***#MLwithDrBilalAhmad*** *and* ***#DrBilalAhmad****. Connect with* [*Dr. Bilal Ahmad on Facebook*](https://www.facebook.com/Dr.BilalAhm) *to follow his research in AI and Deep Learning.*
