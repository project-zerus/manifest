licenses(['notice'])

cc_library(
  name = 'libssl',
  visibility = ['//visibility:public'],
  srcs = [],
  linkopts = [
    '-lssl',
    '-lz',
  ]
)

cc_library(
  name = 'libevent',
  visibility = ['//visibility:public'],
  srcs = [],
  deps = [
    ':libssl',
  ],
  linkopts = [
  '-levent',
  ]
)
