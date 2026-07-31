FROM ubuntu:24.04 AS build

RUN apt update && apt install -y \
    build-essential \
    cmake \
    ninja-build \
    gdb

# Copy the entire project folder into /CPP-in-Container
COPY . /CPP-in-Container

# Set working directory to the project root
WORKDIR /CPP-in-Container

# Configure and build project
RUN cmake -B build -S . -G Ninja && \
    cmake --build build

# -------------------------------------------------------------

FROM ubuntu:24.04

# Copy the compiled binary from the build stage
COPY --from=build /CPP-in-Container/build/myapp /usr/local/bin/myapp

# Run the application
CMD ["myapp"]

LABEL Name=leetcode Version=0.0.1