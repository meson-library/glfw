
includes = include_directories('../deps')

glad_sources = ['../deps/glad/glad.h', '../deps/glad.c']
getopt_sources = ['../deps/getopt.h', '../deps/getopt.c']
tinycthread_sources = ['../deps/tinycthread.h', '../deps/tinycthread.c']

resources = []
if system == 'windows'
    windows  = import('windows')
    resources += windows.compile_resources('glfw.rc')

    opengl_dep = cc.find_library('opengl32', required: true)
endif


executable('boing' 
           ,include_directories : [includes]
           ,sources             : ['boing.c'] + glad_sources + resources
           ,c_args              : c_args            
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('gears' 
           ,include_directories : [includes]
           ,sources             : ['gears.c'] + glad_sources + resources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('heightmap' 
           ,include_directories : [includes]
           ,sources             : ['heightmap.c'] + glad_sources + resources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('particles'
           ,include_directories : [includes]
           ,sources             : ['particles.c'] + glad_sources + getopt_sources + tinycthread_sources + resources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('simple'
           ,include_directories : [includes] 
           ,sources             : ['simple.c'] + glad_sources + resources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('splitview'
           ,include_directories : [includes]
           ,sources             : ['splitview.c'] + glad_sources + resources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('wave'
           ,include_directories : [includes] 
           ,sources             : ['wave.c'] + glad_sources + resources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)




install_data(['doc/glew.txt', 
              install_dir : 'share/licenses/glew')