## Introduction

A function in C++ is a self-contained block of code that performs a specific task. Functions can take input parameters, perform some operations, and return an output. Functions can also be reused multiple times throughout a program, making the code more organized an easier to maintain.

There are two types of functions:

1. **Standard Library Functions:** Predefined in C++.
2. **User-defined Functions:** created by users.

### cpp Function Declaration

_Syntax:_

```cpp
returnType functionName (parameter1, parameter2, ...) {
	// function body
}
```

Example 1.8.1:

```cpp
#include <iostream>

int addNumbers(int x, int y) {
	int result = x + y;
	return result;
}

int main() {
	int a = 10;
	int b = 20;
	int sum = addNumbers(a, b);
	std::cout << "The sum of " << a << " and " << b << " is: " << sum << std::endl;
	return 0;
}
```

**Output:**

```
The sum of 10 and 20 is: 30
```

In this code:

- The function `addNumbers` takes two `int` parameters `x` and `y`.
- The function then adds them together and returns the result.
- In the `main` function, the values of `a` and `b` are passed to the `addNumbers` function.
- The result is stored in the variable `sum`.
- The `sum` is then printed to the console.

---
### Function Prototype

In C++, the code of function declaration should be before the function call. However, if we want to define a function after the function call, we need to use the function prototype.

_Syntax:_

```cpp
// function prototype
returnType functionName(dataType1, dataType2, ...);

int main() {
	// calling the function before declaration
	functionName(dataType1, dataType2, ...);

	return 0;
}

// function definition
returnType functionName(dataType1, dataType2, ...) {
	... .. ...
	... .. ...
}
```

The prototype provides the compiler with information about the function name and its parameters. That's why we can use the code to call a function before the function has been defined.

---
### Passing by value and Passing by reference

In C++, when a function is called, you can pass parameters to the function in two ways:

1. by value.
2. by reference.

Passing by value means that a copy of the actual parameter is made, and the function operates on the copy. Changes made to the parameter within the function are not reflected in the calling code.

Passing by reference means that the function operates directly on the original parameter. Changes made to the parameter within the function are reflected in the calling code.

Example 1.8.2:

```cpp
#include <iostream>

void addOne (int x) {
	x++;
}

int main() {
	int num = 10;
	addOne(num);
	std::cout << "The value of num is: " << num << std::endl;
	return 0;
}
```

**Output:**

```
The value of num is: 10
```

In this code:

- The function `addOne` takes an `int` parameter `x` and increments it by `1`.
- In the `main` function, the value of `num` is passed to the `addOne` function.
- However, after the function call, the value of `num` remains unchanged, as the function operates on a copy of `num`.

Example 1.8.3:

```cpp
#include <iostream>

void addOne (int &x) {
	x++;
}

int main() {
	int num = 10;
	addOne(num);
	std::cout << "The value of num is: " << num << std::endl;
	return 0;
}
```

**Output:**

```
11
```

In this code:

- The function `addOne` takes an `int` reference parameter `x` and increments it by `1`.
- In the `main` function, the value of `num` is passed to the `addOne` function.
- After the function call, the value of `num` is incremented by `1`, as the function operates directly on `num`.

Example 1.8.4:

```cpp
#include <iostream>
using namespace std;

/* Apply equation to parameters passed by value
 * Z = 10*X + 20*Y
 */
int FuncVal(int x,int y)
{
	x *= 10;
	y *= 20;
	int z = x + y;
	return z;
}

/* Apply equation to parameters passed by reference
 * Z = 10*X + 20*Y
 */
 int FuncRef(int* x,int* y)
{
	(*x) *= 10;
	(*y) *= 20;
	int z = (*x) + (*y);
	return z;
}


int main(){
	int x1, x2, y1, y2;
	cout << "Enter x1 value: ";
	cin >> x1;
	cout << endl;
	
	cout << "Enter y1 value: ";
	cin >> y1;
	cout << endl;
	
	cout << "Enter x2 value: ";
	cin >> x2;
	cout << endl;
	
	cout << "Enter y2 value: ";
	cin >> y2;
	cout << endl;
	
	cout << "Passing x1 & y1 by value: (Z = 10*X + 20*Y)" << endl;
	cout << "Z = " << FuncVal(x1, y1) << endl << endl;
	cout << "x1 & y1 values after passing them by value: " << endl;
	cout << "x1 = " << x1 << "     " << "y1 = " << y1 << endl;
	cout << "----------------------------------------------------" << endl;
	
	cout << "Passing x2 & y2 by reference: (Z = 10*X + 20*Y)" << endl;
	cout << "Z = " << FuncRef(&x2, &y2) << endl << endl;
	cout << "x2 & y2 values after passing them by reference: " << endl;
	cout << "x2 = " << x2 << "     " << "y2 = " << y2 << endl;
	cout << "----------------------------------------------------" << endl;
	
	return 0;
}
```

**Output:**

```
Enter x1 value: 1

Enter y1 value: 1

Enter x2 value: 1

Enter y2 value: 1

Passing x1 & y1 by value: (Z = 10*X + 20*Y)
Z = 30

x1 & y1 values after passing them by value: 
x1 = 1     y1 = 1
----------------------------------------------------
Passing x2 & y2 by reference: (Z = 10*X + 20*Y)
Z = 30

x2 & y2 values after passing them by reference: 
x2 = 10     y2 = 20
----------------------------------------------------
```

In this code:

- There are two functions, `FuncVal` and `FuncRef`, that perform the same mathematical operation `(Z = 10X + 20Y)`.
- The only difference between them is how they receive their parameters.
- `FuncVal` receives it parameters by value, which means that it receives a copy of the original values and any changes made to the parameters in the function won't affect the original values outside the function.
- `FuncRef` receives its parameters by reference, meaning it operates on the original values, so any changes made to the parameters in the function will affect the original values outside the function.
- In the `main` function, the user inputs 4 values, `x1`, `y1`, `x2`, and `y2`.
- Then, the program calculates the value of `z` using both functions, `FuncVal` and `FuncRef`, and prints the results along with the values of `x1`, `y1`, `x2` and `y2` after passing them to the functions.
- This demonstrates the difference between passing by value and passing by reference.

---