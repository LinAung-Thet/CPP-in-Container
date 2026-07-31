# Create the executable from source file
add_executable(myapp
    MinCoinsForFruits.cpp
)

# Optional: set C++ standard
target_compile_features(myapp PRIVATE cxx_std_17)

# Cross-platform warning flags
if (MSVC)
    target_compile_options(myapp PRIVATE /W4)
else()
    target_compile_options(myapp PRIVATE -Wall -Wextra -Wpedantic)
endif()