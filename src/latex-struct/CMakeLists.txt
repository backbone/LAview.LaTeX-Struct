SET (LibName ${PROJECT_LOWERCASE_NAME})
FILE (GLOB_RECURSE LibSources RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.vala)
SET (LibPackages gee-0.8 posix)
SET (LibPkgModules gee-0.8)
SET (LibInstall ON)
SET (LibExtraSources ${CMAKE_CURRENT_BINARY_DIR}/library_constructor.c)
SET (LC_RELATIVE_PREFIX "..")
CONFIGURE_FILE ( "${CMAKE_SOURCE_DIR}/cmake/backbone/templates/library_constructor.c.in" "${LibExtraSources}")
INCLUDE (ValaLibCommonRules)
