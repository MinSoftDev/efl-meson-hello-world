project('hello-world', 'c')

compiler = meson.get_compiler('c')
incdirs = ['/usr/include/efl-1',
    '/usr/include/ecore-1',
    '/usr/include/eina-1',
    '/usr/include/eina-1/eina',
    '/usr/include/eo-1',
    '/usr/include/elementary-1',
    '/usr/include/eet-1',
    '/usr/include/emile-1',
    '/usr/include/evas-1',
    '/usr/include/ecore-evas-1',
    '/usr/include/ecore-file-1',
    '/usr/include/ecore-input-1',
    '/usr/include/ecore-imf-1',
    '/usr/include/ecore-con-1',
    '/usr/include/edje-1',
    '/usr/include/eldbus-1',
    '/usr/include/efreet-1',
    '/usr/include/ethumb-client-1',
    '/usr/include/ethumb-1',
    '/usr/include/eio-1',
    '/usr/include/elocation-1']

deps = []
foreach libname : ['ecore', 'elementary', 'eo', 'ecore_con']
    deps += [compiler.find_library(libname, dirs : '/lib64')]
endforeach

executable('hello-world', 'main.c', 
  include_directories : include_directories(incdirs),
  dependencies : deps,
  gui_app : true
)
