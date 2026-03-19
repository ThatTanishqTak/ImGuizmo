project(imguizmo)

add_library(imguizmo STATIC ImGuizmo.cpp)

target_include_directories(imguizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(imguizmo PUBLIC imgui)

if(MSVC)
    target_compile_options(imguizmo PRIVATE /W0)
    set_property(TARGET imguizmo PROPERTY COMPILE_WARNING_AS_ERROR OFF)
endif()