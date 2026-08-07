A **class** or **struct** is an object with its own type that can be called multiple different times.
- Classes and structs have variables and functions or methods assigned to them. These variables and functions can either be **public** or **private**.
### Example
```cpp
#include <cmath>

class Player
{
	float m_x;
	float m_y;
	
	float Distance(float x, float y)
	{
		return std::sqrt(std::pow((x-m_x),2) - std::pow((y-m_y),2));
	}
};
```
- *Convention: Private member variables use an* `m_` *infront.*

Public variables and functions can be accessed outside of the class, while private variables and functions can only be accessed inside the class. These are denoted by `public:` and `private:`.

A **class** uses private variables by default.
A **struct** uses public variables by default.
### Example
```cpp
#include <iostream>

class Log
{
public:

    const int LogLevelError = 0;
    const int LogLevelWarn = 1;
    const int LogLevelInfo = 2;
    
private:

    int m_LogLevel = LogLevelInfo; // set to LogLevelInfo by default
    
public:

    void SetLogLevel(int level)
    {
        m_LogLevel = level;
    }
    
    void Error(const char* error)
    {
        std::cout << "[ERROR]: " << error << std::endl;
    }
    
    void Warn(const char* warning)
    {
        if (m_LogLevel >=1)
            std::cout << "[WARNING]: " << warning << std::endl;
    }
    
    void Info(const char* info)
    {
        if (m_LogLevel == 2)
            std::cout << "[INFO]: " << info << std::endl;
    }
};

int main()
{
	Log log;
	log.SetLogLevel(log.LogLevelWarn);
	log.Warn("Hello!");
	return 0;
}
```
## Constructors

A **constructor** intializes the memory used by a class and can assign values upon creation.
### Example
```cpp
#include <iostream>

class Vector2
{    
public:

    float X;
    float Y;
    
    void PrintPos()
    {
        std::cout << X << ", " << Y << std::endl;
    }
    
int main()
{
	Vector2 vec;
	vec.PrintPos();
	return 0;
}
```
```bash
-5.32598e+06, 4.5751e-41
```
- The memory hasn't been initialized and will simply show whatever happens to be stored in it.
- `std::cout << vec.X << std::endl;` gives an unititialized error.
### Use

A **constructor** is a function using the name of the class with no return type. 
```cpp
#include <iostream>

class Vector2
{    
public:

    float X;
    float Y;
	
	Vector2()
	{
	X = 0.0f
	Y = 0.0f
	}
	
    void PrintPos()
    {
        std::cout << X << ", " << Y << std::endl;
    }
}

int main()
{
	Vector2 vec;
	vec.PrintPos();
	return 0;
}
```
```bash
0, 0
```
Without a constructor, the compiler uses a *default constructor* that doesn't set variables to anything specific.

Constructors can also take inputs.
```cpp
	Vector2()
	{
	X = 0.0f;
	Y = 0.0f;
	}
	
	Vector2(float x, float y)
	{
	X = x;
	Y = y;
	}
```
- This gives the option of adding parameters at assignment: `Vector2 vec(1.0f, 2.0f);`
## Operator Overloading

An operation can be defined for a specific class using a function with the name of the class, operator, and no return type
### Example
```cpp
#include <iostream>

class Vector2
{    
public:

    float X;
    float Y;
	
	Vector2()
	{
	X = 0.0f
	Y = 0.0f
	}
	
	Vector2(float x, float y)
	{
	X = x
	y = Y
	}

    Vector2 operator+(Vector2 other) 
    {
        Vector2 VectorSum(X + other.X, Y + other.Y); 
        return VectorSum;
    }
}

int main()
{
	Vector2 vec1(1.0f, 2.0f);
	Vector2 vec2(-3.0f, 4.0f);
	std::cout << (vec1 + vec2).X << std::endl;
}
```
```bash
-1.0
```
