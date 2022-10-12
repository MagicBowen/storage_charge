file(GLOB_RECURSE SOURCES CONFIGURE_DEPENDS
    "*.c" "*.C" "*.cc" "*.CC" "*.cpp" "*.CPP" "*.c++"
)

add_library(${TARGET_LIB} STATIC ${SOURCES})

target_include_directories(${TARGET_LIB}
    PUBLIC ${PROJECT_SOURCE_DIR}/include
    PUBLIC ${PROJECT_SOURCE_DIR}/src
)

set_target_properties(${TARGET_LIB} PROPERTIES CXX_STANDARD 17)