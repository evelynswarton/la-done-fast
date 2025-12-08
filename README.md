# Linear Algebra Library

## Overview
A simple C++ linear algebra library for basic matrix and vector operations, designed for research purposes.

## Features
- Matrix and vector classes with basic arithmetic operations
- Linear system solving using LU decomposition
- Determinant calculation
- Matrix inversion
- Basic linear algebra operations (dot product, cross product)

## Dependencies
- C++11 or later

## Installation

### Using Git
```bash
git clone https://github.com/evelynswarton/eve_linalg
cd eve_linalg
make
```

### Without Git
Download the source code and build manually:
```bash
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make
```

## Usage

### Including the Library
```cpp
#include "eve_linalg/matrix.hpp"
#include "eve_linalg/vector.hpp"
```

### Basic Operations
```cpp
// Matrix creation
Matrix<double, 3, 3> A = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

// Vector creation
Vector<double, 3> v = {1, 2, 3};

// Matrix multiplication
Matrix<double, 3, 3> B = A * A;

// Solve linear system
Vector<double, 3> solve_system(const Matrix<double, 3, 3>& A, const Vector<double, 3>& b);

// LU Decomposition
auto [L, U] = lu_decompose(A);
```

### Solving Linear Systems
```cpp
// Create test matrix and vector
Matrix<double, 3, 3> A = {{2, -1, 0}, {-1, 2, -1}, {0, -1, 2}};
Vector<double, 3> b = {1, -2, 3};

// Solve the system
Vector<double, 3> solution = solve_linear_system(A, b);

// Output solution
std::cout << "Solution: " << solution << std::endl;
```

## API Documentation
See the `docs/` directory for complete documentation:
```bash
docs/
├── matrix.hpp
├── vector.hpp
└── lu_decomposition.hpp
```

## Examples
See the `examples/` directory for complete runnable examples:
```bash
examples/
├── matrix_operations.cpp
├── linear_system.cpp
└── eigenvalue_test.cpp
```                                                                                                                                                                         [0/201]

## License
This library is distributed under the MIT License. See `LICENSE` for details.

## Contact
For questions or issues, please contact:
- Email: me@evelynw.xyz
- GitHub: [evelynswarton](https://github.com/evelynswarton)

## Roadmap
- [ ] Add sparse matrix support
- [ ] Implement more advanced decompositions (QR, Cholesky)
- [ ] Add documentation for all functions
- [ ] Improve numerical stability

## Acknowledgments
- Thanks to the scientific computing community for foundational concepts

