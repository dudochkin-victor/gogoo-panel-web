SET(VERSION_MAJOR 0)
SET(VERSION_MINOR 0)
SET(VERSION_PATCH 0)

INCLUDE_DIRECTORIES(
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${MX_INCLUDE_DIRS}
    )

SET (LIBRARY common)

SET(LIBRARY_SRCS 
	mwb-ac-list.cc 
	mwb-ac-list.h 
	mwb-radical-bar.cc 
	mwb-radical-bar.h 
	mwb-separator.cc 
	mwb-separator.h 
	mwb-spindle.cc 
	mwb-spindle.h 
	mwb-utils.cc 
	mwb-utils.h 
    )

	

ADD_DEFINITIONS(-DPKGDATADIR=\"$(pkgdatadir)\")
ADD_DEFINITIONS(-DMWB_VERSION_STRING=\"$(MWB_VERSION)\")

ADD_LIBRARY(${LIBRARY} ${LIBRARY_SRCS})

SET_TARGET_PROPERTIES( ${LIBRARY} PROPERTIES
     SOVERSION 0
     VERSION ${VERSION_MAJOR}.${VERSION_MINOR}.${VERSION_PATCH}
   )


TARGET_LINK_LIBRARIES(${LIBRARY}
    ${MX_LIBRARIES}
    )
