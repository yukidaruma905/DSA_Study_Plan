## Introduction

In computer science, time complexity is a fundamental concept that measures the amount of time an algorithm takes to run as a function of the size of its input data.

This is an important aspect of algorithm design and analysis, as it helps us determine the efficiency of different algorithms and choose the best one for a particular problem. Understanding time complexity is key to creating efficient and scalable software systems.

Time complexity is often expressed using `Big O Notation`, which provides an upper bound on the growth of the running time as the size of the input data increases. The notation describes the rate at which the running time grows relative to the size of the input. For example, if an algorithm has a time complexity of `O(n)`, it means that its running time is proportional to the size of the input data.

---
### The Constant Time Complexity

_Symbol:_ `O(1)`

The running time does not depend on the size of the input data and remains constant, regardless of how large the input is.

<figure markdown>
![image](constant_time_complexity_dark.svg#only-dark)
![image](constant_time_complexity_light.svg#only-light)
    <figcaption>Constant Time Complexity Flowchart</figcaption>
</figure>

_Common Uses:_

- Accessing an element in an array using an index.
- Retrieving the value of a constant or a simple mathematical expression.
- Checking if a number is odd or even.

---
### The Logarithmic Time Complexity

_Symbol:_ `O(log(n))`

The running time grows logarithmic-ally with the size of the input data. This is often the case for algorithms that divide the input data in half at each step.

<figure markdown>
![image](log_time_complexity_dark.svg#only-dark)
![image](log_time_complexity_light.svg#only-light)
    <figcaption>Logarithmic Time Complexity Flowchart</figcaption>
</figure>

_Common Uses:_

- Binary Search in a sorted array.
- Finding the lower bound of an element in a sorted array using binary search.
- Performing operations on binary trees.

---
### The Linear Time Complexity

_Symbol:_ `O(n)`

The running time grows linearly with the size of the input data. This is often the case for algorithms that process each item in the input data once.

<figure markdown>
![image](linear_time_complexity_dark.svg#only-dark)
![image](linear_time_complexity_light.svg#only-light)
    <figcaption>Linear Time Complexity Flowchart</figcaption>
</figure>

_Common Uses:_

- Iterating through an array and performing an operation on each element.
- Finding the maximum or minimum value in an array.
- Sequentially searching for an element in an unsorted array.

---
### The Log-linear Time Complexity

_Symbol:_ `O(n*log(n))`

The running time grows at a rate that is between linear and logarithmic. This is often the case for algorithms that divide the input data in half and process each item once, such as the merge sort algorithm.

<figure markdown>
![image](log_linear_time_complexity_dark.svg#only-dark)
![image](log_linear_time_complexity_light.svg#only-light)
    <figcaption>Log-linear Time Complexity Flowchart</figcaption>
</figure>

_Common Uses:_

- Sorting algorithms like Merge Sort, Quick Sort.
- Finding the closest pair of points in a set of points.
- Finding the longest increasing sub-sequence in a sequence.

---
### The Quadratic Time Complexity

_Symbol:_ `O(n^2)`

The running time grows at a rate that is proportional to the square of the size of the input data. This is often the case for algorithms that compare each item in the input data with every other item.

<figure markdown>
![image](quadratic_time_complexity_dark.svg#only-dark)
![image](quadratic_time_complexity_light.svg#only-light)
    <figcaption>Quadratic Time Complexity Flowchart</figcaption>
</figure>

_Common Uses:_

- Simple sorting algorithms like Bubble Sort, Insertion Sort.
- Checking all possible combinations of pairs in an array.
- Finding all sub-arrays in an array.

---
### The Exponential Time Complexity

_Symbol:_ `O(2^n)`

The running time grows at a rate that is proportional to two raised to the power of the size of the input data. This is often the case for algorithms that solve problems by considering all possible combinations of items.

<figure markdown>
![image](exponential_time_complexity_dark.svg#only-dark)
![image](exponential_time_complexity_light.svg#only-light)
    <figcaption>Exponential Time Complexity Flowchart</figcaption>
</figure>

_Common Uses:_

- Generating all subsets of a set.
- Solving the traveling salesman problem.
- Finding all possible solutions to the n-queens problem.

---
### The Factorial Time Complexity

_Symbol:_ `O(n!)`

<figure markdown>
![image](factorial_time_complexity_dark.svg#only-dark)
![image](factorial_time_complexity_light.svg#only-light)
    <figcaption>Factorial Time Complexity Flowchart</figcaption>
</figure>

_Common Uses:_

- Generating all permutations of a set.
- Solving the n-puzzle problem.
- Calculating the number of possible Hamiltonian cycles in a graph.

---
### Summary

Time complexity is an essential concept in computer science that helps us determine the efficiency of algorithms and choose the best one for a particular problem. By understanding time complexity and its various forms, we can design algorithms that are both efficient and scalable, which is crucial for creating successful software systems.

<figure markdown>
![image](full_time_complexity_dark.svg#only-dark)
![image](full_time_complexity_light.svg#only-light)
    <figcaption>Full Time Complexity Flowchart</figcaption>
</figure>

---