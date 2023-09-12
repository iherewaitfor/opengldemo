project(glad)
#项目使用UNICODE版本。win中的各种API将使用UNICODE版本。
#add_definitions("-DUNICODE" "-D_UNICODE")

set(SRC ../${GLAD_DIR}/src/glad.c)
message(NOTICE "the prejectname: ${PROJECT_NAME}" )
add_library(${PROJECT_NAME} ${SRC})
SET_EXAMPLE_PROPERTIES(${PROJECT_NAME})
#COPY_FILES("${PROJECT_NAME}" "${GLFW_BIN_FiLES}" "${GLFW_BIN_DIR}" "${EXAMPLE_TARGET_OUT_DIR}")