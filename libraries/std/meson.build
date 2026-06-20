subdir('src')

libstd_includes = include_directories('include')

if (build_target == 'arm')
libstd = library('std',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libstd_includes],
    pic: false,
    sources: [libstd_srcs, fx_const_h]
)
else
libstd = library('std',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libstd_includes],
    pic: build_target == 'nx',
    sources: [libstd_srcs, fx_const_h],
    native: (build_target == 'linux' or build_target == 'win64')
)
endif

nitrosdk_libs += libstd

