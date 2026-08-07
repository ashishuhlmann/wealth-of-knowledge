
**OpenGL** is a specification that lists functions. OpenGL is not library or framework.
- OpenGL can't be downloaded or installed, because the implementation is contained within the **graphics drivers**.
- OpenGL is written by each graphics card manufacturer, and is ironically *not* open source.
- OpenGL functions are implemented in the graphics drivers.
## Installation

Install the latest NVIDIA driver from terminal or the Pop! Shop.

```bash
sudo apt install nvidia-driver-XXX
```
## Windowing

Each platform (Windows, Mac OS, Linux) has its own windowing **API** used to create windows, and this code can be manually written for each operating system.
### Graphics Library Framework

The **Graphics Library Framework (GLFW)** library provides implementations of windowing creation and management code for each operating system.
- GLFW just creates a window and an **OpenGL context**.
```bash
 sudo apt install libglfw3-dev
```
### [Link GLFW](https://www.glfw.org/documentation.html)
```c
#include <GLFW/glfw3.h>

int main(void)
{
    GLFWwindow* window;

    /* Initialize the library */
    if (!glfwInit())
        return -1;

    /* Create a windowed mode window and its OpenGL context */
    window = glfwCreateWindow(640, 480, "Hello World", NULL, NULL);
    if (!window)
    {
        glfwTerminate();
        return -1;
    }

    /* Make the window's context current */
    glfwMakeContextCurrent(window);

	/* Keep window open */
    if (!gladLoadGLLoader((GLADloadproc)glfwGetProcAddress)) {
        std::cerr << "Couldn't load OpenGL functions through GLAD" << std::endl;
        glfwTerminate();
        return -1;
    }
    
    std::cout << "OpenGL " << glGetString(GL_VERSION) << std::endl;

    /* Loop until the user closes the window */
    while (!glfwWindowShouldClose(window))
    {
        /* Render here */
        glClear(GL_COLOR_BUFFER_BIT);

        /* Swap front and back buffers */
        glfwSwapBuffers(window);

        /* Poll for and process events */
        glfwPollEvents();
    }

    glfwTerminate();
    return 0;
}
```
## [GLAD](https://github.com/Dav1dde) / GLEW

With OpenGL functions built into the drivers, we need to declare them and link them.
- Access the driver DLL files and retrieve function pointers.

The **GLAD** library provides function and symbol declarations in a header file `glad.h`.
- The actual implementation identifies the graphics drivers being used, finds the appropriate DLL file, and retrieves all the function pointers.
### [Function Documentation](https://docs.gl/)
## CMake

Properly link the packages.
```cmake
find_package(OpenGL REQUIRED)

add_executable(hello_window
	src/main.cpp
	src/glad.c
) 

target_link_libraries(hello_window
	glfw
	OpenGL::GL
)

include_directories(include)
```
## [[2 Vertex Buffers]]