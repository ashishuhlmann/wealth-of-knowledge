## Preprocessor Statements
- begin with `#`
- processed before all the code runs
## Include
- `#include` makes the compiler literally paste all the contents of the file called in to current file at the include statement
### Example 1
```cpp
#include <iostream>
```
- compiler pastes all of `iostream` into where the include statement is
- `<iostream>` has standard framework for handling input and output operations
	- `cin` is used for keyboard inputs
	- `cout` is used for printed outputs
### Example 2
`main.cpp`
```cpp
int Multiply(int a, int b)
{
return a * b;
#include "endbrace.h"
```
`endbrace.h`
```
}
```
- end brace gets pasted in to the `main.cpp` file exactly where the `#include` statement is
### Angle Brackets vs. Double Quote
- Angle Brackets
	- used for system-level header files or libraries
	- compiler searches for these files in a predefined set of directories, which are usually configured by the compiler or build system
- Double Quotes 
	- used for user-defined header files *and system libraries*
	- compiler first searches for these files in the directory containing the source file that includes them
	- then searches in other directories specified by the build system or compiler options (`-I` for gcc)
	- also searches in system libraries
## Define
- `#define`
- labels something as another
- defines a term
- search for one word and replace it with another (like CTRL+F -> Replace All)
- define any name
### Example
```cpp
#define INTEGER int

INTEGER main()
{
return 0;
}
```
- all instances of `INTEGER` are replaced with `int`
```cpp
#define MY_VARIABLE
```
- `MY_VARIABLE` is now defined

The convention is to have defined variables in all capital letters, that there may be minimal risk in ever using them accidentally. Variables can get cut off if part of their name is defined somewhere.
## If
- `#if`
- include or exclude code based on a condition
## End If
- `#endif`
- ends effect of if statement
### Example
```cpp
#if 1
int main()
{
return 0;
}
#endif
```
## If Not Defined
- `#ifndef`
- check if something is defined
## The Main Function
```cpp
int main()
{
	return 0;
}
```
- entry point
- computer executes code inside `main()` function line by line
- does *not* have to have a return value specified
- returns `0` if successful by default (exit code)
## Compiling

- `.cpp` files -> `.obj` files -> `.exe` file
- all `.cpp` files are compiled individually into **translation units** and stitched together in processes called **compiling** and **linking**
## Definitions and Declarations

- **Definition**
	explains what a function does
```cpp
void Log(const char* message)
{
	std::cout << message << std::endl;
}
```
- **Declaration**
	says that a function exists
```cpp
void Log(const char* message);
```
```cpp
void Log(const char*);
```
- a compiler may not know about certain functions when compiling multiple files
- declarations are needed to let the compiler know that these functions exist
- naming parameters doesn't matter for declarations
- a **linking error** will appear if a function is *declared but not defined*
- a proper declaration must have the correct *return type* and the correct *inputs*
## Function Keywords

### Static
- `static` is used to define a function that is only going to be used in the current file
### Example
```cpp
#include <iostream>

void Undefined_Function(int a);

int Multiply(int a, int b)

{
	Undefined_Function(0);
	return a * b
}

int main()
{
return 0;
}
```
- will return a linking error for `Undefined_Function` even though it is never called since it *could* be used in other files
```cpp
#include <iostream>

void Undefined_Function(int);

static int Multiply(int a, int b)

{
	Undefined_Function(0);
	return a * b
}

int main()
{
return 0;
}
```
- will *not* return a linking error for `Undefined_Function` since it is never called and will not be used in other files
### Inline
- `inline` copies the body of a function into where it is being called
## [[Header Files]]