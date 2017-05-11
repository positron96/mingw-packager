# mingw-packager
Packages DLLs needed by an executabe into one dirextory.

It is written to be used instead of windeployqt that cannot be used if project is cross-compiled on linux while target is mingw.

Uses ``objdump`` to scan executable for DLLs and recursively scans all found DLLs. Then it copies required dlls to specified directory.

Written in python v2. Requires modules os, subprocess, sys (All present in most python distributions).

## Usage:

``package <executable_name>`` - will put DLLs to the same folder where executable resides.

