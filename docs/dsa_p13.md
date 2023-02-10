## Solution

```cpp
#include <iostream>

int n=5, cnt=1;

int main(){
	for(int i=0;i<n;i++) {
		for(int j=0;j<=i;j++) {
			std::cout << cnt++ << " ";
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
1 
2 3 
4 5 6 
7 8 9 10 
11 12 13 14 15 
```

In this code:

- First, we define two integers `n` and `cnt`, with values `5` and `1` respectively. `n` will be used to control the number of rows for the two triangles and `cnt` is a counter variable that will be used to print the numbers in the triangle pattern.
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`0` to `n-1`), this will handle the height of the pattern, and the inner loop `j` runs from (`0` to `i`) for each iteration of the outer loop.
- The code `std::cout << cnt++ << " ";` prints the value of `cnt` and then increments `cnt` by `1`. This will print the numbers in ascending order in the triangle pattern.
- After that, the code `std::cout << std::endl;` is executed to print a newline character and move to the next row of the triangle pattern.
- The loop continues to run until all `n` iterations are completed.

---