<u>Quick links to navigate:</u>
- [[#Introduction]]
	- [[#cpp for Loop]]
	- [[#Ranged Based for Loop]]
	- [[#cpp Infinite for Loop]]

## Introduction

In C++, loops are a control flow statements that allows you to execute a block of code repeatedly for a given number of iterations.

---
### cpp for Loop

_Syntax:_

```cpp
for (initialization; condition; increment/decrement) {
	// code to be executed
}
```

- The `initialization` statement is executed only once, before the loop starts. It is used to initialize the loop control variable.
- The `condition` is a boolean expression that is evaluated before each iteration of the loop.
	- If the condition is true, the loop continues to execute.
	- If the condition is false, the loop exits.
- The `increment/decrement` statement is executed after each iteration of the loop. It is used to update the loop control variable.

<figure markdown>
![image](for_loop_statement_dark.svg#only-dark)
![image](for_loop_statement_light.svg#only-light)
    <figcaption>For Loop Statement Flowchart</figcaption>
</figure>

Example 1.6.1:

```cpp
for (int i = 1; i <= 10; i++) {
	std::cout << i << " ";
}
```

**Output:**

```
1 2 3 4 5 6 7 8 9 10
```

In this code:

- The loop starts with the initialization statement `int i = 1`, which initializes the loop control variable `i` to `1`.
- The condition `i <= 10` is checked before each iteration of the loop. As long as `i` is less than equal to `10`, the loop continues to execute.
- The increment statement `i++` is executed after each iteration of the loop, which increments the value of `i` by `1`.

---
### Ranged Based for Loop

The `ranged-based for loop` is  a new feature in C++11 that allows you to iterate over elements in an array or container with a simple and readable syntax. It uses a range-based expression to define the elements that the loop will operate on.

_Syntax:_

```cpp
for (element : collection) {
	// statements
}
```

- `element` is a variable that will hold each element in the collection.
- `collection` is the array or container to iterated.

Example 1.6.2:

```cpp
#include <iostream>

int main() {
	int arr[] = {1, 2, 3, 4, 5};
	for (int i : arr) {
		std::cout << i << " ";
	}
	std::cout << std::endl;

	return 0;
}
```

**Output:**

```
1 2 3 4 5
```

In this code:

- The ranged-base `for` loop is used to iterate over the elements in the `arr` array.
- The variable `i` is declared inside the loop to hold each element.
- The body of the loop prints out each element in the array.

---
### cpp Infinite for Loop

If the `condition` in a `for` loop is always `true`, it runs forever (_until memory is full_).

_Syntax:_

```cpp
// infinite for loop
for (true) {
	// block of code
}
```

---