## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=1;i<=n;i++) {
		for(int j=1;j<=n-i;j++) {
			std::cout << " ";
		}
		for(int j=0;j<2*i - 1;j++) {
			std::cout << "*";
		}
		std::cout << std::endl;
	}

	for(int i=n;i>=1;i--) {
		for(int j=1;j<=n-i;j++) {
			std::cout << " ";
		}
		for(int j=0;j<2*i - 1;j++) {
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
   ***
  *****
 *******
*********
*********
 *******
  *****
   ***
    *
```

In this code:

- We need to print two mirrored pyramid patterns of height `n`.
- The first half of the code (the first loop) creates the upper half of the pyramid pattern:
	- The outer loop `i` runs from (`1` to `n`), this will handle the height of the pattern.
	- The first inner loop `j`  runs from (`1` to `n-i` ) creates the necessary white-spaces before each row of asterisks to maintain the pyramid shape.
		- The number of white-spaces decreases by `1` after each iteration of the outer loop.
	- The second inner loop `j` runs from (`0` to `2*i-1`) creates the actual row of asterisks.
		- The number of asterisks in each row increases by `2` after each iteration of the outer loop.
- The second half of the code (the second loop) creates the bottom half of the pyramid pattern, which is simply a mirror image of the upper half:
	- The outer loop `i` runs from (`n` to `1`), this will handle the height of the pattern.
	- The first inner loop `j`  runs from (`1` to `n-i` ) creates the necessary white-spaces before each row of asterisks to maintain the pyramid shape.
		- The number of white-spaces decreases by `1` after each iteration of the outer loop.
	- The second inner loop `j` runs from (`0` to `2*i-1`) creates the actual row of asterisks.
		- The number of asterisks in each row increases by `2` after each iteration of the outer loop.
- In the end, the two mirrored pyramid patterns are displayed on the console.

---