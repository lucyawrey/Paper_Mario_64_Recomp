# Paper Mario 64 Recompiled

# Cloning
Clone the project recursively to include git submodules with `git clone --recurse-submodules https://github.com/lucyawrey/Paper_Mario_64_Recomp`. To update submodules if the project is already cloned, instead run `git submodule update --init --recursive`.

# Building
1) Make sure cmake and a C++ 20 or later compiler are installed. To do so on most Linux distributions run `sudo apt update`, then, `sudo apt install build-essential gdb cmake` to get cmake and GCC. On windows, you should use "Visual Studio Build Tools 2022". They can be installed from winget with the command `winget install --id=Microsoft.VisualStudio.2022.BuildTools -e`.
2) Build the `N64Recomp` tool. To do so open a terminal to `lib/N64Recomp` and run the commands `cmake -S . -B build` plus `cmake --build build` to build the project binaries. They will be outputted to build/debug.
3) Put a "Paper Mario NTSC 1.0" ROM in this project's `rom` directory with the name `paper_mario_usa_rev1.z64`.
4) Build the `papermario` decompilation project at `lib/papermario` according to [these instructions](https://github.com/pmret/papermario/blob/main/SETUP.md) and put the resulting `ver/us/build/papermario.elf` file in this project's `rom` directory with the name `paper_mario_usa_rev1.elf`.
5) From the root of this repository run `./lib/N64Recomp/build/N64Recomp paper_mario_usa_rev1.toml` to generate the decompiled C code.

That's as far as I have gotten on the port so far. Next up is to set up a build script to recompile the C code into a native binary. We will need to link N64 Modern Runtime and RT64 in order for anything to work.

# Dependencies
* [N64: Recompiled](https://github.com/N64Recomp/N64Recomp)
* [N64 Modern Runtime](https://github.com/N64Recomp/N64ModernRuntime)
* [RT64](https://github.com/rt64/rt64)
* [papermario (decompilation project)](https://github.com/pmret/papermario)

# Reference Projects
* [Zelda 64: Recompiled](https://github.com/Zelda64Recomp/Zelda64Recomp)
