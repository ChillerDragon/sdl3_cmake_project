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

## Ready to use github actions for builds

There is a CI pipeline in the ``.github/`` directory that tests the build
on macOS, windows and linux. It requires no setup and the produced builds can be downloaded
from github. This allows you to quickly distribute a release for other platforms without cross compilation.


Click on the green pipeline checkmark -> Details -> Summary and scroll down to download the artifacts.

![click checkmark](https://raw.githubusercontent.com/ChillerDragon/cdn/refs/heads/master/sdl3/artifacts0.png)
![click details](https://raw.githubusercontent.com/ChillerDragon/cdn/refs/heads/master/sdl3/artifacts1.png)
![click download](https://raw.githubusercontent.com/ChillerDragon/cdn/refs/heads/master/sdl3/artifacts2.png)

These builds are not perfect for distribution yet. Because they do not bundle the SDL3 dependency.
But they offer you a good starting point and maybe one day I will improve the pipeline.

