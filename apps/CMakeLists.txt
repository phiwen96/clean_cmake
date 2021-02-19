cmake_minimum_required (

	VERSION 	3.19.4
)

get_filename_component (

	self	"${CMAKE_CURRENT_SOURCE_DIR}" 	NAME
)

project (

	${self} 	LANGUAGES 	CXX 
					C 
					ASM
)

add_executable (

	${self} 	"src/main.cpp" 
			"include/main.hpp"
)

target_include_directories (

	${self}	PRIVATE	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
					$<INSTALL_INTERFACE:include>
)

set_property (

	TARGET 	${self}	PROPERTY 	CXX_STANDARD 20
)

target_compile_features (

	${self}	PUBLIC 	cxx_std_20
)

target_link_libraries (
	
	${self} 	PUBLIC 	"library"
)