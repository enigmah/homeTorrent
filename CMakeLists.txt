project(homeTorrent)

#setup target
set (CMAKE_BUILD_TYPE Debug)
#set (CMAKE_BUILD_TYPE Release)

#####add boost boost
FIND_PACKAGE( Boost COMPONENTS system thread REQUIRED )
INCLUDE_DIRECTORIES( ${Boost_INCLUDE_DIR} )


set(HOMETORRENT_SRC
main.h main.cpp
http.h http.cpp
)

set (HOMETORRENT_LIBS
${Boost_LIBRARIES}
)

add_executable(homeTorrent ${HOMETORRENT_SRC})
target_link_libraries(homeTorrent ${HOMETORRENT_LIBS})
