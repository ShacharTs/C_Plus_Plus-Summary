# 📘 C++ & Makefile Beginner Summaries  
**Author: Shachar Tsrafati**

A concise, student-authored reference covering both core C++ topics and build automation tools used in C++ development.  
This repository includes summaries, guides, and installation instructions intended for beginners and intermediate students.

---

# 📚 Contents

1. [C++ Summary](#c-summary)  
2. [Makefile Guide](#makefile-guide)  
3. [CMake & Clang-Tidy Guide](#cmake-clang-tidy-guide)  
4. [CMake & Clang-Tidy Installation](#cmake-clang-tidy-installation)  
5. [Usage](#usage)  
6. [Credits](#credits)  
7. [License](#license)

---

<a name="c-summary"></a>
# 🚀 C++ Summary

A quick reference of key C++ topics from syntax basics to advanced features.

For full details see:

📄 **C++_Summary.pdf**

---

## Topics Covered

- Variables & Data Types  
- Strings & `using namespace std`  
- `const` Qualifier  
- Namespaces  
- Typedefs & Aliases  
- Input/Output (`std::cin`, `std::cout`)  
- Control Flow (`if` / `else`, `switch`, loops)  
- Functions & Overloading  
- Header Files & Includes  
- Structs & Classes  
- Constructors & Destructors  
- Arrays & Raw Pointers  
- Static Members & Methods  
- RAII & Smart Pointers (`unique_ptr`, `shared_ptr`, `weak_ptr`)  
- Exception Handling (`try` / `catch`)  
- Composition & Initialization  
- Friend Functions & Operator Overloading  
- Literals & Type Conversions  
- Copy Control (Shallow vs Deep)  
- `explicit` Keyword  
- Inheritance & Polymorphism  
- Casting (`static_cast`, `dynamic_cast`, `reinterpret_cast`)  
- Templates (Function, Class, Specialization, Metaprogramming)  
- STL Containers & Algorithms (`tuple`, `vector`, `set`, `map`, iterators)

---

## Compile Example

```bash
g++ -std=c++17 -Wall -Wextra example.cpp -o example
./example
```

---

<a name="goals"></a>
# 🎯 Next Goals to Add to the Summary (not promising)

Possible topics to expand in the future:

- Lambda expressions  
- Move semantics & rvalue references  
- `constexpr` and `noexcept`  
- Type inference (`auto`, `decltype`)  
- `nullptr` and scoped enums (`enum class`)  
- Modern C++ utilities:
  - `std::optional`
  - `std::variant`
  - `std::any`
  - `std::filesystem`
- Structured bindings  
- Range-based algorithms with lambdas  
- Concurrency support:
  - `<thread>`
  - `<mutex>`
  - `<future>`
  - atomics

---

<a name="makefile-guide"></a>
# 🛠️ Makefile Guide

For a full Makefile reference see:

📄 **Makefile_guide.pdf**

### Topics Covered

- Notes and introduction to Makefiles  
- How to create a Makefile  
- Basic Makefile structure  
- Shortcuts and variables  
- Symbol shortcuts and wildcards  
- Clean targets  
- Phony targets  
- Working with libraries  
- Echo messages  
- Recursive Make  
- Conditional syntax (`if` / `else`)

---

<a name="cmake-clang-tidy-guide"></a>
# ⚙️ CMake & Clang-Tidy Guide

This guide explains how to configure and use **CMake together with Clang-Tidy** for C++ projects.

📄 **How to use CMake And Tidy.pdf**

The document includes:

- What **CMake** is and how it works  
- Why build system generators are useful  
- How to write a `CMakeLists.txt` file  
- Using **Clang-Tidy** for static code analysis  
- Example CMake configuration for C++ projects  
- Building programs using default generators or Ninja  
- Understanding where compiled executables are generated  

---

<a name="cmake-clang-tidy-installation"></a>
# 💻 CMake & Clang-Tidy Installation

Step-by-step installation instructions for development environments.

📄 **Cmake and TIdy Guide.pdf**

This document covers installation on:

### Windows
- Installing **CMake**
- Installing **LLVM / Clang-Tidy**
- Adding tools to the system PATH
- Verifying installation

### macOS
- Installing using **Homebrew**
- Adding LLVM tools to PATH
- Verifying environment configuration

### Linux
- Installing using package managers such as `apt`
- Verifying the installation

---

<a name="usage"></a>
# ⚙️ Usage

### Compile C++ Programs

```bash
g++ -std=c++17 -Wall -Wextra example.cpp -o example
```

Run:

```bash
./example
```

---

### Build with Make

```bash
make
```

or

```bash
make app
```

Clean build artifacts:

```bash
make clean
```

---

### Build with CMake

```bash
cmake -S . -B build
cmake --build build
```

---

<a name="credits"></a>
# 🙏 Credits

Created by **Shachar Tsrafati** using:

- GeeksforGeeks tutorials and articles  
- Official C++ reference documentation  
- Various online tutorials  
- Coursework materials from Ariel University  

---

<a name="license"></a>
# 📜 License

Free to use and adapt for educational purposes.

Please verify examples before production use and feel free to report improvements.
