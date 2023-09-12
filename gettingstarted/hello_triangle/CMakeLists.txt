project(hello_triangle)

aux_source_directory(. EXAMPLE_SRCS)

# Executable target.
add_executable(${PROJECT_NAME} ${EXAMPLE_SRCS})
SET_EXAMPLE_PROPERTIES(${PROJECT_NAME})
add_dependencies(${PROJECT_NAME} glad)

target_link_libraries(${PROJECT_NAME} glfw3dll )
target_link_libraries(${PROJECT_NAME} glad)

# Copy binary and resource files to the target output directory.
COPY_FILES("${PROJECT_NAME}" "${GLFW_BIN_FiLES}" "${GLFW_BIN_DIR}" "${EXAMPLE_TARGET_OUT_DIR}")

