## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=0;i<n;i++) {
		for(int j=0;j<=i;j++) {
			std::cout << i+1;
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
1
22
333
4444
55555
```

In this code:

- Like the previous two programs, this one also prints a right-triangle pattern, but instead of asterisks (`*`) or numbers, it prints the current value of the outer loop variable `i+1`.
- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from `0` to `n-1` (`0` to `4`), this will handle the height of the pattern, and the inner loop `j` runs from `0` to `i` (`0` to `i`) for each iteration of the outer loop.
- Inside the inner loop, the statement `std::cout << i+1;` prints the value of `i+1` to the console (the number of the current row we are in).
	- when the algorithm is running in the second row `i=2`, we need to print the number of the row, `i+1=2` time to the console `2 2`.
	- when the algorithm is running in the third row `i=3`, we need to print the number of the row, `i+1=3` time to the console `3 3 3`.
- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- This process repeats until both loops have finished executing, and a right-triangle pattern of numbers `1` to `5` is printed to the console.

---