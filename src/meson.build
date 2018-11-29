src = [
  'CircularEngine.cpp',
  'Geohash.cpp',
  'GeodesicLine.cpp',
  'Ellipsoid.cpp',
  'LambertConformalConic.cpp',
  'Math.cpp',
  'GeodesicExact.cpp',
  'NormalGravity.cpp',
  'Geodesic.cpp',
  'MagneticCircle.cpp',
  'CassiniSoldner.cpp',
  'AzimuthalEquidistant.cpp',
  'Geoid.cpp',
  'OSGB.cpp',
  'AlbersEqualArea.cpp',
  'Rhumb.cpp',
  'Geocentric.cpp',
  'TransverseMercator.cpp',
  'TransverseMercatorExact.cpp',
  'GravityModel.cpp',
  'Accumulator.cpp',
  'PolarStereographic.cpp',
  'GeodesicLineExact.cpp',
  'GravityCircle.cpp',
  'SphericalEngine.cpp',
  'MagneticModel.cpp',
  'UTMUPS.cpp',
  'LocalCartesian.cpp',
  'Utility.cpp',
  'GeoCoords.cpp',
  'Gnomonic.cpp',
  'Georef.cpp',
  'EllipticFunction.cpp',
  'GARS.cpp',
  'PolygonArea.cpp',
  'DMS.cpp',
  'GeodesicExactC4.cpp',
  'MGRS.cpp',
  config_h,
]

public_args = ['-DGEOGRAPHICLIB_SHARED_LIB=1']
private_args = ['-DGEOGRAPHICLIB_CXX11_MATH=1', '-DGEOGRAPHICLIB_HAS_STATIC_ASSERT=1', '-DGeographicLib_EXPORTS']

libgeographic_lib = shared_library('Geographic',
  name_prefix : 'lib',
  sources : src,
  include_directories : include_directories('../include'),
  cpp_args : private_args + public_args,
)

libgeographic_dep = declare_dependency(
  link_with : libgeographic_lib,
  include_directories : include_directories('../include', is_system : true),
  cpp_args : public_args,
)

