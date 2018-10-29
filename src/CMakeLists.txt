set (openglshader_headers
     include/OpenGLShader/shader.h)

set (openglshader_sources
     shader.cpp)

add_library(OpenGLShader ${openglshader_headers} ${openglshader_sources})

target_link_libraries(OpenGLShader PUBLIC
  GLEW::GLEW)

target_include_directories(OpenGLShader PUBLIC
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
  $<INSTALL_INTERFACE:include>)

target_include_directories(OpenGLShader PRIVATE
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/OpenGLShader>)


install(TARGETS OpenGLShader EXPORT OpenGLShaderConfig
  ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
  LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR},
  RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})

set_target_properties(OpenGLShader PROPERTIES LINKER_LANGUAGE CXX)


install(DIRECTORY include/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
