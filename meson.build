project('argtable3', 'c', default_options : ['c_std=c89'])

argtable_src = [
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

argtable_inc = include_directories('src')

argtable_include_directories = [argtable_inc]

argtable_lib = library(
  'argtable',
  argtable_src,
  include_directories : butterfly_include_directories
)

argtable_dep = declare_dependency(
  link_with : argtable_lib,
  include_directories : argtable_include_directories
)
