# 📘 C++ & Makefile Beginner Summaries  
**Author: Shachar Tsrafati**

A concise, student-authored reference covering both core C++ topics and comprehensive Makefile-based build automation. Ideal for beginners and intermediate learners preparing for coursework or quick refreshers during development.

---

## 📚 Contents

1. [C++ Summary](#c-summary)  
   1. [Topics Covered](#topics-covered)  
   2. [Compile Example](#compile-example)  
2. [Makefile Guide](#makefile-guide)  
   1. [Topic Covers](#Topics_Covered:)
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
- Control Flow (`if`/`else`, `switch`, loops)  
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

For a full Makefile reference, see [Makefile_guide.pdf](Makefile_guide.pdf).

**Topics Covered:**
- **What is a Makefile?**
- **Basic Example**
- **Variables & Patterns**
- **Common Symbols**
- **Cleaning & Phony Targets**
- **Working with Libraries**
- **Example Project Structure**

<a name="usage"></a></a>
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

