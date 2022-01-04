set(GLADRoot ${PROJECT_SOURCE_DIR}/dependencies/glad)
set(GLFWRoot ${PROJECT_SOURCE_DIR}/dependencies/GLFW)
set(StbRoot ${PROJECT_SOURCE_DIR}/dependencies/stb_image)
set(GLMRoot ${PROJECT_SOURCE_DIR}/dependencies/glm)

include_directories(${GLADRoot}/include)
include_directories(${GLFWRoot}/include)
include_directories(${StbRoot})
include_directories(${GLMRoot})


set(HEADER_FILES ${PROJECT_SOURCE_DIR}/src/shader.h)
set(SOURCE_FILES ${PROJECT_SOURCE_DIR}/src/main.cc glad.c)

add_executable(OpenGLTest ${HEADER_FILES} ${SOURCE_FILES})
target_link_libraries(OpenGLTest ${GLFWRoot}/lib/glfw3.lib)
