# 📘 C++ and Makefile Beginner Summaries  
**Author: Shachar Tsrafati**

This repository includes two beginner-friendly guides:

- ✅ A summary of core **C++** topics (weeks 1–10)
- ✅ A clear and practical **Makefile** guide for C++ projects

These guides are great for students or anyone starting to learn programming in C++ and working with automated builds using Makefiles.

---

## 📚 Contents

- [🚀 C++ Summary](#-c-summary)
- [🛠️ Makefile Guide](#-makefile-guide)

---

## 🚀 C++ Summary

This guide covers key topics introduced in a C++ programming course up to Week 10.
I WILL UPDATE THIS

### ✅ Topics Covered

- Variables & Data Types  
- Namespaces, Typedef, and Aliases  
- User-defined Functions  
- Structs & Classes  
- Constructors & Destructors  
- Pointers & Arrays  
- Static Members & Methods  
- Exception Handling (`try`, `catch`)  
- Friend Functions & Operator Overloading  
- Copy Constructors & Assignment Operators  
- `explicit`, Inheritance, and Overriding  
- Function and Class Templates  

### ▶️ Compile Example

```bash
g++ -Wall -Werror -std=c++17 main.cpp -o main
./main
```

# 🛠️ Makefile Beginner Guide  
**Author: Shachar Tsrafati**

This guide introduces the **basics of Makefiles**, helping C and C++ beginners learn how to automate compilation, linking, and working with static and dynamic libraries.

---

## 📚 Contents

- [📘 What is a Makefile?](#-what-is-a-makefile)
- [🔧 Basic Makefile Example](#-basic-makefile-example)
- [📦 Using Shortcuts](#-using-shortcuts)
- [📌 Common Symbols](#-common-symbols)
- [🧹 Cleaning Up](#-cleaning-up)
- [📛 Phony Targets](#-phony-targets)
- [📚 Working with Libraries](#-working-with-libraries)
- [📂 Example Project Structure](#-example-project-structure)
- [📥 Full PDF](#-full-pdf)

---

## 📘 What is a Makefile?

A **Makefile** automates compiling C/C++ projects. It helps manage multiple source files, dependencies, and build steps using simple syntax.

---

## 🔧 Basic Makefile Example

```makefile
other.o: other.cpp
	g++ -c other.cpp -o other.o

main.o: main.cpp
	g++ -c main.cpp -o main.o

output: other.o main.o
	g++ other.o main.o -o output
```
