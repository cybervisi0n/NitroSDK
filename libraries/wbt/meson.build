subdir('src')

if (build_target == 'arm')
libwbt = library('wbt',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: false,
    sources: [libwbt_srcs, fx_const_h]
)
else
libwbt = library('wbt',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: build_target == 'nx',
    sources: [libwbt_srcs, fx_const_h],
    native: (build_target == 'linux' or build_target == 'win64')
)
endif

nitrosdk_libs += libwbt
