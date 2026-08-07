## For Loop
1. definition
2. condition
3. code to execute at the end of the loop for each iteration

- all arguments are *optional*
- if the condition is not specified, the loop will run *indefinitely*
### Example
```cpp
#include <iostream>

int main()
{
	int sum = 0;
	
	for (int i = 1; i < 11; i++)
	{
	sum += i;
	}
	
	std::cout << "Sum: " << sum << std::endl;
	
	return 0;
}
```
## While Loop

1. condition
### Example
```cpp
#include <iostream>

int main()
{
	int sum = 0;
	int i = 1;
	
	while (i <= 10)
	{
		sum += i;
	}
	
	std::cout << "Sum: " << sum << std::endl;
	
	return 0;
}
```
## Do While Loop

- executes the code *at least once* even if the condition is false to begin with
### Example
```cpp
#include <iostream>

int main()
{
	do
	{
		std::cout << "This text will be printed once." << sum << std::endl;
	} while (0);
	
	return 0;
}
```
## Control Statements
### Continue
- `continue`
- skips to the next iteration
### Break
- `break`
- terminates the loop
### Return
- `return`
- returns a value