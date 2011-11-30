cmake_minimum_required(VERSION 2.6)
project(homeTorrent)

#setup target
set (CMAKE_BUILD_TYPE Debug)
#set (CMAKE_BUILD_TYPE Release)

#####add boost
set (Boost_NO_SYSTEM_PATHS TRUE)
set (Boost_DEBUG TRUE)
set (BOOST_ROOT /home/dex/workspace/sdks/boost_1.48.0)
set (BOOOST_LIBRARYDIR ${BOOSTROOT}/stage/lib)
FIND_PACKAGE( Boost 1.48.0 COMPONENTS system thread REQUIRED )
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
