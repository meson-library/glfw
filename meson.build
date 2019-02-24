project('glfw', ['c'], 
         version       : '3.2.1',  
         license       : ['ZLIB'],
         meson_version : '>= 0.49.0')




name = 'glfw'




system     = build_machine.system()
cpu        = build_machine.cpu()
cpu_family = build_machine.cpu_family()

cc    = meson.get_compiler('c')
cc_id = cc.get_id() 

lib_type    = get_option('default_library')

includes  = []
sources   = []
c_args    = []
link_args = []

root_include = include_directories('.')

conf_data = configuration_data()




if system not in ['windows']
    error('Script (meson.build) not prepared for your platform yet.')
endif

if system == 'windows' and cc_id not in ['msvc']
    error('Script (meson.build) not prepared for your compiler yet.')
endif




subdir('src')




if get_option('build_examples')
	if not meson.is_subproject()
		subdir('examples')
	else
		warning('The option ' + name + ':' + 'build_examples' + ' not work in subproject.')
	endif
endif

if get_option('build_tests')
	if not meson.is_subproject()
		subdir('tests')
	else
		warning('The option ' + name + ':' + 'build_tests' + ' not work in subproject.')
	endif 
endif