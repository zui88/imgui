add_library(imgui
  "imgui.cpp"
  "imgui_demo.cpp"
  "imgui_draw.cpp"
  "imgui_tables.cpp"
  "imgui_widgets.cpp"
  
  "backends/imgui_impl_glfw.cpp"
  "backends/imgui_impl_opengl3.cpp"
)

target_include_directories(imgui
  PRIVATE ../glfw/include
)

add_library(imgui::imgui ALIAS imgui)

target_include_directories(imgui
  # PUBLIC ${PROJECT_SOURCE_DIR}
  # PUBLIC ${PROJECT_SOURCE_DIR}/backends
  PUBLIC .
  PUBLIC backends
)
