# Visual Studio 2022 OpenGL Graphics Template
A simple template for starting OpenGL graphics (64x) with all dependencies included.

 ---

![image](https://github.com/MaxineCodes/VS2022-OpenGL-Graphics-Template/blob/main/git_img/screenshot.jpg)

 ---

 ## Structure: 

The software is separated into two projects: Core and App. App builds into App.exe which includes Core.dll as a library. This ensures that Core.dll can be used as an external library. This template is made with graphics rendering in mind and Core is thus meant as a rendering engine that can be tacked on to another project.

It is recommended to rename Core to the name of the project. Easiest way to do this is by manually editing the .vcxproj files. 

```
Repository
|
|-- Dependencies            # Dependencies are included in the repository
|   |-- glew-2.1.0
|   |-- glfw-3.4.bin.WIN64
|   |-- glm-0.9.9.8
|   |-- imgui
|   `-- stb
|
|-- Binaries                # This folder is only shown/generated when building
|
|-- Application             # Contains all the interesting stuff
|   |-- App                 # Builds as an .exe using Core.dll, this is where you run the program
|   |   `-- Source
|   `-- Core                # Core contains the implementation that is built into a .dll
|       `-- Source
|           ` Core          # Core.h exposes the 'api' of Core.dll and is included in App.exe
|
`-- git_img                 # Web preview stuff for github
```
 ---

## Building:

This project should compile and link properly on Microsoft Visual Studio 2022 (17) with any compiler supporting C++ 20 or higher on Windows x64.
The dependencies are included in the repository and do not require to be downloaded and linked manually.
OpenGL is required. It is assumed that OpenGL is pre-installed on the system.

 ---

 ## Dependencies:
 - GLEW 2.1.0
 - GLFW 3.4
 - imgui
 - stb_image
 - glm 0.9.9.8

---
