project(homeTorrent)

#set (CMAKE_BUILD_TYPE Debug)
set (CMAKE_BUILD_TYPE Release)

set(HOMETORRENT_SRC
main.h main.cpp
)

add_executable(homeTorrent ${HOMETORRENT_SRC})


