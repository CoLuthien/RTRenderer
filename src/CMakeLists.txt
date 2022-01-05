set(target RTRenderer)

# Define
set(root_dir ${CMAKE_CURRENT_SOURCE_DIR}/../..)


# Sources
file(GLOB_RECURSE sources
    ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

# Build library
add_library(${target} 

STATIC
    ${sources}
)


# Compile options
target_compile_options(${target}
    PRIVATE

    PUBLIC
    ${DEFAULT_COMPILE_OPTIONS}

    INTERFACE
)

target_link_libraries(${target}
    ${SUBMODULES}

    PUBLIC
    PRIVATE

    INTERFACE
)


