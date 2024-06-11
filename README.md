# Paper Mario 64 Recompiled

# Building
Build https://github.com/N64Recomp/N64Recomp. This is done by:
1) Clone the project recursively (to also clone submodules) with `git clone --recurse-submodules https://github.com/N64Recomp/N64Recomp`.
2) Make sure cmake and a C++ 20 or later compiler is installed. On windows, you should use "Visual Studio Build Tools 2022". They can be installed from winget with the command `winget install --id=Microsoft.VisualStudio.2022.BuildTools -e`.
3) In a terminal (VS Command Prompt on windows) run the commands `cmake -S . -B build` and `cmake --build build` to build the project binaries, which will be outputted to build/debug.

Once done, place the built binaries `N64Recomp` and `RSPRecomp` in this project's root directory. Then, place the "Paper Mario NTSC 1.0" ROM in this project's `rom` directory with the name `paper_mario_usa_rev1.z64`.

# Reference Projects
https://github.com/Zelda64Recomp
https://github.com/N64Recomp/N64Recomp
https://github.com/pmret/papermario
