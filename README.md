# opengldemo
# opengl环境搭建
## glad
## glfw
# 管理流水关键流程

## 顶点着色器
- glCreateShader(GL_VERTEX_SHADER)
- glShaderSource
- glCompileShader
- glDeleteShader
  - 链接完可以删除
### 填充顶点数据
- glGenVertexArrays
- glBindVertexArray
- glGenBuffers
- glBindBuffer
- glBufferData
- glVertexAttribPointer
- glEnableVertexAttribArray

