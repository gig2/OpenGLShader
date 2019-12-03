project('OpenGLShader','cpp', default_options : ['cpp_std=c++14'],
       version: '0.0.0')

glew_dep = dependency('glew', required:true)
subdir('src')

# pkgconfig section
pkg = import('pkgconfig')

pkg.generate(description: 'OpenGLShader is a simple utility to render mesh',
             filebase: 'OpenGLShader',
             libraries: [openglshader_lib],
             name: 'OpenGLShader',
             version: meson.project_version()
            )
