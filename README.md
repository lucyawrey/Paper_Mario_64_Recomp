# Paper Mario 64 Recompiled

# Building
Build https://github.com/N64Recomp/N64Recomp. This is done by:
1) Clone the project recursively (to also clone submodules) with `git clone --recurse-submodules https://github.com/N64Recomp/N64Recomp`.
2) Make sure cmake and a C++ 20 or later compiler are installed. To do so on most Linux distributions run `sudo apt update`, then, `sudo apt install build-essential gdb cmake` to get cmake and GCC. On windows, you should use "Visual Studio Build Tools 2022". They can be installed from winget with the command `winget install --id=Microsoft.VisualStudio.2022.BuildTools -e`.
3) Then open a terminal (VS Command Prompt on windows) to the root of the `N64Recomp` repository and run the commands `cmake -S . -B build` plus `cmake --build build` to build the project binaries, which will be outputted to build/debug.

Once done, place the built binaries `N64Recomp` and `RSPRecomp` in this project's root directory. Then, place the "Paper Mario NTSC 1.0" ROM in this project's `rom` directory with the name `paper_mario_usa_rev1.z64`.

Next, build the papermario decompilation project according to [these instructions](https://github.com/pmret/papermario/blob/main/SETUP.md) and copy the resulting `ver/us/build/papermario.elf` file to this project's `rom` directory with the name `paper_mario_usa_rev1.elf`.

Finally, from the root of this repository run `./N64Recomp paper_mario_usa_rev1.toml` to generate the decompiled C code. That's as far as I have gotten for now but work to turning that C code into a PC port is ongoing using the Zelda64 recomp as a reference.

# Dependencies
* [N64: Recompiled](https://github.com/N64Recomp/N64Recomp)
* [papermario (decompilation project)](https://github.com/pmret/papermario)

# Reference Projects
* [Zelda 64: Recompiled](https://github.com/Zelda64Recomp/Zelda64Recomp)
