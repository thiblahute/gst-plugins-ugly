a52_comp = component('a52dec')
a52_dep = cc.find_dependency('a52', libs: 'a52',
  headers_symbols: [['a52dec/a52.h', 'a52_init']],
  prefix : '#include <stdint.h>',
  components: a52_comp,
  required : false)

a52dec = library('gsta52dec',
  'gsta52dec.c',
  c_args : ugly_args,
  include_directories : [configinc],
  dependencies : [gstaudio_dep, orc_dep, a52_dep],
  install : true,
  install_dir : plugins_install_dir,
  components: a52_comp
)
