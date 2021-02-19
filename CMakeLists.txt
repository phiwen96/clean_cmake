cmake_minimum_required (VERSION 3.19.4)
get_filename_component (my_folder_name ${CMAKE_CURRENT_SOURCE_DIR} NAME)
project (${my_folder_name} LANGUAGES CXX C ASM)

add_subdirectory (library)
add_subdirectory (app)

set (my_cache_variable "hejsan" CACHE STRING "hallå" )
set (my_bool off CACHE INTERNAL BOOL "kfmd")



# message (${my_cache_variable})


