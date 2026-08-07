- all primary types are just numbers
- primary types can be used interchangeably since they are all numbers
## Integers

| Type    | Size (Bytes) | Description                          |
| ------- | ------------ | ------------------------------------ |
| `int`   | 4            | from -2,147,483,648 to 2,147,483,647 |
| `short` | 2            | from -32768 to 32768                 |

## Floating Point

| Type     | Size (Bytes) | Description               |
| -------- | ------------ | ------------------------- |
| `float`  | 4            | from 1.2e-38 to 3.4e38    |
| `double` | 8            | from 1.7e-308 to 1.7e+308 |

## Characters

| Type      | Size (Bytes) | Description                                                                                                                                                                            |
| --------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `char`    | 1            | store up to 256 characters according to their [ASCII codes](https://www.geeksforgeeks.org/computer-organization-architecture/what-is-ascii-a-complete-guide-to-generating-ascii-code/) |

## Boolean

| Type   | Size (Bytes) | Description                            |
| ------ | ------------ | -------------------------------------- |
| `bool` | 1            | is false for 0, true for anything else |
## Void

| Type   | Size (Bytes) | Description      |
| ------ | ------------ | ---------------- |
| `void` | 0            | absence of value |

## Auto
- `auto` will automatically deduce a type based on the definition of a variable
## Modifiers

| Name       | Descriptions                               |
| ---------- | ------------------------------------------ |
| `unsigned` | uses only positive numbers, doubling range |
| `long`     | increases range                            |
| `const`    | cannot be changed after assignment         |

## [[Classes and Structs]]
- classes and structs create their own unique types
### [[Pointers and References]]
- a `*` after a type means that the variable is a **pointer** with that type
- a `&` after a type means that variable is a **reference** with that type
## Size of
- the `sizeof()` function takes in a type and returns the size in bytes (an `int`)
## If Statements
- check if a variable is `true` or `false`
- `0` means `false`
- `1` *or anything else* means `true`
- an invalid pointer means `false`
- a valid pointer means `true`
- the comparison operator `==` returns `true` or `1` if both sides are equal
- `if` statements are *slow*
### Example
```cpp
#include <iostream>

int main()
{
	int x = 5;
	
	if (x == 5)
	{
	std::cout << "x is 5" << std::endl;
	}
	
	if (1) std::cout << "This will be logged." << std::endl;
	
	if (0)
	{
		std::cout << "This won't be logged." << std::endl;
	}
	else if (100) 
	{
		std::cout << "This will be logged." << std::endl;
	}
	
	return 0;
}
```