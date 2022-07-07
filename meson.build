project('Dear ImGUI', 'cpp', default_options : ['default_library=static'])

imguiInc = include_directories('./backends', '.')

glfwLib = subproject('glfw').get_variable('glfw_dep')

gl = dependency('gl')
thread_dep = dependency('threads')

sources = [
    'imgui.cpp',
    'imgui_draw.cpp',
    'imgui_tables.cpp',
    'imgui_demo.cpp',
    'imgui_widgets.cpp',
    './backends/imgui_impl_glfw.cpp',
    './backends/imgui_impl_opengl3.cpp']

libImGUI = library('ImGUI', sources, include_directories : imguiInc, dependencies : [glfwLib, gl, thread_dep])
libImGUIDep = declare_dependency(link_with : libImGUI, include_directories : imguiInc)
