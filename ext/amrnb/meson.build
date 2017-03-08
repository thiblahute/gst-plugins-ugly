amrnb_comp = component('amrnb',
  dependencies: dependency('opencore-amrnb', version : '>= 0.1.3', required : false))

amrnb = library('gstamrnb',
  ['amrnb.c', 'amrnbdec.c', 'amrnbenc.c'],
  c_args : ugly_args,
  include_directories : [configinc],
  dependencies : [gstaudio_dep, amrnb_comp.dependencies()],
  install : true,
  install_dir : plugins_install_dir,
  components: amrnb_comp
)
install_data(sources: 'GstAmrnbEnc.prs', install_dir: presetdir)
