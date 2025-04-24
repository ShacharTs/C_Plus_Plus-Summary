# 📘 C++ & Makefile Beginner Summaries  
**Author: Shachar Tsrafati**

A concise, student-authored reference covering both core C++ topics and Makefile-based build automation. Ideal for beginners and intermediate learners preparing for coursework or quick refreshers during development.

---

## 📚 Contents

1. [C++ Summary](#c-summary)  
   1. [Topics Covered](#topics-covered)  
   2. [Compile Example](#compile-example)  
2. [Makefile Guide](#makefile-guide)  
   1. [What is a Makefile?](#what-is-a-makefile)  
   2. [Basic Example](#basic-example)  
   3. [Variables & Patterns](#variables-and-patterns)  
   4. [Common Symbols](#common-symbols)  
   5. [Cleaning & Phony Targets](#cleaning-and-phony-targets)  
   6. [Libraries](#libraries)  
   7. [Project Structure](#project-structure)  
3. [Usage](#usage)  
4. [Credits](#credits)  
5. [License](#license)

---

<a name="c-summary"></a>
## 🚀 C++ Summary

A quick reference of key C++ topics from syntax basics to advanced features. For full details, see [C++_Summary.pdf](C++_Summary.pdf).

<a name="topics-covered"></a>
### 1. Topics Covered

- Variables & Data Types  
- Strings & `using namespace std`  
- `const` Qualifier  
- Namespaces  
- Typedefs & Aliases  
- Input/Output (`std::cin`, `std::cout`)  
- Control Flow (`if`, `switch`, loops)  
- Functions & Overloading  
- Header Files & Includes  
- Structs & Classes  
- Constructors & Destructors  
- Arrays & Raw Pointers  
- Static Members & Methods  
- RAII & Smart Pointers (`unique_ptr`, `shared_ptr`, `weak_ptr`)  
- Exception Handling (`try`/`catch`)  
- Composition & Initialization  
- Friend Functions & Operator Overloading  
- Literals & Type Conversions  
- Copy Control (Shallow vs. Deep)  
- `explicit` Keyword  
- Inheritance & Polymorphism  
- Casting (`static_cast`, `dynamic_cast`, `reinterpret_cast`)  
- Templates (Function, Class, Specialization, Metaprogramming)  
- STL Containers & Algorithms (tuple, vector, set, map, iterators)

<a name="compile-example"></a>
### 2. Compile Example

```bash
g++ -std=c++17 -Wall -Wextra example.cpp -o example
./example
```

---

<a name="makefile-guide"></a>
## 🛠️ Makefile Guide

An introduction to automating builds in C/C++ projects using Makefiles. For full details, see [Makefile_guide.pdf](Makefile_guide.pdf).

<a name="what-is-a-makefile"></a>
### 1. What is a Makefile?
A plain-text file defining build targets, dependencies, and shell commands. Automates compilation, linking, and cleaning.

<a name="basic-example"></a>
### 2. Basic Example
```makefile
# Build object files
main.o: main.cpp
	g++ -std=c++17 -c main.cpp -o main.o

util.o: util.cpp
	g++ -std=c++17 -c util.cpp -o util.o

# Link executable
app: main.o util.o
	g++ main.o util.o -o app
```

<a name="variables-and-patterns"></a>
### 3. Variables & Patterns
```makefile
CXX      = g++
CXXFLAGS = -g -std=c++17
SRCS     = main.cpp util.cpp
OBJS     = $(SRCS:.cpp=.o)
TARGET   = app

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

$(TARGET): $(OBJS)
	$(CXX) $(CXXFLAGS) -o $@ $^
```

<a name="common-symbols"></a>
### 4. Common Symbols
| Symbol | Description   |
|--------|---------------|
| `$@`   | Target name   |
| `$^`   | All prerequisites |
| `$<`   | First prerequisite |

<a name="cleaning-and-phony-targets"></a>
### 5. Cleaning & Phony Targets
```makefile
.PHONY: clean all
all: $(TARGET)
clean:
	rm -f $(OBJS) $(TARGET)
```

<a name="libraries"></a>
### 6. Working with Libraries
- **Static**: `ar rcs libmylib.a mylib.o` then `g++ main.o -L. -lmylib -o main`  
- **Shared**: `g++ -fPIC -shared util.cpp -o libutil.so` then `g++ main.cpp -L. -lutil -Wl,-rpath=. -o main`

<a name="project-structure"></a>
### 7. Example Project Structure
```
project/
├── Makefile
├── main.cpp
├── util.cpp
├── include/
│   └── util.h
├── lib/           # compiled libraries
│   ├── libutil.a
│   └── libutil.so
└── README.md
```

---

<a name="usage"></a>
## ⚙️ Usage

1. **Compile C++ Samples:**  
   `g++ -std=c++17 -Wall -Wextra example.cpp -o example`  
2. **Build with Make:**  
   `make` or `make app`  
3. **Clean:**  
   `make clean`

---

<a name="credits"></a>
## 🙏 Credits

Created by Shachar Tsrafati using:
- GeeksforGeeks tutorials and articles  
- Official C++ reference documentation  
- Various online tutorials  
- Coursework materials from Ariel University

---

<a name="license"></a>
## 📜 License

Free to use and adapt for educational purposes. Verify examples and report improvements.

