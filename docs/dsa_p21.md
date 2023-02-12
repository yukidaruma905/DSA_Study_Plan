## Solution

```cpp
#include <iostream>

int n= 5;

int main() {
	for(int i=0;i<n;i++) {
		for(int j=0;j<n;j++) {
			if(i==0 || i==n-1) {
				std::cout << "*";
			}
			else if(j==0 || j==n-1) {
				std::cout << "*";
			}
			else {
				std::cout << " ";
			}
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
*****
*   *
*   *
*   *
*****
```

In this code:

- The first line defines the variable `n` with the value `n`. This value determines the size of the rectangle shape.
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from `0` to `n-1` (`0` to `4`), and the inner loop `j` runs from `0` to `n-1` (`0` to `4`) for each iteration of the outer loop.
	- For each iteration of the inner loop, an `if` statement is used to determine what to print.
		- If `i` is equal to `0` or `n-1`, meaning it is the first or last row, the program will output an asterisk.
		- If `j` is equal to `0` or `n-1`, meaning it is the first or last column, the program will output an asterisk
		- In all other cases, the program outputs a space.
	- After the inner loop finishes, the program outputs a newline character to move to the next row.
- The program continues this process until all iterations of the outer loop are finished.

---