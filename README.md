# 📘 C++ and Makefile Beginner Summaries  
**Author: Shachar Tsrafati**

This repository includes two beginner-friendly guides:

- ✅ A summary of core **C++** topics (weeks 1–10), based on materials studied at the **University of Ariel**
- ✅ A clear and practical **Makefile** guide for C++ projects

These guides are great for students or anyone starting to learn programming in C++ and working with automated builds using Makefiles.
**THERE MIGHT BE SOME MISTAKES KEEP IN MIND THIS IS NOT PERFECT**

---

## 📚 Contents

- 🚀 C++ Summary
  - ✅ Topics Covered
  - ▶️ Compile Example
- 🛠️ Makefile Guide
  - 📘 What is a Makefile?
  - 🔧 Basic Makefile Example
  - 📦 Using Shortcuts
  - 📌 Common Symbols
  - 🧹 Cleaning Up
  - 📛 Phony Targets
  - 📚 Working with Libraries
  - 📂 Example Project Structure

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

---

## 🛠️ Makefile Guide

This guide introduces the **basics of Makefiles**, helping C and C++ beginners learn how to automate compilation, linking, and working with static and dynamic libraries.

### 📘 What is a Makefile?

A **Makefile** automates compiling C/C++ projects.  
It helps manage multiple source files, dependencies, and build steps using simple syntax.

### 🔧 Basic Makefile Example

```makefile
other.o: other.cpp
	g++ -c other.cpp -o other.o

main.o: main.cpp
	g++ -c main.cpp -o main.o

output: other.o main.o
	g++ other.o main.o -o output
```

### 📦 Using Shortcuts

```makefile
CXX = g++
CXXFLAGS = -g
OUTPUT = output
SRCS = main.cpp other.cpp
OBJS = $(SRCS:.cpp=.o)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

$(OUTPUT): $(OBJS)
	$(CXX) $(CXXFLAGS) -o $@ $^
```

### 📌 Common Symbols

| Symbol | Description                             |
|--------|-----------------------------------------|
| `$@`   | The target (e.g., `main`)               |
| `$^`   | All dependencies (right side of `:`)    |
| `$<`   | First dependency                        |
| `$*`   | Target name without extension (rare)    |

### 🧹 Cleaning Up

```makefile
clean:
	rm -f *.o output *.so *.a
```

### 📛 Phony Targets

```makefile
.PHONY: clean all
```

Helps avoid conflicts when file names match target names.

### 📚 Working with Libraries

#### 🧱 Static Library

```bash
ar rcs libutils.a utils.o
g++ main.cpp -L. -lutils -o main
```

#### 🔗 Shared Library

```bash
g++ -fPIC -shared utils.cpp -o libutils.so
g++ main.cpp -L. -lutils -Wl,-rpath,. -o main
LD_LIBRARY_PATH=. ./main
```

### 📂 Example Project Structure

```
project/
├── main.cpp
├── utils.cpp
├── Makefile
├── lib/
│   └── libutils.so / libutils.a
└── README.md
```

### 📥 Full PDF

- [📄 Makefile Guide PDF](Makefile_guide.pdf)
- [📘 C++ Summary PDF](C++_Summary.pdf)

---

## 🙋‍♂️ Author

**Shachar Tsrafati**

---

## 📜 License

Free to use for educational purposes.
