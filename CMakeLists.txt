cmake_minimum_required (VERSION 3.19.4 FATAL_ERROR)
get_filename_component (my_folder_name ${CMAKE_CURRENT_SOURCE_DIR} NAME)
project (${my_folder_name} LANGUAGES CXX C ASM)

add_subdirectory (library)
add_subdirectory (apps)

set (my_cache_variable "hejsan" CACHE STRING "hallå" )
set (my_bool off CACHE INTERNAL BOOL "kfmd")

if (APPLE)
	message ("APPLE!!!")
endif ()

# message (${my_cache_variable})



# in root
# cmake -Bbuild
# cmake -Bbuild --build .

# in build
# cmake ..
# cmake --build .

