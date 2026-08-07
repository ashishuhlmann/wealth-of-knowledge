A **shader** is code that we write to be compiled and run on the GPU.
- Shaders are written in [GLSL](https://docs.gl/sl4).
1. **vertex shaders** - calculates where verticies should end up on screen
2. **fragment shaders** - calculates the color of each pixel

On a draw call, the vertex shader is called, and then the fragment shader is called.
- The vertex shader runs for every vertex on screen.
- The fragment shader runs for every pixel on the screen.