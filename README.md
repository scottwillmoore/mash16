**NOTE.** This is a fork of tykel's Chip16 emulator. It is assumed to have the best compatibility and support for various Chip16 ROMs. I have modified the emulator so that it can be compiled and run with vs2017. I plan to add additional code to the emulator in order to create a test platform for [my Chip16 emulator written in Rust](https://github.com/scottwillmoore/chip16). This should involve creating a new file format for testing Chip16 emulators. This file format should be language agnostic so that anyone implementing a Chip16 emulator can use it to test compatibility.

# Mash16 -- Reference Chip16 Emulator

## Summary

Mash16 is an emulator for the [Chip16](http://github.com/tykel/chip16) platform, which aims to make writing
emulators easier for beginners.

It is one of the reference emulators, and hence supports the full instruction set.
The user is encouraged to read the source code.

[Download here!](https://github.com/tykel/mash16/releases/latest)

## Screenshots

![Screenshot #1](http://i.imgur.com/hIDyxMAm.png) _ ![Screenshot #2](http://i.imgur.com/v6Y9fg1m.png)    
![Screenshot #3](http://i.imgur.com/ltCzAk4m.png) _ ![Screenshot #4](http://i.imgur.com/NJHhTKDm.png)

## Features

- Full support of the latest (1.3) Chip16 specification
- Debugging functionality (breakpoints, stepping, state viewing)
- Multiple video scalers
- Unrestricted emulation speed possible

## Usage
    mash16 filename [OPTIONS]

## Options
    --no-audio              : disable audio output
    --audio-sample-rate=n   : set audio sample rate (8000,11025,22050,44100 recommended)
    --audio-buffer=n        : set audio buffer size (512-8192 recommended)
    --verbose               : log emulation
    --video-scaler=n        : screen scaler size (1,2,3,4)
    --fullscreen            : use fullscreen mode
    --no-cpu-limit          : do not restrict the speed of the emulation

    --cpu-rec               : use (experimental) recompiler core

    --break@n               : add a breakpoint at address n
    --break-all             : break at every instruction
    --help                  : print the help text
    --version               : print version information
    
## Supported platforms

Mash16 is officially supported on Linux and Windows. OS X testing is welcome.
- On Linux, it has been tested with GCC and Clang. Build with the Makefile.
  - Cross-compiling for Windows is possible from Linux; build the `windows` target (`make windows`).
    Do not forget to specify your MinGW prefix (use `make windows WIN_PREFIX=...`); the default is `i486-mingw32`.
- On Windows, it has been tested with Visual Studio 2010. Build with the provided solution files.

## More Screenshots

![Screenshot #5](http://i.imgur.com/EpVg5Nbm.png) _ ![Screenshot #6](http://i.imgur.com/zIfy3mtm.png)
![Screenshot #7](http://i.imgur.com/rVa3UKLm.png) _ ![Screenshot #8](http://i.imgur.com/KRpuCQem.png)
