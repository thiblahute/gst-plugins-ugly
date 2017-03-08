mpeg2_comp = component('mpeg2dec',
  dependencies: dependency('libmpeg2', version : '>= 0.4.0', required : false))

mpeg2dec = library('gstmpeg2dec',
  ['gstmpeg2dec.c'],
  c_args : ugly_args,
  include_directories : [configinc],
  dependencies : [gstvideo_dep, mpeg2_comp.dependencies()],
  install : true,
  install_dir : plugins_install_dir,
  components: mpeg2_comp
)
