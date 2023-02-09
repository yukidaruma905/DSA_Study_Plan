## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=0;i<n;i++) {
		for(int j=0;j<=i;j++) {
			std::cout << "*";
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
*
**
***
****
*****
```

In this code:

- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`0` to `n-1`), this will handle the height of the pattern, and the inner loop `j` runs from (`0` to `i`) for each iteration of the outer loop.
- Inside the inner loop, the statement `std::cout << "*";` prints an asterisk to the console.
	- when the algorithm is running in row `i=2` the inner loop will print `2` asterisks.
	- when it runs in row `i=3` the inner loop will print `3` asterisks.
- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- This process repeats until both loops have finished executing, and a right triangle pattern of asterisks `5` rows tall is printed to the console.

---