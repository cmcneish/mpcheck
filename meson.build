project('mpcheck', 'c')

cc = meson.get_compiler('c')
libm_dep = cc.find_library('m')
mpfr_dep = cc.find_library('mpfr')
gmp_dep = cc.find_library('gmp')

executable('check',
    [
        'check.c',
        'test.c',
        'func.c',
        'setup.c',
        'rnd_mode.c',
        'ulp.c',
    ],
    c_args : [
        '-DUSE_FENV_H',
    ],
    dependencies : [
        mpfr_dep,
        libm_dep,
        gmp_dep,
    ])
