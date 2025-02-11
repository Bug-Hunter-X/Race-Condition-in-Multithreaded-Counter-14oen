# Race Condition in Multithreaded Counter

This repository demonstrates a classic race condition bug in Java.  Two threads concurrently increment a shared counter, leading to an inaccurate final count. The `Counter` class represents a simple counter, and the `Main` class creates two threads that concurrently increment the counter.

## How to Reproduce

1. Compile and run the `Main.java` file.
2. Observe that the final count is often less than 20000, even though each thread attempts to increment the counter 10000 times.

## Solution

The solution involves using atomic operations or synchronization mechanisms (like locks) to ensure that the increment operation is atomic.  The solution provides a fixed version using `AtomicInteger`.