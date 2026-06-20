subdir('src')

if (build_target == 'arm')
libinit = library('init',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: false,
    sources: [libinit_srcs, fx_const_h]
)
else
libinit = library('init',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: build_target == 'nx',
    sources: [libinit_srcs, fx_const_h],
    native: (build_target == 'linux' or build_target == 'win64')
)
endif

crt0_obj = libinit.extract_all_objects(recursive: true)
