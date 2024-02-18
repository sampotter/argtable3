project('argtable3', 'c', default_options : ['c_std=c89'])

pkgconfig = import('pkgconfig')

m_dep = meson.get_compiler('c').find_library('m', required : true)

argtable3_src = [
  './src/arg_cmd.c',
  './src/arg_date.c',
  './src/arg_dbl.c',
  './src/arg_dstr.c',
  './src/arg_end.c',
  './src/arg_file.c',
  './src/arg_hashtable.c',
  './src/arg_int.c',
  './src/arg_lit.c',
  './src/arg_rem.c',
  './src/arg_rex.c',
  './src/arg_str.c',
  './src/arg_utils.c',
  './src/argtable3.c',
  './src/arg_getopt_long.c',
]

argtable3_inc = include_directories('src')

argtable3_lib = library(
  'argtable3',
  argtable3_src,
  dependencies : [m_dep],
  include_directories : [argtable3_inc],
  install : true
)

install_headers('src/argtable3.h')

argtable3_dep = declare_dependency(
  link_with : argtable3_lib,
  include_directories : [argtable3_inc]
)

pkgconfig.generate(
  libraries : argtable3_lib,
  version : '3.2.2',
  name : 'argtable3',
  filebase : 'argtable3',
  description : 'A single-file, ANSI C, command-line parsing library that parses GNU-style command-line options.'
)