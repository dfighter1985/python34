PROJECT( python C )

CMAKE_MINIMUM_REQUIRED( VERSION 2.8 )

SET( python_headers )
SET( python_sources 
	../../Modules/python.c )
	
INCLUDE_DIRECTORIES( ../../Include ../../PC ) 
	
ADD_DEFINITIONS( -D_CONSOLE )

ADD_EXECUTABLE( ${PROJECT_NAME} ${python_sources} ${python_headers} )

TARGET_LINK_LIBRARIES( ${PROJECT_NAME} python34 )

INSTALL( TARGETS ${PROJECT_NAME} DESTINATION ${INSTALL_DESTINATION} )
