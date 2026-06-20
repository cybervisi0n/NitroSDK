subdir('src')

libsim7_includes = include_directories('include')

libsim7 = library('sim7',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libsim7_includes],
    pic: build_target == 'nx',
    sources: [libsim7_srcs, fx_const_h],
    native: (build_target == 'linux' or build_target == 'win64')
)

nitrosdk_libs += libsim7
