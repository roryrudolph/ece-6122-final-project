# ECE 6122 Final Project

- 3D OpenGL Rendering with GLFW3
- Bullet Physics simulations
- Object (.obj) and Material (.mtl) model loading with Assimp
- Text overlay with FreeType
- Raytracing

## Compilation

This project is intended to work on Linux, primarily Ubuntu systems, and has not been fully tested on Windows.  In order to compile properly, a few library dependencies are needed. 

| Library | Package | Description |
|---|---|---|
| OpenGL | libgl1-mesa-dev | Graphics rendering library |
| OpenGL Extension Wrangler | libglew-dev | Helper for loading the proper OpenGL extensions |
| GLM | libglm-dev | OpenGL math library |
| Bullet Physics | libbullet-dev | Physics simulation library |
| FreeType | libfreetype6-dev | Used for uploading and displaying fonts |
| Assimp | libassimp-dev | Handles loading of Wavefront .obj and .mtl files |
| GLFW3 | libglfw3-dev | Windowing and user input (among other things) |
| FFmpeg | ffmpeg | Not a library, per se, but the actual application |
| FreeImage | libfreeimage-dev | Used for image loading, especially with textures |

These libraries can be installed via the apt-get package manager like this:

```sh
$ sudo apt-get install cmake libgl1-mesa-dev libglew-dev libglm-dev libbullet-dev libfreetype6-dev libassimp-dev libglfw3-dev ffmpeg libfreeimage-dev
```

**NOTE**: As of the latest update in May 2018, you have to run the program from the **bin** directory as the file paths for the Wavefront object files are hard-coded. I know this is bad, and it will be fixed later.

```sh
$ git clone https://github.com/roryrudolph/ece-6122-final-project.git
$ cd ece-6122-final-project/
$ mkdir bin
$ cd bin/
$ cmake ..
$ make
```

## TODOs

There are lots of TODO notes in the code, mainly for documentation. Here are some more:

- Don't hardcode object file paths
- Remove dependency on ffmpeg in lieu of libavutil and libavcodec.  I want to put the movie-making process in the code itself, not by calling ffmpeg externally.
- Finish documentation and create Doxygen files.

