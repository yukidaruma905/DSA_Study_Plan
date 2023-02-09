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

	for(int i=n-1;i>=1;i--) {
		for(int j=1;j<=i;j++) {
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
****
***
**
*
```

In this code:

- We need to print two mirrored right-triangle patterns of height `n`.
- The first half of the code (the first loop) creates the upper half of the right-triangle pattern, where the number of asterisks increases in each row until it reaches the maximum value of `n`:
	- The outer loop `i` runs from (`0` to `n-1`), this will handle the height of the pattern, and the inner loop `j` runs from `0` to `i` (`0` to `i`) for each iteration of the outer loop.
	- Inside the inner loop, the statement `std::cout << "*";` prints an asterisk to the console.
		- when the algorithm is running in row `i=2` the inner loop will print `2` asterisks.
		- when it runs in row `i=3` the inner loop will print `3` asterisks.
	- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- The second half of the code (the second loop) creates the lower half of the right-triangle pattern, where the number of asterisks decreases in each row until it reaches `1`:
	- The outer loop `i` runs from (`n-1` to `1`), this will handle the height of the pattern, and the inner loop `j` runs from (`1` to `i`) for each iteration of the outer loop.
	- Inside the inner loop, the statement `std::cout << "*";` prints an asterisk to the console.
		- when the algorithm is running in row `i=2` the inner loop will print `4` asterisks.
		- when it runs in row `i=3` the inner loop will print `3` asterisks, and so on.
	- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- In the end, we will get two mirrored right-triangle pattern printed to the console.

---