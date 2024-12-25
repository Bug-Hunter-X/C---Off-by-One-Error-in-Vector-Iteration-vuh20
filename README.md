# C++ Off-by-One Error in Vector Iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The error occurs when the loop condition incorrectly includes the index equal to the vector's size, leading to an attempt to access an element outside the valid range.

**Bug:** The `for` loop in `bug.cpp` iterates from `i = 0` to `i <= vec.size()`. This means the loop attempts to access `vec[vec.size()]`, which is one element past the last valid element. This results in undefined behavior, potentially crashing the program or producing unpredictable results.

**Solution:** `bugSolution.cpp` corrects the loop condition to `i < vec.size()`. This ensures that the loop iterates only over valid indices of the vector.

This example highlights the importance of carefully considering loop bounds when working with containers in C++.