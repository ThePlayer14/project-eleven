# project-eleven
A native PC recompilation of the Xbox 360 version of 11eyes CrossOver PC recompilation using ReXGlue.

## Building

If you want to build from source you'll need:

* ReXGlue SDK
* CMake
* Visual Studio / MSVC
* Clang 20+
* Your legally owned game files

## Setup
* Get the `Nightly 0.8.1.68-dev.g8dadea6` or newer release of the ReXGlue SDK.
* Put your your own legally owned game's XEX file into `extracted`.
* Copy the path to `rexglue` or `rexglue.exe` from the downloaded SDK, then in the downloaded `project-eleven` archive, run `rexglue --verbose --log-file ../logs/recomp.log codegen`
* After codegen is successful, run `cmake --preset linux-amd64-relwithdebinfo -DCMAKE_PREFIX_PATH=/path/to/rexglue-sdk` to configure (be sure to select your platform), if not sure, check `CMakePresets.json`)
* Build the code with `cmake --build out/build/linux-amd64-relwithdebinfo` (Again, be sure to select your platform)

## Legal

This repository does not contain any game assets, game code, ROMs, XEX files, textures, audio, or other copyrighted material.

You must provide your own game files.
