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

# /W0	No warnings
# /W1	Basic warnings
# /W2	More warnings
# /W3	Default warnings (moderate)
# /W4	High warning level (strict)
# /Wall	Everything, including noisy system headers

# /W4 is only valid for MSVC
# -Wall -Wextra -Wpedantic are only valid for GCC/Clang