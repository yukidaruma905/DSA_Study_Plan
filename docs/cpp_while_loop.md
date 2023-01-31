## Introduction

The `while` loop in C++ repeatedly executes a block of code as long as the specified condition is `true`.

### cpp while Loop

_Syntax:_

```cpp
while (condition) {
	// statement
}
```

Here:

- A `while` loop evaluates the `condition`.
- If the `condition` is `true`, the code inside the `while` loop is executed.
- The `condition` is evaluated again.
- This process continues until the `condition` is `false`.
- When the `condition` evaluates to `false`, the loop terminates.

<figure markdown>
![image](while_loop_statement_dark.svg#only-dark)
![image](while_loop_statement_light.svg#only-light)
    <figcaption>while Loop Statement Flowchart</figcaption>
</figure>

Example 1.7.1:

```cpp
#include <iostream>

int main() {
	int count = 1;
	while (count <= 5) {
		std::cout << count << " ";
		count++;
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

- The `while` loop continues to execute as long as `count` is less than or equal to `5`.
- The variable `count` is incremented inside the loop so that eventually the condition becomes false and the loop terminates.

---
### cpp do...while Loop

The `do...while` loop in C++ is similar to the `while` loop, but with one important difference: the block of code in a `do...while` loop is guaranteed to execute at least once.

_Syntax:_

```cpp
do {
	//statement
} while (condition);
```

Here:

- The body of the loop is executed at first. Then the `condition` is evaluated.
- If the `condition` evaluates to `true`, the body of the loop inside the `do` statement is executed again.
- The `condition` is evaluated once again.
- If the `condition` evaluates to `true`, the body of the loop inside the `do` statement is executed again.
- This process continues until the `condition` evaluates to `false`. Then the loop stops.

<figure markdown>
![image](do_while_loop_statement_dark.svg#only-dark)
![image](do_while_loop_statement_light.svg#only-light)
    <figcaption>do...while Loop Statement Flowchart</figcaption>
</figure>

Example 1.7.2:

```cpp
#include <iostream>

int main() {
	int count = 1;
	do {
		std::cout << count << " ";
		count++;
	} while (count <= 5);
	std::cout << std::endl;
	return 0;
}
```

**Output:**

```
1 2 3 4 5
```

In this code:

- The `do...while` loop will first execute the block of code inside the loop.
- Then it evaluates the condition.
	- If the condition is true, the loop will repeat.
	- If the condition is false, the loop will terminate.

---