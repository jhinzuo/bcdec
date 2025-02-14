project('bcdec', 'c',
	license: 'MIT',
	version: '0.98',
	default_options: [
		'prefix=/usr',
		'warning_level=3',
	],
    meson_version: '>=1.2.1')

compiler = meson.get_compiler('c')
bcdeclib = library('bcdec', ['bcdec.c'], install: true, c_args: ['-DBCDEC_EXPORTING'])
bcdecdep = declare_dependency(link_with: bcdeclib, include_directories: include_directories('.'))
install_headers('bcdec.h')