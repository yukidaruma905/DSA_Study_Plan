## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=0;i<n;i++) {
		for(int j=0;j<=i;j++) {
			std::cout << (char)('A' + j);
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
A
AB
ABC
ABCD
ABCDE
```

In this code:

- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`0` to `n-1`), this will handle the height of the pattern, and the inner loop `j` runs from (`0` to `i`) for each iteration of the outer loop.
- Inside the inner loop, the statement `std::cout << (char)('A' + j);` prints an ASCII code of the character that corresponds to `j`, and the `(char)` typecast converts the result to a character.
	- when the algorithm is running in the second row `i=2`, we need to print the character `'A'+j` that corresponds to the column number to the console `AB`.
	- when the algorithm is running in the third row `i=3`, we need to print the character `'A'+j` that corresponds to the column number to the console `ABC`.
- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- This process repeats until both loops have finished executing, and a right triangle pattern of `5` rows tall using characters from the alphabet is printed to the console.

---