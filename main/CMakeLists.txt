# HootsimSDL main

SET(EXECUTABLE_NAME hootsimSDL)

add_executable(${EXECUTABLE_NAME}
	${GL_SRC}

	src/main.cpp
	
	src/HootsimApp.cpp
	src/HootsimSDLApp.cpp
	
	src/DrawManager.cpp
	
	src/graphics/GraphicsBuffer.cpp
	src/graphics/ArrayBuffer.cpp
	
	src/resource/ResourceIndex.cpp
)

include_directories(
	${CMAKE_SOURCE_DIR}/main/src
	${CMAKE_SOURCE_DIR}/hootsim2000/include
	${GL_INCLUDE}
)

target_link_libraries(${EXECUTABLE_NAME}
	hootsim
	${OPENGL_LIBRARIES}
	SDL2
	SDL2_image
)

