cmake_minimum_required(VERSION 2.8.12)

# Install tracks
file(GLOB TRACKS "[^.]*")
foreach(track ${TRACKS})
	if(IS_DIRECTORY ${track})
		install(DIRECTORY ${track} DESTINATION "${SHARE_INSTALL}/tracks")
	endif()
endforeach()
