libcimgui_cpp_args = [
    '-DIMGUI_IMPL_OPENGL_LOADER_GLAD',
    '-Dcimgui_EXPORTS'
]

cimgui_includes = include_directories('imgui')

cimgui_srcs = files(
    'cimgui.cpp',
    'cimgui_impl.cpp',
    'imgui/imgui.cpp',
    'imgui/imgui_draw.cpp',
    'imgui/imgui_demo.cpp',
    'imgui/imgui_tables.cpp',
    'imgui/imgui_widgets.cpp',
    'imgui/backends/imgui_impl_opengl3.cpp',
    'imgui/backends/imgui_impl_sdl2.cpp'
)

libcimgui = library('cimgui',
    sources: cimgui_srcs,
    cpp_args: libcimgui_cpp_args,
    pic: false,
    include_directories: [nitrosdk_includes, cimgui_includes],
    native: true
)

nitrosdk_libs += libcimgui
