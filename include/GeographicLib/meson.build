cfg = configuration_data()
cfg.set('PROJECT_VERSION_MAJOR', 1)
cfg.set('PROJECT_VERSION_MINOR', 49)
cfg.set('PROJECT_VERSION_PATCH', 0)
cfg.set('PROJECT_VERSION', '1.49.0')

if host_machine.system() == 'windows'
  cfg.set('GEOGRAPHICLIB_DATA', 'C:/ProgramData/GeographicLib')
else
  cfg.set('GEOGRAPHICLIB_DATA', '/usr/local/share/GeographicLib')
endif

cpp =  meson.get_compiler('cpp')

if cpp.has_type('long double')
  cfg.set('GEOGRAPHICLIB_HAVE_LONG_DOUBLE', 1)
endif

if host_machine.endian() == 'big'
  cfg.set('GEOGRAPHICLIB_WORDS_BIGENDIAN', 1)
endif

cfg.set('GEOGRAPHICLIB_PRECISION', 2)
cfg.set('GEOGRAPHICLIB_LIB_TYPE_VAL', 1)

config_h = configure_file(
  input : 'Config.h.in',
  output : 'Config.h',
  configuration : cfg
)

