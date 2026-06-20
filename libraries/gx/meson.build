subdir('src')

libgx_includes = include_directories('include')

if (build_target == 'arm')
libgx = library('gx',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libgx_includes],
    pic: false,
    sources: [libgx_srcs, fx_const_h],
)
else
libgx = library('gx',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libgx_includes],
    pic: build_target == 'nx',
    sources: [libgx_srcs, fx_const_h],
    native: (build_target == 'linux' or build_target == 'win64')
)
endif

nitrosdk_libs += libgx
