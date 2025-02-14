project('bcdec', 'c',
	license: 'MIT',
	version: '0.99',
	default_options: [
		'prefix=/usr',
		'warning_level=3',
	],
    meson_version: '>=1.2.1')

defines = ['-DBCDEC_EXPORTING']

if get_option('precise_bc3')
	defines += ['-DBCDEC_BC3_PRECISE']
endif

if get_option('precise_bc4bc5')
	defines += ['-DBCDEC_BC4BC5_PRECISE']
endif

compiler = meson.get_compiler('c')
bcdeclib = library('bcdec', ['bcdec.c'], install: true, c_args: defines)
bcdecdep = declare_dependency(link_with: bcdeclib, include_directories: include_directories('.'))
install_headers('bcdec.h')

executable('bcdec', ['test.c'], install: true, c_args: defines)
