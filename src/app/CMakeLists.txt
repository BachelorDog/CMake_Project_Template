cmake_minimum_required(VERSION 3.10)

#set project name
project(SPH_APP)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)

file(	GLOB SPH_APP_SRC
	"*.h"
	"*cpp"
	)

#add the executable
add_executable(SPH_APP ${SPH_APP_SRC}) 

target_link_libraries(  SPH_APP PUBLIC
			${OPENGL_LIBRARIES}
			${GLUT_LIBRARY})

target_include_directories(	SPH_APP INTERFACE 
				${CMAKE_CURRENT_SOURCE_DIR} 
				${OPENGL_INCLUDE_DIRS}
				${GLUT_LIBRARY}
				)
