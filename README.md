# Project README

## Overview
The project is a C-based GUI interaction system that uses the Alx library for window creation and rendering. It includes features such as creating windows, handling input events, and rendering simple graphical elements.

## Features
- Window creation
- Handling of mouse click events
- Rendering of rectangles with different colors
- Basic GUI interaction system

## Project Structure
```
Gui_InteractionSystem/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── alx.h           # Header file for Alx library functions
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- GCC (C/C++ Compiler)
- Make utility
- Standard development tools
- Alx library

## Build & Run
### Linux
1. Install the necessary libraries and compiler:
   ```sh
   sudo apt-get install build-essential libpng-dev libjpeg-dev
   ```
2. Build the project:
   ```sh
   make -f Makefile.linux all
   ```
3. Run the executable:
   ```sh
   ./build/Main
   ```

### Windows
1. Install MinGW and set it up in your system's PATH.
2. Build the project:
   ```sh
   make -f Makefile.windows all
   ```
3. Run the executable:
   ```sh
   build\Main.exe
   ```

### Wine
1. Install Wine and mingw-w64 on Linux.
2. Build the project for Windows:
   ```sh
   make -f Makefile.wine all
   ```
3. Run the executable using Wine:
   ```sh
   WINEPREFIX=~/wine64 WINEARCH=win64 wine build\Main.exe
   ```

### WebAssembly
1. Install Emscripten and set it up in your system's PATH.
2. Build the project for WebAssembly:
   ```sh
   make -f Makefile.web all
   ```
3. Serve the output with a web server:
   ```sh
   emrun --no_browser --port 8080 build/index.html
   ```

These instructions provide a clear guide on how to build and run the project across different platforms using the provided Makefiles.