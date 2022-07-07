project('Dear ImGUI', 'cpp')

incdir = include_directories('./backends', '.')

sources = [
    'imgui.cpp',
    'imgui_draw.cpp',
    'imgui_tables.cpp',
    'imgui_demo.cpp',
    'imgui_widgets.cpp',
    'imgui_impl_glfw.cpp',
    'imgui_impl_opengl3.cpp']

libImGUI = library('ImGUI', sources, include_directories : incdir)
libImGUIDep = declare_dependency(link_with : libImGUI, include_directories : incdir)
