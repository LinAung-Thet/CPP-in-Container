FROM ubuntu:24.04 AS build

RUN apt update && apt install -y \
    build-essential \
    cmake \
    ninja-build \
    gdb \
    git \
    lldb \
    python3-lldb

# Copy the entire project folder into /CPP-in-Container
COPY . /CPP-in-Container

# Set working directory to the project root
WORKDIR /CPP-in-Container

# # Configure and build project
# RUN cmake -B /opt/build -S /CPP-in-Container -G Ninja && \
#     cmake --build /opt/build

# # -------------------------------------------------------------

# FROM ubuntu:24.04

# # Copy the compiled binary from the build stage
# COPY --from=build /CPP-in-Container/build/mincoin /usr/local/bin/mincoin

# # Run the application
# CMD ["mincoin"]

# LABEL Name=leetcode Version=0.0.1