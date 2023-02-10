## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=0;i<n;i++) {
		for(int j=0;j<=i;j++) {
			std::cout << ((i+j+1))%2;
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
1
01
101
0101
10101
```

In this code:

- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`0` to `n-1`), this will handle the height of the pattern, and the inner loop `j` runs from (`0` to `i`) for each iteration of the outer loop.
- The expression `((i + j + 1)) % 2` is used to determine the value to be printed in each position of the pattern
	- The expression `i + j + 1` returns the sum of the row number `i` and the column number `j`, plus `1`.
	- The result is then taken modulo `2`, which results in either `0` or `1`.
- For each iteration of the inner loop, the value of `((i + j + 1)) % 2` is printed to the console.
- After each inner loop finishes, a new line is printed to the console with `std::cout << std::endl;`.

---