PROJECT (LAviewLatexStruct C)

CMAKE_MINIMUM_REQUIRED (VERSION 2.8)

SET (PROJECT_LOWERCASE_NAME "laview-latex-struct")
SET (PROJECT_DESCRIPTION "LaTeX representation in the memory.")

SET (MAJOR 0)
SET (MINOR 1)
SET (PATCH 10)

LIST (APPEND CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake/backbone)

ADD_SUBDIRECTORY (src)
ADD_SUBDIRECTORY (po)
ADD_SUBDIRECTORY (pkg-config)
ADD_SUBDIRECTORY (test)
ADD_SUBDIRECTORY (cpack)

# enable testing
ENABLE_TESTING ()
