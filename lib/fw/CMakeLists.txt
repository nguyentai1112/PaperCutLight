CMAKE_MINIMUM_REQUIRED(VERSION 3.10)

PROJECT(FW)

FILE(GLOB_RECURSE SRC
		"${PROJECT_SOURCE_DIR}/source/*.cpp"
		"${PROJECT_SOURCE_DIR}/include/*.h")

ADD_LIBRARY(FileWatcher STATIC ${SRC})

TARGET_INCLUDE_DIRECTORIES(FileWatcher PUBLIC "${PROJECT_SOURCE_DIR}/include")
