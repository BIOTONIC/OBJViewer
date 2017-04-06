cmake_minimum_required(VERSION 3.6)
project(OBJViewer)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -framework OPENGL")
set(GLFW3_LIBRARY "/usr/local/lib/libglfw.3.2.dylib")
set(GLEW_LIBRARY "/usr/local/lib/libGLEW.dylib")

set(SOURCE_FILES objviewer.cpp HalfEdge.h HalfEdge.cpp utils/shader.h utils/shader.cpp)
add_executable(OBJViewer ${SOURCE_FILES})
target_link_libraries(OBJViewer ${GLFW3_LIBRARY} ${GLEW_LIBRARY})