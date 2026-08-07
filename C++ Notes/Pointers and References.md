## Pointers
- a pointer is a number that stores a memory address
- types are used to explain what type the pointer points to
- pointers don't have to be valid or can be `NULL`
- pointers can point to other pointers
- declared with a type and a `*`
## The Ampersand Operator
- used in front of a variable to give the pointer to where that variable is stored in memory
### Example
```cpp
#include <iostream>

int main()
{
	int var = 5;
	void* ptr = &var;

	std::cout << "Address: " << ptr << std::endl;

	return 0;
}
```
- returns a hexadecimal value
## The Asterisk
- used in front of a pointer to read what is stored in that memory address
### Example
```cpp
#include <iostream>

int main()
{
	int var = 5;
	void* ptr = &var;

	std::cout << "Address: " << ptr << std::endl;
	std::cout << "Value: " << *ptr << std::endl;

	return 0;
}
```
- returns a hexadecimal value
-  **Dereferencing** - take the value stored given a memory address using `*ptr`
## The Memset Function
- fill variables in the **heap**
1. pointer
2. value
3. size
### Example
```cpp
#include <iostream>

int main()
{
	// reserve 8 bytes of memory and give me the pointer to that spot
	char* buffer = new char[8];
	
	// fill that spot with zeros
	memset(buffer, 0, 8);
	
	// delete data in that spot so it can be used for other things
	delete[] buffer;

return 0;
}
```
## References
- alias existing variable
- can't be `NULL` or `0` like pointers
- are not variables themselves
- references *cannot be changed*
- references *cannot be declared*
- defined with a type and an `&`
### Example
```cpp
#include <iostream>

int main()
{
	int a = 5;
	
	// create an alias
	int& ref = a;
	
	// change a
	ref = 2;
	
	std::cout << a << std::endl;
	
	b = 8;
	ref = b;
	
	std::cout << "a: " << a << " b: " << b << std::endl;

return 0;
}
```

```bash
2
a: 8 b: 8
```
### Use Case

Consider an `Increment` function that should add one to a variable
```cpp
#include <iostream>

void Increment(int value)
{
	value++;
}

int main()
{
	int a = 5;
	Increment(a);
	std::cout << a << std::endl;
	
	return 0;
}

```

```bash
5
```
- `Increment` simply defines an entirely new variable that is one greater than `a`, leaving `a unchanged`
```cpp
#include <iostream>

void Increment(int* value)
{
	// dereference the address, and add one to it
	(*value)++;
}

int main()
{
	int a = 5;
	Increment(&a);
	std::cout << a << std::endl;
	
	return 0;
}

```
```bash
6
```
- `Increment` now takes in a memory address and writes to that memory address to increment it by one, changing `a`
```cpp
#include <iostream>

void Increment(int& value)
{
	value++;
}

int main()
{
	int a = 5;
	Increment(a);
	std::cout << a << std::endl;
	
	return 0;
}

```
```bash
6
```
- `Increment` takes in a reference to a variable or its alias, and adds one, changing the variable
- does exactly the same thing as the second version, but in a cleaner style
## [[Loops]]