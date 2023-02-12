## Solution

```cpp
#include <iostream>

int n=7;
int a = (n+1)/2;
int cnt;
int temp;

int main(){
	for(int i=0;i<a;i++) {
		cnt = i;
		temp=0;
		
		for(int j=0;j<a;j++) {
			std::cout << a-temp;
			if(cnt > 0) {
				temp++;cnt--;
			}
		}
		cnt = a-1-i;
		
		for(int j=0;j<a-1;j++) {
			if(cnt > 0) {
				cnt--;
			}
			else {
				temp--;
			}
			std::cout << a-temp;
		}
		std::cout << std::endl;
	}

/* ---------------------------- */

	for(int i=a-2;i>=0;i--) {
		cnt = i;
		temp=0;
		
		for(int j=0;j<a;j++) {
			std::cout << a-temp;
			if(cnt > 0) {
				temp++;cnt--;
			}
		}
		cnt = a-1-i;
		
		for(int j=0;j<a-1;j++) {
			if(cnt > 0) {
				cnt--;
			}
			else {
				temp--;
			}
			std::cout << a-temp;
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
4444444
4333334
4322234
4321234
4322234
4333334
4444444
```

In this code:

- First, the value of `n` is defined as `7`. This means the output will be a square of size `7x7`.
- Next, `a` is defined as `(n+1)/2`, which means `a` will be equal to `4`.
- `cnt` and `temp` are defined as `int` variables with the initial value of `0`.
	- `cnt` is used as a counter.
	- `temp` is used to keep track of the value that is to printed in each iteration.
- The `main` function starts with two nested `for` loops. The outer `for` loop runs `a` times, and the inner `for` loop runs `a` times as well. The purpose of these loops is to print each layer of the square.
- Inside the inner loop, `a-temp` is printed.
	- `temp` starts at `0` and increases by `1` in each iteration. So the first iteration will print `a`, which is `4`.
- The value of `cnt` is also checked in each iteration. If `cnt` is greater that `0`, then `temp` is increased by `1` and `cnt` is decremented by `1`.
- The second inner loop runs `a-1` times, inside this loop, `cnt` is decremented by `1` in each iteration.
	- If `cnt` is not greater than `0`, then `temp` is decremented by `1`. The value of `a - temp` is then printed.
- When the two inner loops are finished, a newline character is printed using `std::endl`.
- The second outer loop runs `a - 2` times, and each time the same process is repeated in order to print the second half of the pattern.

---