# 📘 C++ & Makefile Beginner Summaries  
**Author: Shachar Tsrafati**

A concise, student-authored reference covering both core C++ topics and Makefile-based build automation. Ideal for beginners and intermediate learners preparing for coursework or quick refreshers during development.

---

## 📚 Contents

1. [C++ Summary](#-c-summary)  
   1. Topics Covered  
   2. Compile Example  
2. [Makefile Guide](#-makefile-guide)  
   1. What is a Makefile?  
   2. Basic Example  
   3. Variables & Patterns  
   4. Common Symbols  
   5. Cleaning Up & Phony Targets  
   6. Libraries  
   7. Project Structure  
3. [Usage](#-usage)  
4. [Acknowledgements](#-acknowledgements)  
5. [License](#-license)

---

## 🚀 C++ Summary

A quick reference of key C++ topics from syntax basics to advanced features. For full details, see [C++_Summary.pdf](C++_Summary.pdf).

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

### 2. Compile Example

```bash
g++ -std=c++17 -Wall -Wextra example.cpp -o example
./example
```

---

## 🛠️ Makefile Guide

An introduction to automating builds in C/C++ projects using Makefiles. For full details, see [Makefile_guide.pdf](Makefile_guide.pdf).

### 1. What is a Makefile?

A plain-text file defining build targets, dependencies, and shell commands. Automates compilation, linking, and cleaning.

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

### 4. Common Symbols

| Symbol | Description                        |
|--------|------------------------------------|
| `$@`   | Target name                        |
| `$^`   | All prerequisites                  |
| `$<`   | First prerequisite                 |

### 5. Cleaning Up & Phony Targets

```makefile
.PHONY: clean all

all: $(TARGET)

clean:
	rm -f $(OBJS) $(TARGET)
```

### 6. Working with Libraries

- **Static**: `ar rcs libmylib.a mylib.o` then `g++ main.o -L. -lmylib -o main`  
- **Shared**: `g++ -fPIC -shared util.cpp -o libutil.so` then `g++ main.cpp -L. -lutil -Wl,-rpath=. -o main`

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

## ⚙️ Usage

1. **Compile C++ Samples:**  
   `g++ -std=c++17 -Wall -Wextra example.cpp -o example`  
2. **Build with Make:**  
   `make` or `make app`  
3. **Clean:**  
   `make clean`

---

## 🙏 Acknowledgements

Created by Shachar Tsrafati using:

- GeeksforGeeks tutorials and articles  
- Official C++ reference documentation  
- Various online tutorials  
- Coursework materials from Ariel University

---

## 📜 License

Free to use and adapt for educational purposes. Verify examples and report improvements.

