project(shaders_class)

aux_source_directory(. EXAMPLE_SRCS)
list(APPEND EXAMPLE_SRCS ${PROJECT_SOURCE_DIR}/3.3.shader.fs)
list(APPEND EXAMPLE_SRCS ${PROJECT_SOURCE_DIR}/3.3.shader.vs)

# Executable target.
add_executable(${PROJECT_NAME} ${EXAMPLE_SRCS})
SET_EXAMPLE_PROPERTIES(${PROJECT_NAME})
add_dependencies(${PROJECT_NAME} glad)

target_link_libraries(${PROJECT_NAME} glfw3dll )
target_link_libraries(${PROJECT_NAME} glad)

set (SHADER_FILES
3.3.shader.fs
3.3.shader.vs)

# Copy binary and resource files to the target output directory.
COPY_FILES("${PROJECT_NAME}" "${GLFW_BIN_FiLES}" "${GLFW_BIN_DIR}" "${EXAMPLE_TARGET_OUT_DIR}")
COPY_FILES("${PROJECT_NAME}" "${SHADER_FILES}" "${PROJECT_SOURCE_DIR}" "${EXAMPLE_TARGET_OUT_DIR}")
COPY_FILES("${PROJECT_NAME}" "${SHADER_FILES}" "${PROJECT_SOURCE_DIR}" "${CMAKE_BINARY_DIR}/${PROJECT_NAME}")