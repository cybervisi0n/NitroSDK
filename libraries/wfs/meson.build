subdir('src')

if (build_target == 'arm')
libwfs = library('wfs',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: false,
    sources: [libwfs_srcs, fx_const_h]
)
else
libwfs = library('wfs',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: build_target == 'nx',
    sources: [libwfs_srcs, fx_const_h],
    native: (build_target == 'linux' or build_target == 'win64')
)
endif

nitrosdk_libs += libwfs
