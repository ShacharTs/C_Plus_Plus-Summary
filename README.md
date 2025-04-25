# 📘 C++ & Makefile Beginner Summaries  
**Author: Shachar Tsrafati**

A concise, student-authored reference covering both core C++ topics and comprehensive Makefile-based build automation. Ideal for beginners and intermediate learners preparing for coursework or quick refreshers during development.

---

## 📚 Contents

1. [C++ Summary](#c-summary)  
   - [Topics Covered](#topics-covered)  
   - [Compile Example](#compile-example)  
   - [Goals](#goals)
2. [Makefile Guide](#makefile-guide)  
3. [Usage](#usage)  
4. [Credits](#credits)  
5. [License](#license)

---

<a name="c-summary"></a>
## 🚀 C++ Summary

A quick reference of key C++ topics from syntax basics to advanced features. For full details, see [C++_Summary.pdf](C++_Summary.pdf).

### Topics Covered
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

### Compile Example
```bash
g++ -std=c++17 -Wall -Wextra example.cpp -o example
./example
```

<a name="goals"></a>
## 🎯 Next Goals to Add to the Summary (not promising)
- Next goals to add to the summary (not promising):
  - **Lambda expressions** for concise, inline functions
  - **Move semantics & rvalue references** for efficient resource transfers
  - **`constexpr` & `noexcept`** to enable compile-time evaluation and improved safety
  - **Type inference (`auto`, `decltype`)** to reduce code verbosity
  - **`nullptr` and scoped enums (`enum class`)** for safer code
  - **Standard library utilities** introduced in C++17/20: `std::optional`, `std::variant`, `std::any`, `std::filesystem`
  - **Structured bindings** and **range-based algorithms** with lambdas
  - **Concurrency support**: `<thread>`, `<mutex>`, `<future>`, and atomics
  - **Enhanced algorithms** from `<algorithm>` and ranges (C++20)

---

<a name="makefile-guide"></a>
## 🛠️ Makefile Guide

For a full Makefile reference, see [Makefile_guide.pdf](Makefile_guide.pdf).

**Topics Covered:**
- **Note**  
- **How to Create Makefile**  
- **Basic Makefile**  
- **Shortcuts**  
- **Symbol Shortcuts (Wildcards)**  
- **Clean**  
- **Phony Targets**  
- **Working with Libraries**  
- **Echo Messages**  
- **Recursive Make**  
- **Conditional Syntax (If-Else)**

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

---

