licenses(['notice'])

config_setting(
  name = 'darwin',
  values = {
    'cpu': 'darwin',
  }
)

cc_library(
  name = 'pthread',
  visibility = ['//visibility:public'],
  srcs = ['empty.cc'],
  linkopts = select({
    'darwin': ['-lpthread'],
    '//conditions:default': ['-pthread'],
  }),
  alwayslink = 1,
)
