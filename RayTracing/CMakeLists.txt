cmake_minimum_required(VERSION 3.20)
project(RayTracing)

set(CMAKE_CXX_STANDARD 17)

# Include
include_directories(/usr/local/Cellar/glfw/3.3.8/include)
include_directories(/usr/local/Cellar/glm/0.9.9.8/include)
include_directories(/Users/jessevogel/Development/VulkanSDK/MoltenVK/include)

# Source files
add_executable(RayTracing main.cpp Application.cpp Application.h)

# External libraries
find_package(glfw3 3.3 REQUIRED)
target_link_libraries(RayTracing glfw)
#target_link_libraries(RayTracing /usr/local/lib/libMoltenVK.dylib)
target_link_libraries(RayTracing /Users/jessevogel/Development/VulkanSDK/macOS/lib/libvulkan.1.dylib)
target_link_libraries(RayTracing /Users/jessevogel/Development/VulkanSDK/macOS/lib/libvulkan.1.3.216.dylib)

