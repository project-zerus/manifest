licenses(['notice'])

config_setting(
  name = 'darwin',
  values = {
    'cpu': 'darwin',
  }
)

cc_library(
  name = 'libssl',
  visibility = ['//visibility:public'],
  srcs = ['empty.cc'],
  linkopts = [
    '-lssl',
    '-lz',
  ]
)

cc_library(
  name = 'libevent',
  visibility = ['//visibility:public'],
  srcs = ['empty.cc'],
  deps = [
    ':libssl',
  ],
  linkopts = [
    '-levent',
    '-levent_core',
    '-levent_extra',
    '-levent_openssl',
    '-levent_pthreads',
  ] + select({
    'darwin': ['-L/usr/local/lib'],
    '//conditions:default': [],
  })
)

cc_library(
  name = 'pthread',
  visibility = ['//visibility:public'],
  srcs = ['empty.cc'],
  linkopts = select({
    'darwin': ['-lpthread'],
    '//conditions:default': ['-pthread'],
  }),
)
