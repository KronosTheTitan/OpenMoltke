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
        src/shader_classes/colorshaderclass.cpp
        src/shader_classes/colorshaderclass.h
        modelclass.cpp
        modelclass.h
        textureclass.cpp
        textureclass.h
        src/shader_classes/textureshaderclass.cpp
        src/shader_classes/textureshaderclass.h
        lightclass.cpp
        lightclass.h
        src/shader_classes/lightshaderclass.cpp
        src/shader_classes/lightshaderclass.h
        src/shader_classes/refractionshaderclass.cpp
        src/shader_classes/refractionshaderclass.h
        rendertextureclass.cpp
        rendertextureclass.h
        src/shader_classes/watershaderclass.cpp
        src/shader_classes/watershaderclass.h
)

target_link_libraries(OpenMoltke PRIVATE d3d11 d3dx11 dxgi d3dcompiler dinput8 dxguid)

file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/OpenMoltke")
file(COPY data/models DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/OpenMoltke")
file(COPY data/textures DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/OpenMoltke")
file(COPY data/shaders DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/OpenMoltke")
