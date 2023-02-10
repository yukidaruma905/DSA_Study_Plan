## Solution

```cpp
#include <iostream>

int n=5,m=5;

int main(){
	for(int i=0;i<n;i++) {
		for(int j=0;j<=i;j++) {
			std::cout << (char)('A' + i);
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
A
BB
CCC
DDDD
EEEEE
```

In this code:

- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`0` to `n-1`), this will handle the height of the pattern, and the inner loop `j` runs from (`0` to `i`) for each iteration of the outer loop.
- Inside the inner loop, the statement `std::cout << (char)('A' + i);` prints an ASCII code of the character that corresponds to `i`, and the `(char)` typecast converts the result to a character.
	- when the algorithm is running in the second row `i=2`, we need to print  `'A'+i=B`, `i` time to the console `BB`.
	- when the algorithm is running in the third row `i=3`, we need to print `'A'+i=C`, `i` time to the console `CCC`.
- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- This process repeats until both loops have finished executing, and a right-triangle pattern of numbers `1` to `5` is printed to the console.
---