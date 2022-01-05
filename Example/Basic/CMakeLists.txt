# Target name
set(target Basic)

# Includes
include_directories(${CMAKE_CURRENT_SOURCE_DIR})


# Sources
file(GLOB sources
    ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

# Build executable
add_executable(${target}
    ${sources})
    
target_include_directories(${target}
    PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/../../src/
    PRIVATE
)


# Compile options
target_compile_options(${target}
    PRIVATE
    PUBLIC
)


# Link libraries
target_link_libraries(${target}
    PUBLIC
    RTRenderer
    PRIVATE
    )
