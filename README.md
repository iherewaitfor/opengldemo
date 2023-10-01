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
  - 先绑定特定的顶点数组
  - 才能对具体的操作顶点数组的各个属性
- glGenBuffers
  - 创建buffer
- glBindBuffer
  - 绑定buffer
- glBufferData
  - 复制数据到对应的buffer。复制前需要先绑定
- glVertexAttribPointer
  - 指定顶点的某个属性的内存格式
- glEnableVertexAttribArray
  - 启用顶点的某个属性

