cmake_minimum_required(VERSION 3.5)
PROJECT(MFC_ODBC)

SET(EXE_DIR ../../tmp)
SET(INC_DIR /usr/include/mysql)
SET(LINK_DIR /usr/lib/mysql)
SET(SRC_LIST main.c link_list.c file_process.c database_process.c mysql_fun.c)
SET(CMAKE_C_COMPILE "gcc")
SET(CMAKE_C_FLAGS "-g -Wall")
INCLUDE_DIRECTORIES(${INC_DIR})
LINK_DIRECTORIES(${LINK_DIR})

SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${EXE_DIR})
ADD_EXECUTABLE(stu ${SRC_LIST})
target_link_libraries(stu mysqlclient)
