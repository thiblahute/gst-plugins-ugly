x264_sources = [
  'gstx264enc.c',
]

x264_comp = component('x264', dependencies: dependency('x264', required : false))
x264_libraries = get_option('x264_libraries')
x264_args = []
if x264_libraries != ''
  x264_args += ['-DHAVE_X264_ADDITIONAL_LIBRARIES="@0@"'.format(x264_libraries)]
endif

gstx264 = library('gstx264',
  x264_sources,
  c_args : ugly_args + x264_args,
  include_directories : [configinc],
  dependencies : [gstbase_dep, gstvideo_dep, gstpbutils_dep, x264_comp.dependencies()],
  install : true,
  install_dir : plugins_install_dir,
  components: x264_comp
)

if x264_comp.enabled()
  install_data(sources: 'GstX264Enc.prs', install_dir: presetdir)
endif
