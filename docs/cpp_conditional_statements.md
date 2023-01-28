## Introduction

Conditional statements in C++ allow you to control the flow of a program based on certain conditions. The basic for of a conditional statement is an `if` statement. We use the `if` statement to run a block of code only when a certain condition is met.

There are three forms of `if...else` statements in C++.

1. `if` Statement.
2. `if...else` Statement.
3. `if...else if...else` Statement.

### cpp if Statement

*Syntax:*

```cpp
if (condition) {
	// body of if statement
}
```

The `condition` is a Boolean expression that is evaluated to either true or false.

- If the `condition` evaluates to `true`, the code inside the body of `if` is executed.
- If the `condition` evaluates to `false`, the code inside the body of `if` is skipped.

---

### cpp if...else Statement

_Syntax:_

```cpp
if (condition) {
	// block of code if condition is true
}
else {
	// block of code if condition is false
}
```

The `if...else` allows you to specify code that should be executed if the condition is false.

If the `condition` evaluates to `true`:

- the code inside the body of `if` is executed.
- the code inside the body of `else` is skipped from execution.

If the `condition` evaluates to `false`:

- the code inside the body of `if` is skipped from execution.
- the code inside the body of `else` is executed.

---

### cpp if...else if...else Statement

_Syntax:_

```cpp
if (condition1) {
	// code block 1
}
else if (condition2) {
	// code block 2
}
else {
	// code block 3
}
```

Here,

- If `condition1` evaluates to `true`, the `code block 1` is executed.
- If `condition1` evaluates to `false`, then `condition2` is evaluated.
- If `condition2` evaluates to `true`, the `code block 2` is executed.
- If `condition2` evaluates to `false`, the `code block 3` is executed.

---

### cpp Nested if...else

_Syntax:_

```cpp
// outer if statement
if (condition1) {
	// statements

	// inner if statement
	if (condition2) {
		// statements
	}
}
```

Here,

- If `condition1` evaluates to `true`, the statements inside the outer if will be executed and the `condition2` will be evaluated.
  - If `condition2` evaluates to `true`, the statements inside the inner if will be executed (Both outer and inner statements were executed).
  - If `condition2` evaluates to `false`, then the block will be skipped (Only outer statement were executed).
- If `condition1` evaluates to `false`, then the block will be skipped (No statement will be executed).

---

### Ternary Operator

C++ also provide a ternary operator `? :` which is a shorthand for `if...else` statement and it is used to make the code more readable.

_Syntax:_

```cpp
variable = (condition) ? value1 : value2;
```

The above line of code can be read as "if `condition` is `true` then assign `value1` to variable else assign `value2` to variable."

Example 1.3.1:

```cpp
#include <iostream>

int main(){
    int a = 5;
    int b = 10;
    int c;

    c = (a > b) ? a : b;
    std::cout << "c: " << c << std::endl;
    return 0;
}
```

**Output:**

```
c: 10
```

In this code:

- The program will compare the value of `a` and `b`.
- If the value of `a` is greater than `b`, then `c` will be assigned the value of `a`.
- Otherwise `c` will be assigned the value of `b`.

> **Note:** Ternary operator should be used with caution, as it can make the code harder to read and understand if overused or used in complex expressions.

Conditional statements are fundamental building block of many programs and they allow you to create more complex logic and decision making in your code.

---
