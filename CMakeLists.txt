cmake_minimum_required(VERSION 3.27)
project(OpenMoltke)

set(CMAKE_CXX_STANDARD 23)

add_executable(OpenMoltke main.cpp
        inputclass.cpp
        inputclass.h
        systemclass.cpp
        systemclass.h
        applicationclass.cpp
        applicationclass.h
        d3dclass.cpp
        d3dclass.h
        cameraclass.cpp
        cameraclass.h
        colorshaderclass.cpp
        colorshaderclass.h
        modelclass.cpp
        modelclass.h
        textureclass.cpp
        textureclass.h
        textureshaderclass.cpp
        textureshaderclass.h
        lightclass.cpp
        lightclass.h
        lightshaderclass.cpp
        lightshaderclass.h
)

target_link_libraries(OpenMoltke PRIVATE d3d11 d3dx11 dxgi d3dcompiler)
