
includes = include_directories('../deps')

glad_sources = ['../deps/glad/glad.h', '../deps/glad.c']
getopt_sources = ['../deps/getopt.h', '../deps/getopt.c']
tinycthread_sources = ['../deps/tinycthread.h', '../deps/tinycthread.c']




executable('clipboard' 
           ,include_directories : [includes]
           ,sources             : ['clipboard.c'] + glad_sources + getopt_sources
           ,c_args              : c_args            
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('events' 
           ,include_directories : [includes]
           ,sources             : ['events.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('msaa' 
           ,include_directories : [includes]
           ,sources             : ['msaa.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('gamma'
           ,include_directories : [includes]
           ,sources             : ['gamma.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('glfwinfo'
           ,include_directories : [includes] 
           ,sources             : ['glfwinfo.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('iconify'
           ,include_directories : [includes]
           ,sources             : ['iconify.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('joysticks'
           ,include_directories : [includes] 
           ,sources             : ['joysticks.c'] + glad_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('monitors'
           ,include_directories : [includes] 
           ,sources             : ['monitors.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('reopen'
           ,include_directories : [includes] 
           ,sources             : ['reopen.c'] + glad_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('cursor'
           ,include_directories : [includes] 
           ,sources             : ['cursor.c'] + glad_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('empty' 
           ,include_directories : [includes]
           ,sources             : ['empty.c'] + glad_sources + tinycthread_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('icon'
           ,include_directories : [includes]
           ,sources             : ['icon.c'] + glad_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('sharing'
           ,include_directories : [includes] 
           ,sources             : ['sharing.c'] + glad_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('tearing'
           ,include_directories : [includes]
           ,sources             : ['tearing.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('threads'
           ,include_directories : [includes] 
           ,sources             : ['threads.c'] + glad_sources + tinycthread_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('timeout'
           ,include_directories : [includes] 
           ,sources             : ['timeout.c'] + glad_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('title'
           ,include_directories : [includes] 
           ,sources             : ['title.c'] + glad_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)

executable('windows'
           ,include_directories : [includes] 
           ,sources             : ['windows.c'] + glad_sources + getopt_sources
           ,c_args              : c_args
           ,dependencies        : [glfw_dep]
           ,install             : true)