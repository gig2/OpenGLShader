openglshader_headers = files(['include/OpenGLShader/shader.h',])

openglshader_sources = files(['shader.cpp'])

openglshader_include = include_directories('./include')

openglshader_internal_include = include_directories('./include/OpenGLShader')


install_subdir('include/OpenGLShader', install_dir:'include')


openglshader_lib = library('OpenGLShader',
                               sources: [openglshader_headers,
                                        openglshader_sources],
                               dependencies: [glew_dep],
                               include_directories: [openglshader_include,
                                                    openglshader_internal_include],
                               install:true)

openglshader_dep = declare_dependency(link_with: openglshader_lib,
                                       dependencies: [glew_dep],
                                       include_directories: [openglshader_include]
                                         )
