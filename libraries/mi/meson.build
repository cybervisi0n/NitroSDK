subdir('src')

libmi_includes = include_directories('include')

if (build_target == 'arm')
libmi = library('mi',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libmi_includes],
    pic: false,
    sources: [libmi_srcs, fx_const_h],
)
else
libmi = library('mi',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libmi_includes],
    pic: build_target == 'nx',
    sources: [libmi_srcs, fx_const_h],
    native: (build_target == 'linux' or build_target == 'win64')
)
endif

nitrosdk_libs += libmi
