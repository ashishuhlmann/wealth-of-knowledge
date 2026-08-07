
A **vertex buffer** is just a **buffer** or a array of bytes in memory in OpenGL within the GPU's VRAM.

1. Add triangle data to the GPU's VRAM
2. Issue a draw call.
3. GPU interprets the data using code written in a **shader**.

OpenGL operates as a **state machine**. Everything you generate gets assigned an identifier. 
## Creating VRAM Buffers

`glGenBuffers` - generate a buffer and return an identification
1. number of buffers
2. memory address

`glBindBuffer` - select a buffer
1. specification
2. identification of buffer

**Vertex** - object containing data associated with a vertex
1. position
2. color
3. texture coordinate
4. normal vector
5. binormal vector
6. tangent vector

**Vertex Attribute** - position, normal, texture, color, or other property of a vertex

`glBufferData` - add data to a buffer
3. specification
4. amount of space in bytes
5. data
6. hint (`STREAM`, `STATIC`, `DYNAMIC`)
```cpp
unsigned int buffer;
glGenBuffers(1, &buffer);
glBindBuffer(GL_ARRAY_BUFFER, buffer);
glBufferData(GL_ARRAY_BUFFER, 6*sizeof(float), positions, GL_DYNAMIC_DRAW);
```
## Assign Buffer Attributes

Now we need to specify what this data represents and how it is formatted.
- buffers must be bound first before the draw call is issued for anything to be drawn

`glVertexAttribPointer`
1. attribute number
2. number of floats within that attribute
3. data type
4. normalized? (usually `GL_FALSE`)
5. number of bytes to skip to go to the next vertex
6. number of bytes to skip within a single vertex to get to the attribute
```cpp
glEnableVertexAttribArray(0);
glVertexAttribPointer(0, 3, GL_FLOAT, GL_FALSE, 6 * sizeof(GLfloat), (GLvoid*)0);
```
## Issue a Draw Call

`glDrawArrays`
1. shape
2. starting vertex
3. number of verticies

```cpp
glDrawArrays(GL_TRIANGLES, 0, 3);
```
## [[3 Shaders]]