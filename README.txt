Prebuilt MinGW Playstation 2 Toolchain - 2018/10/19
---------------------------------------------------

The MinGW directory and its contents must be unpacked to C:\ (i.e. as C:\MinGW).
Unpacking it to some other place may cause the tools to not work.

To open the MinGW terminal, which has the development environment set up: run MinGW\msys\1.0\msys.bat.

Version Information
-------------------
This package contains a prebuilt PlayStation 2 homebrew toolchain, libraries and tools.
All these were the latest-possible versions, as of the date of packaging:
- EE, IOP & DVP toolchains
- Homebrew PS2SDK
- gsKit
- ps2sdk-ports: libjpeg, libpng, zlib & freetype
- ps2-client
- ps2-packer lite
- MinGW + MSYS: version 2012/04/26. Includes only the C compiler, MinGW & MSYS system.

What's not included?
--------------------
- Git: there is a proper Windows version, which you can install easily.
- wget: I could not find an up-to-date version. Not needed anyway, unless you use the toolchain scripts.

Additional notes:
-----------------
When the toolchain was built, I worked around the incompatibility between the old
Binutils Autoconf script and MinGW's stdint.h file by appending the contents of stdint.h to sys/types.h.
I have restored sys/types.h to its original contents while creating this pre-built package.

In the future, I plan to improve on the current toolchain patches to allow MinGW to build the toolchains properly.
