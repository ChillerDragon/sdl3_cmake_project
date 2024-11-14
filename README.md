# sdl3_cmake_project
Cross platform sample setup to quickstart your SDL3 C++ project.


It uses the system wide SDL3 installation by default. And automatically
falls back to downloading SDL3 from source and compiling it.
Works on linux, macOS and windows. No need to manually install sdl.


Example on how to play snake in 3 commands on linux:

```
cmake -B build/
cmake --build build/
./build/sdl3_cmake_project
```

