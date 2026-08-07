- used to store function declarations which are needed when compiling and linking multiple `.cpp` files into one executable
## Header Guards
- make sure that contents of header files are not repeated more than once
```cpp
#pragma once
// declarations here
```

```cpp
#ifndef FUNCTION_NAME
#def FUNCTION_NAME
// declarations here
#endif
```
## [[Variables and Types]]