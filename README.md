# Tiny3DLoader

**Tiny3DLoader** is an open source single-file library aiming to load some 3D formats.

**Supported Formats:**
* [glTF](https://github.com/KhronosGroup/glTF/tree/master/specification/1.0)
  * vertices, normals, texcoords and indices 
  * transforms
* [obj](http://www.martinreddy.net/gfx/3d/OBJ.spec)

**Tiny3DLoader** is greatly influenced by libraries such as [assimp](http://www.assimp.org/), [tinyobjloader](https://github.com/syoyo/tinyobjloader), or [tinygltfloader](https://github.com/syoyo/tinygltfloader)

## Design Goals
* **Simple integration.** The code consists of two header files ```tiny-3D-loader.hpp``` and ```json.hpp``` (from [this repository](https://nlohmann.github.io/json/))
* **Simple data-structure.** Loaded data are saved in an easy-to-use tree structure discribed in the [Data Layout section](#data-layout).
* **Lightweight.** Created to handle only few of the most common 3D format.

## Integration
Both files to include are located in the ```includes``` directory.
In order to use **Tiny3DLoader**, you just need to add:
```C++
#include "tiny-3D-loader.hpp"
...
```
to the files in which tou want to handle the loading.

Do not forget to enable C++11 compilation when compiling your code (required by the [json.hpp](https://github.com/nlohmann/json) library).

**Supported compilers:**
* `GCC 4.9.3` or newer
* `Clang 3.6.0` or newer

## Data Layout



## Examples

## Tests
Use [CMake](https://cmake.org/) to build and run the tests:
```sh
$ mkdir build && cd build
$ cmake .. && make check
$ cd bin && ./bin/check
```

## TODO

* glTF
  * [ ] materials
  * [ ] animations
* obj
  * [ ] vertices, normals, texcoords
  * [ ] materials

## Contributing

Contributions are appreciated. You can submit PR on the develop branch, that will later be merged to the master branch.
We also use the [GitHub issues tracker](https://github.com/DavidPeicho/Tiny3DLoader/issues) for bugs and requests, feel free to post your questions/recommandations on it.
