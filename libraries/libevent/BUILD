licenses(['notice'])

config_setting(
  name = 'darwin',
  values = {
    'cpu': 'darwin',
  }
)

cc_library(
  name = 'libevent',
  visibility = ['//visibility:public'],
  srcs = ['empty.cc'],
  deps = [
    '//external:libssl',
    '//external:pthread',
  ],
  linkopts = [
    '-levent',
  ] + select({
    'darwin': ['-L/usr/local/lib'],
    '//conditions:default': [],
  }),
  alwayslink = 1,
)
