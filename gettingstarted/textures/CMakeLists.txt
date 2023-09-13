project(textures)

aux_source_directory(. EXAMPLE_SRCS)

file (GLOB SHADER_FILES RELATIVE ${PROJECT_SOURCE_DIR}
		"*.vs" "*.fs")
include_directories(${CMAKE_BINARY_DIR}/configuration)

# Executable target.
add_executable(${PROJECT_NAME} ${EXAMPLE_SRCS} ${SHADER_FILES})
SET_EXAMPLE_PROPERTIES(${PROJECT_NAME})
add_dependencies(${PROJECT_NAME} glad)

target_link_libraries(${PROJECT_NAME} glfw3dll )
target_link_libraries(${PROJECT_NAME} glad)
target_link_libraries(${PROJECT_NAME} STB_IMAGE)


# Copy binary and resource files to the target output directory.
COPY_FILES("${PROJECT_NAME}" "${GLFW_BIN_FiLES}" "${GLFW_BIN_DIR}" "${EXAMPLE_TARGET_OUT_DIR}")
COPY_FILES("${PROJECT_NAME}" "${SHADER_FILES}" "${PROJECT_SOURCE_DIR}" "${EXAMPLE_TARGET_OUT_DIR}")
COPY_FILES("${PROJECT_NAME}" "${SHADER_FILES}" "${PROJECT_SOURCE_DIR}" "${CMAKE_BINARY_DIR}/${PROJECT_NAME}")