cmake_minimum_required (

	VERSION 	3.19.4
)

get_filename_component (

	self 	"${CMAKE_CURRENT_SOURCE_DIR}" 	NAME
)

project (
	
	${self} 	LANGUAGES 	CXX 
					C 
					ASM
)

add_library (

	${self} 	STATIC 	"src/library.cpp"
					"include/${self}/library.hpp"
)

target_include_directories (

	${self}	PUBLIC	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/${self}>
					$<INSTALL_INTERFACE:include>
)

set_property (

	TARGET 	${self}	PROPERTY 	CXX_STANDARD 20
)

target_compile_features ( 

	${self} 	PUBLIC 	cxx_std_20
)

target_include_directories (

	${self} 	PUBLIC 	"include"
)