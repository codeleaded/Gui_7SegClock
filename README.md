# Project README

## Overview
This project is a 7-segment clock GUI application written in C. It utilizes the WindowEngine library for window management and the DD7Segment library to handle 7-segment display rendering.

## Features
- Displays the current time on a 7-segment LED display.
- Supports multiple build targets (Linux, Windows, Wine, WebAssembly).

## Project Structure

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries:
  - For Linux: X11 for window management, PNG and JPEG libraries for asset handling.
  - For Windows: User32, GDI32, Winmm for window management.

## Build & Run

### Linux
```sh
cd <Project>
make -f Makefile.linux all
make -f Makefile.linux exe
```

### Windows
```sh
cd <Project>
make -f Makefile.windows all
make -f Makefile.windows exe
```

### Wine (Linux cross compile for Windows)
```sh
cd <Project>
make -f Makefile.wine all
make -f Makefile.wine exe
```

### WebAssembly (using Emscripten)
```sh
cd <Project>
make -f Makefile.web all
make -f Makefile.web exe
# Open http://localhost:8080 in a browser to run the application
```

## Targets
- `all`: Build the application.
- `do`: Clean and build, then execute the application.
- `clean`: Remove build artifacts.

Each target is specific to the respective operating system or build configuration.