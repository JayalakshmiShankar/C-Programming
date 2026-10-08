# C Programming for Absolute Beginners

## Part 1: Introduction

No experience needed. If you can use a phone or a computer, you can learn this. Every new word is explained the first time it appears, and there is a small word list at the end.

---

## 1. What is a program?

You already know what a **recipe** is: a list of clear steps that someone follows to make a dish.

A **program** is a recipe for a computer. It is a list of steps that tells the computer exactly what to do, for example "add these two numbers" or "show this message on the screen".

A computer is very fast, but it cannot guess. It does exactly what the steps say, nothing more and nothing less. Writing those steps is called **programming** (or **coding**).

---

## 2. How does a computer understand instructions?

Inside a computer, everything is stored using only two symbols: **0** and **1**. This is called **binary**. A computer's processor (the **CPU**, the part that does the work) only understands instructions written in 0s and 1s. These raw instructions are called **machine code**.

Here is the problem: humans find it extremely hard to write or read long lists of 0s and 1s. Imagine writing a whole recipe using only dots and dashes.

So programmers invented a better way.

---

## 3. What is a programming language?

A **programming language** is a way for humans to write instructions in a form they can read, which is then translated into machine code for the computer.

Think of a **travel guide who translates**: you speak in your own language, and the guide turns it into the local language for the people you are visiting. In programming, that translator is a program called a **compiler** (you will learn more about it in Part 2).

Languages come in different "levels":

| Level | Example | What it is like |
| ----- | ------- | --------------- |
| Very close to the machine | Machine code, Assembly | Like giving a worker tiny, detailed steps for every movement. Powerful but slow to write and hard to read |
| Closer to human language | Python, Java | Like telling the worker "make tea". Easy to write, but you do not control the small details |
| In the middle | **C** | Readable like a language, yet still gives you control over the machine |

---

## 4. What is C?

**C** is a programming language that sits in the middle: it is easy enough for humans to read, but close enough to the computer that you can control how it works.

It is also **fast**, because C programs are translated into machine code before they run, and the result runs straight on the computer.

> **Analogy:** Driving a **manual car** gives you more control and can be more efficient, but you have to do more yourself (clutch, gears). An **automatic car** is easier, but you control less. Python is closer to the automatic car. C is closer to the manual car.

---

## 5. Why was C created? (a short story)

Long ago, programmers had two choices:

1. **Assembly language:** full control of the computer, but hard to read, slow to write, and it only worked on one type of computer. If you bought a different computer, you had to rewrite everything.
2. **Higher-level languages:** easier to write, but too slow and too far from the machine to build something as important as an **operating system** (the main software that runs a computer, like Windows, Android or Linux).

Nobody had a language that was both **readable** and **close to the machine**.

That is why **Dennis Ritchie** created C in **1972** at **Bell Labs**, a research lab in the USA. A few years later, the **Unix** operating system was rewritten in C. This was a big moment: because C can be translated for many types of computers, the operating system could be moved to a new computer without rewriting it from scratch.

### Timeline

| Year | What happened |
| ---- | ------------- |
| 1967 | BCPL: a simple language made for writing compilers |
| 1969 | B: a smaller version of BCPL, made by Ken Thompson for early Unix |
| 1972 | **C is created** by Dennis Ritchie, adding data types and more structure |
| 1973 | Unix is rewritten in C |
| 1989 | First official standard for C (ANSI C), so C works the same way on different systems |

---

## 6. Where is C used today?

You use software written in C every day without knowing it.

| Where | Example |
| ----- | ------- |
| Operating systems | The Linux kernel, which also sits at the core of Android |
| Small smart devices (**embedded systems**) | Washing machines, car electronics, medical devices |
| Databases (programs that store data) | SQLite, which is inside many phone apps |
| Other languages | The main Python interpreter is itself written in C |
| Games and graphics | Parts where speed matters a lot |

**Why this matters if you want to learn AI or data science:** popular Python tools like NumPy are fast because their heavy parts are written in C. Learning C helps you understand what is happening underneath.

---

## 7. An honest note: C gives you power, and responsibility

In C, **you** manage the computer's **memory** (the temporary workspace where a running program keeps its data, like a desk where you spread out your papers). The computer will not clean up or warn you much. If you make a mistake, the program may crash.

This sounds scary, but it is the very reason C teaches you so much. Once you understand C, other languages become much easier to understand. Take it step by step, and we will build up slowly.

---

## 8. Word list

| Word | Simple meaning |
| ---- | -------------- |
| Program | A list of steps for a computer to follow |
| Programming / coding | Writing those steps |
| Binary | The 0s and 1s a computer works with |
| CPU | The part of the computer that does the work |
| Machine code | Instructions in 0s and 1s that the CPU understands |
| Programming language | A readable way to write a program |
| Compiler | A translator that turns your code into machine code |
| Operating system | The main software that runs the computer (Windows, Android, Linux) |
| Memory | The temporary workspace a running program uses |
| Embedded system | A small computer built into a device |

---

## 9. Quick check

Try answering in your own words, then compare with the answers below.

1. What is a program, in one sentence?
2. Why do we use programming languages instead of writing 0s and 1s?
3. Why was C created?
4. Who created C, and in which year?
5. Name two places where C is used today.
6. In the car comparison, which language is the "manual car", and why?

**Answers**

1. A list of steps that tells a computer what to do.
2. Writing 0s and 1s is extremely hard for humans, so we write readable code and let a translator convert it.
3. Because assembly was hard to read and tied to one machine, and the higher-level languages of that time were too slow for building an operating system. C is readable and still close to the machine.
4. Dennis Ritchie, in 1972, at Bell Labs.
5. For example: operating systems like Linux, embedded devices, and databases like SQLite.
6. C, because it gives you more control but you must handle more things yourself.

---

**Next: Part 2, How a C Program Runs.** You will learn what a compiler does, how to set up your tools, and write and run your very first program.