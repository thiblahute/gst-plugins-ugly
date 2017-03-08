amrwb_dep = dependency('opencore-amrwb', version : '>= 0.1.3', required : false)

amrwbdec = library('gstamrwbdec',
  ['amrwb.c', 'amrwbdec.c'],
  c_args : ugly_args,
  include_directories : [configinc],
  dependencies : [gstaudio_dep, amrwb_dep],
  install : true,
  install_dir : plugins_install_dir,
  components: component('amrwbdec', dependencies: amrwb_dep)
)
