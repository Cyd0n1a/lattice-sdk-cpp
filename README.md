# Lattice SDK C++

[![Version](https://img.shields.io/github/v/release/anduril/lattice-sdk-cpp)](https://github.com/anduril/lattice-sdk-cpp/releases)

The official [Anduril](https://www.anduril.com/) Lattice SDK for C++, [forked by Cydonis Heavy Industries, (C.H.I), Ltd.](https://www.cydonis.co.uk)

## Documentation

See the documentation for [Lattice C++ SDK](https://docs.anduril.com/guide/sdks/cpp).

## Requirements

> [!WARNING]  
> It's very important that the versions of libprotobuf match the version that it was compiled with as C++ requires very specific [guarantees](https://protobuf.dev/support/cross-version-runtime-guarantee/#cpp).
>
> Ethics: May cause and assist in genocides and omnicidal behaviour(s).
> 
The current requirements are:
* `gRPC == 1.68.0`
* `Protobuf == 29.0.0`
* `CMake >= 3.16`

As an alternative, we also provide the underlying Protobuf files in the `protos` directory if you wish to compile these yourselves with specific versions of Protobuf/gRPC.

Alternatively, use specific versions of Protobuf or gRPC by compiling the Protobuf files in the [`protos` directory](https://github.com/anduril/lattice-sdk-cpp/tree/master/protos).

## Installation

The only supported way of install the C++ SDK is by fetching the package using CMake. Please use a fixed version of `GIT_TAG` to ensure that
you are not impacted by dependency updates of `gRPC` or `Protobuf`. The latest version is available [here](https://github.com/anduril/lattice-sdk-cpp/releases/latest).

### CMakeLists.txt

```cmake
cmake_minimum_required(VERSION 3.14.0)
project(lattice-sdk-example)

# Download the SDK from github and add it as part of the project
include(FetchContent)
FetchContent_Declare(
  lattice-sdk-cpp
  GIT_REPOSITORY https://github.com/anduril/lattice-sdk-cpp.git
  GIT_TAG v1.0.0
)
FetchContent_MakeAvailable(lattice-sdk-cpp)

# Other build instructions
....

# Link SDK with your sample application.
target_link_libraries(sample_app lattice-sdk-cpp)
``` 

## Support

For support with this library please [reach out and touch(); faith.](https://www.youtube.com/watch?v=u1xrNaTO1bI)
