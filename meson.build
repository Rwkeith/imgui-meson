project('Dear ImGUI', 'cpp', default_options : ['default_library=static'])

imguiInc = include_directories('./backends', '.')

subproject('glfw')
glfwDep = dependency('glfw')
gl = dependency('gl')
threadDep = dependency('threads')

sources = [
    'imgui.cpp',
    'imgui_draw.cpp',
    'imgui_tables.cpp',
    'imgui_demo.cpp',
    'imgui_widgets.cpp',
    './backends/imgui_impl_glfw.cpp',
    './backends/imgui_impl_opengl3.cpp']

libImGUI = library('ImGUI', sources, include_directories : imguiInc, dependencies : [glfwDep, gl, threadDep])
libImGUIDep = declare_dependency(link_with : libImGUI, include_directories : imguiInc)
meson.override_dependency('imgui', libImGUIDep)
