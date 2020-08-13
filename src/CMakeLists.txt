include_directories(${CMAKE_SOURCE_DIR}/deps/)
include_directories(${CMAKE_SOURCE_DIR}/deps/glfw/include)
include_directories(${CMAKE_SOURCE_DIR}/deps/glm)
include_directories(${CMAKE_SOURCE_DIR}/deps/stb)
include_directories(${CMAKE_SOURCE_DIR}/inc)

set(ALL_LIBS
    ${OPENGL_LIBRARY}
     glfw
    -static-libgcc
    -static-libstdc++
    ${CMAKE_DL_LIBS}
    )

add_executable(pandora main.cpp glad.cpp)

target_link_libraries(pandora
    ${ALL_LIBS}
)
