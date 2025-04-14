FROM mcr.microsoft.com/devcontainers/cpp:ubuntu-22.04

ARG REINSTALL_CMAKE_VERSION_FROM_SOURCE
RUN if [ -n "$REINSTALL_CMAKE_VERSION_FROM_SOURCE" ]; then \
    wget https://github.com/Kitware/CMake/releases/download/v${REINSTALL_CMAKE_VERSION_FROM_SOURCE}/cmake-${REINSTALL_CMAKE_VERSION_FROM_SOURCE}-linux-x86_64.sh \
    && chmod +x cmake-${REINSTALL_CMAKE_VERSION_FROM_SOURCE}-linux-x86_64.sh \
    && ./cmake-${REINSTALL_CMAKE_VERSION_FROM_SOURCE}-linux-x86_64.sh --skip-license --prefix=/usr/local \
    && rm cmake-${REINSTALL_CMAKE_VERSION_FROM_SOURCE}-linux-x86_64.sh; \
fi
