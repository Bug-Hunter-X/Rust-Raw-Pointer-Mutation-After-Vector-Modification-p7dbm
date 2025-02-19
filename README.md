# Rust Raw Pointer Mutation Bug

This repository demonstrates a subtle bug that can occur in Rust when using raw pointers to modify a vector after the vector's internal structure has changed.  The code attempts to modify the first element of a vector using a raw pointer obtained via `as_mut_ptr()`. However, subsequent operations on the vector (like pushing new elements) can invalidate the pointer, leading to unpredictable behavior or crashes.

The solution demonstrates how to safely work with raw pointers by ensuring that memory is managed correctly.