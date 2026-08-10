# Code Optimizer

A C++ static analysis and code optimization tool that detects and eliminates **dead code**, including unreachable functions and unused variables, using **control-flow and reachability analysis**.

## 🚀 Overview

Code Optimizer analyzes C++ source code to identify code that can never be executed or is no longer required.

The project focuses on improving code quality and reducing unnecessary code by applying static-analysis techniques to determine which parts of a program are reachable and which can safely be removed.

### Key Capabilities

* 🔍 Detects unreachable functions
* 🧹 Identifies unused variables
* 🧠 Performs control-flow and reachability analysis
* ✂️ Removes detected dead code
* ⚡ Helps reduce binary size
* 📈 Improves compilation efficiency
* 🖥️ Provides a user-friendly interface for working with the optimizer

## 🛠️ Technologies Used

* **C++**
* **Static Analysis**
* **Control Flow Analysis**
* **Reachability Analysis**
* **Object-Oriented Programming**
* **Qt** — GUI

## 🏗️ How It Works

The optimizer follows a static-analysis pipeline:

```text
       C++ Source Code
              │
              ▼
       ┌─────────────┐
       │   Analysis  │
       └──────┬──────┘
              │
              ▼
     Control Flow Analysis
              │
              ▼
     Reachability Analysis
              │
       ┌──────┴──────┐
       │             │
       ▼             ▼
 Reachable       Unreachable
   Code              Code
       │             │
       │             ▼
       │       Dead Code Detection
       │             │
       │             ▼
       │        Code Removal
       │
       └──────┬──────┘
              ▼
       Optimized Code
```

## 📊 Optimization Results

The optimizer was tested against C++ codebases and benchmarks.

| Metric                   |                      Result |
| ------------------------ | --------------------------: |
| Binary size reduction    |               Up to **25%** |
| Compile-time improvement |              Around **20%** |
| Analysis                 | Control flow & reachability |
| Language                 |                         C++ |

> Results depend on the structure and amount of dead code present in the input program.

## 💻 Getting Started

### Prerequisites

Make sure you have:

* A C++ compiler supporting modern C++
* CMake
* Qt development libraries

### Clone the Repository

```bash
git clone https://github.com/rohanchandrajwar/Code-Optimizer.git
cd Code-Optimizer
```

### Build

```bash
mkdir build
cd build
cmake ..
cmake --build .
```

### Run

After building the project, launch the generated executable:

```bash
./Code-Optimizer
```

On Windows, run the generated `.exe` file from the build directory.

## 📁 Project Structure

```text
Code-Optimizer/
│
├── src/                 # Core optimizer implementation
├── include/             # Header files
├── gui/                 # Qt interface
├── tests/               # Test cases
├── CMakeLists.txt       # Build configuration
└── README.md
```

> Adjust the directory names above if your repository uses a different structure.

## 🔬 Example

### Before Optimization

```cpp
void usedFunction() {
    // Required code
}

void unusedFunction() {
    // Never called
}

int main() {
    usedFunction();

    int unusedVariable = 100;

    return 0;
}
```

### After Optimization

```cpp
void usedFunction() {
    // Required code
}

int main() {
    usedFunction();

    return 0;
}
```

The optimizer identifies `unusedFunction()` and `unusedVariable` as dead code and removes them when they satisfy the tool's analysis criteria.

## 🎯 What I Learned

This project provided practical experience with:

* Static code analysis
* Control-flow graphs
* Reachability analysis
* Dead-code detection
* C++ program analysis
* Code transformation
* Performance optimization
* Building a GUI using Qt
* Designing software that combines analysis with a user interface

## 🔮 Future Improvements

Potential improvements include:

* [ ] More advanced dead-code detection
* [ ] Better handling of complex C++ constructs
* [ ] Control-flow graph visualization
* [ ] Additional optimization passes
* [ ] Support for larger C++ projects
* [ ] Automated benchmark reporting
* [ ] Integration with build systems
* [ ] Command-line interface
* [ ] Improved error handling
