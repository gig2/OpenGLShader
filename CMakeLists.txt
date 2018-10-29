cmake_minimum_required(VERSION 3.5)
project(OpenGLShader VERSION 0.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14)

find_package(GLEW REQUIRED)

include(GNUInstallDirs)

add_subdirectory(src)


install(EXPORT OpenGLShaderConfig DESTINATION share/OpenGLShader/cmake)

export(TARGETS OpenGLShader FILE OpenGLShaderConfig.cmake)
