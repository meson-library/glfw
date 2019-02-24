
includes += include_directories('../include')

sources  += ['internal.h',
             '../include/GLFW/glfw3.h',
             '../include/GLFW/glfw3native.h',
             'context.c', 
             'init.c', 
             'input.c', 
             'monitor.c', 
             'vulkan.c', 
             'window.c']

if system == 'windows'
  sources += ['win32_platform.h', 
              'win32_joystick.h', 
              'wgl_context.h', 
              'egl_context.h', 
              'win32_init.c', 
              'win32_joystick.c', 
              'win32_monitor.c', 
              'win32_time.c', 
              'win32_tls.c', 
              'win32_window.c', 
              'wgl_context.c', 
              'egl_context.c']
endif




if system == 'windows'
    conf_data.set('_GLFW_WIN32', '1')

    if get_option('use_hybrid_hpg')
      conf_data.set('_GLFW_USE_HYBRID_HPG', '1')
    endif
endif




configure_file(input         : 'glfw_config.h.in',
               output        : 'glfw_config.h',
               format        : 'cmake',
               configuration : conf_data)




c_args += ['-D_GLFW_USE_CONFIG_H']




if lib_type == 'static' or lib_type == 'both' 
    static_lib_name        = name
    static_lib_name_prefix = []
    static_lib_name_suffix = []

    if system == 'windows' and cc_id == 'msvc'  
        static_lib_name       += '_static'
        static_lib_name_prefix = ''
        static_lib_name_suffix = 'lib'
    endif

    glfw_static = static_library(static_lib_name,
                                 name_prefix         : static_lib_name_prefix, 
                                 name_suffix         : static_lib_name_suffix,
                                 include_directories : [root_include, includes],
                                 sources             : sources,
                                 c_args              : c_args, 
                                 link_args           : link_args,
                                 install             : true)

    glfw_static_dep = declare_dependency(include_directories : includes,
                                         link_with           : glfw_static)
endif




if lib_type == 'shared' or lib_type == 'both'
    shared_lib_name = name 

    glfw_shared = shared_library(shared_lib_name, 
                                 include_directories : [root_include, includes],
                                 sources             : sources,
                                 c_args              : c_args + ['-D_GLFW_BUILD_DLL'], 
                                 link_args           : link_args,   
                                 install             : true)

    glfw_shared_dep = declare_dependency(include_directories : includes,
                                         link_with           : glfw_shared)
endif




if lib_type == 'static'
    glfw_dep = glfw_static_dep
elif lib_type == 'shared' or lib_type == 'both'
    glfw_dep = glfw_shared_dep
endif




install_headers('../include/GLFW/glfw3native.h', 
                '../include/GLFW/glfw3.h', 
                 subdir : 'GLFW')

install_data(['../COPYING.txt'],
               rename      : ['LICENSE.ZLIB'],
               install_dir :  'share/licenses/glfw')