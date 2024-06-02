cmake_minimum_required(VERSION 3.20)
project(Hello)
set(Headers
    "src/hello.h"
    "src/stdafx.h"
    "src/stdafx_force_includable.h"
)
source_group("Headers" FILES ${Headers})

set(Sources
    "src/hello.cpp"
    "src/stdafx.cpp"
    "src/stdafx_force_includable.cpp"
)
source_group("Sources" FILES ${Sources})


set(ALL_FILES
    ${Headers}
    ${Sources}
)
add_executable(Hello ${ALL_FILES})

target_precompile_headers(Hello PRIVATE
    "src/stdafx_force_includable.h"
)

add_compile_definitions(FORCE_INCLUDE_PRECOMPILED_HEADER 1)