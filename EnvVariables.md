# `env` variables

## General

* `PIOENV` - The name of the active environment
    * E.g. `pokitto`
* `PIOPLATFORM` - The name of the target platform
    * E.g. `nxplpc`
* `PIOFRAMEWORK` - A list of the target frameworks
    * E.g. `['mbed']`
* `EXTRA_SCRIPTS` - A list of the extra pre and post scripts to be executed
    * Includes flags passed to the `extra_scripts` property in `platformio.ini`

## Global environment

* `ENV` - The user's OS environment variables, stored as a dictionary
* `UNIX_TIME` - Current timestamp in Unix time
* `PYTHONEXE` - A path leading to the python executable
    * E.g. `c:\users\user\.platformio\penv\scripts\python.exe`
* `PIOHOME_DIR` - A path leading to the user's `\.platformio` directory
    * E.g. `c:\users\user\.platformio`
    * E.g. `I:\User\.platformio`
* `SHELL` - A path leading to the user's command line/shell/terminal executable
    * E.g. `C:\Windows\System32\cmd.exe`
* `UPLOAD_PROTOCOL` -
    * E.g. `mbed`
* `TOOLS` - A list of tool names

## Miscellaneous settings

* `MAXLINELENGTH` - ???
    * E.g. `2048`
* `STATIC_AND_SHARED_OBJECTS_ARE_THE_SAME` -
    * 0 if static and shared objects _aren't_ the same
    * 1 if static and shared objects _are_ the same

## Host info

* `HOST_OS` - The name of the operating system of the host computer
    * E.g. `win32`
* `HOST_ARCH` - The name of the architecture of the host computer
    * E.g. `x86_64`

## Target info

* `TARGET_OS` - The name of the operating system of the target board (may be empty)
* `TARGET_ARCH` - The name of the architecture of the target board (may be empty)

## Board info

* `BOARD` - The name of the target board
    * E.g. `lpc11u68`
* `BOARD_MCU` - The name of the target board's MCU
    * E.g. `lpc11u68`
* `BOARD_F_CPU` - The frequency of the target board's CPU
    * E.g. `50000000L`

## Project paths

* `PROJECT_DIR` - A path leading to the project's root directory
* `PROJECTBUILD_DIR` - A path leading to the project's `\.pioenvs` directory
* `PROJECTSRC_DIR` - A path leading to the project's `\src` directory
* `PROJECTINCLUDE_DIR` - A path leading to the project's `\include` directory
* `PROJECTDATA_DIR` - A path leading to the project's `\data` directory
* `PROJECTTEST_DIR` - A path leading to the project's `\test` directory

## Build info

* `BUILD_FLAGS` - A list of build flags
    * Includes flags passed to the `build_flags` property in `platformio.ini`
* `BUILD_SCRIPT` - The path to the main build script
    * E.g. `c:\users\user\.platformio\platforms\nxplpc\builder\main.py`
    * E.g. `I:\User\.platformio\platforms\nxplpc\builder\main.py`

## Build paths

* `BUILD_DIR` - `$PROJECTBUILD_DIR\$PIOENV` (may be unevaluated)
    * I.e. if `PIOENV` is `release`, then `BUILD_DIR` is `<project>\.pioevns\release` (when evaluated)
* `BUILDSRC_DIR` - `$BUILD_DIR\src` (may be unevaluated)
    * I.e. if `PIOENV` is `release`, then `BUILD_DIR` is `<project>\.pioevns\release\src` (when evaluated)
* `BUILDTEST_DIR` - `$BUILD_DIR\test` (may be unevaluated)
    * I.e. if `PIOENV` is `release`, then `BUILD_DIR` is `<project>\.pioevns\release\test` (when evaluated)

## Program info

* `PROGNAME` -
    * E.g. `firmware`
* `PROGPREFIX` -
* `PROGSUFFIX` -
    * E.g. `.elf`
* `PROG_PATH` - `$BUILD_DIR\$PROGNAME$PROGSUFFIX`

## Framework info

* `FRAMEWORKS` - ???
* `FRAMEWORKPATH` -  ???

## Debug info

* `GDB` - The name of the GDB debugger program in use
    * E.g. `arm-none-eabi-gdb`

## C++ info

* `CPPPATH` - A list of paths?
* `CPPSUFFIXES` - A list of file suffixes to be treated as C++ files
    * E.g. `['.c', '.C', '.cxx', '.cpp', '.c++', '.cc', '.h', '.H', '.hxx', '.hpp', '.hh', '.F', '.fpp', '.FPP', '.m', '.mm', '.S', '.spp', '.SPP', '.sx', '.ino']`
* `CPPDEFINES` - A list of defined symbols used when building the target
* `CPPDEFPREFIX` - A prefix used as an argument to the compiler when defining a preprocessor symbol
    * E.g. `-D`
* `CPPDEFSUFFIX` - A suffix used as an argument to the compiler when defining a preprocessor symbol
* `INCPREFIX` - A prefix used as an argument to the compiler when including a file
    * E.g. `-I`
* `INCSUFFIX` - A suffix used as an argument to the compiler when including a file

## C Compiler info

* `CC` - The name of the C compiler
    * E.g. `arm-none-eabi-cc`
* `CCCOM` - The command line used to process the C compiler (may be unevaluated)
    * E.g. `$CC -o $TARGET -c $CFLAGS $CCFLAGS $_CCCOMCOM $SOURCES`
* `CCCOMSTR` - The line of text output to inform the user which target is being compiled (may be unevaluated)
    * E.g. `Compiling $TARGET`
* `CFILESUFFIX` - The suffix of C files
    * E.g. `.c`
* `CFLAGS` - The flags passed to indicate the version of C in use
    * E.g. `-std=c11`
* `CCFLAGS` - The flags passed to the C compiler by default

## C Compiler info for shared files

* `SHCC` - The name of the C compiler
    * E.g. `$CC`
* `SHCCCOM` - The command line used to process the C compiler (may be unevaluated)
    * E.g. `$SHCC -o $TARGET -c $SHCFLAGS $SHCCFLAGS $_CCCOMCOM $SOURCES`
* `SHCFLAGS` - The flags passed to indicate the version of C in use
    * E.g. `$CFLAGS`
* `SHCCFLAGS` - The flags passed to the C compiler by default
    * E.g. `$CCFLAGS`

## C++ Compiler info

* `CXX` - The name of the C++ compiler
    * E.g. `arm-none-eabi-g++`
* `CXXCOM` - The command line used to process the C++ compiler (may be unevaluated)
    * E.g. `$CXX -o $TARGET -c $CXXFLAGS $CCFLAGS $_CCCOMCOM $SOURCES`
* `CXXCOMSTR` - The line of text output to inform the user which target is being compiled (may be unevaluated)
    * E.g. `Compiling $TARGET`
* `CXXFILESUFFIX` - The suffix of C++ files
    * E.g. `.cc`
* `CXXFLAGS` - The flags passed to indicate the version of C++ in use
    * E.g. `-std=c++11`
* `CPPFLAGS` - The flags passed to the C++ compiler by default

## C++ Compiler info for shared files

* `SHCXX` - The name of the C++ compiler
    * E.g. `$CXX`
* `SHCXXCOM` - The command line used to process the C++ compiler (may be unevaluated)
    * E.g. `$SHCXX -o $TARGET -c $SHCXXFLAGS $SHCCFLAGS $_CCCOMCOM $SOURCES`
* `SHCXXFLAGS` - The flags passed to indicate the version of C++ in use
    * E.g. `-std=c++11`

## Assembler info

* `AS` - The name of the assembler (may be unevaluated)
    * E.g. `$CC`
* `ASCOM` - The command line used to process the assembler (may be unevaluated)
    * E.g. `$ASPPCOM`
* `ASCOMSTR` - The line of text output to inform the user which target is being assembled (may be unevaluated)
    * E.g. `Compiling $TARGET`
* `ASFLAGS` - The flags passed to the assembler by default

## Static linker info

* `LINK` - The name of the linker (may be unevaluated)
    * E.g. `$SMARTLINK`
* `LINKCOM` - The command line used to process the linker (may be unevaluated)
    * E.g. `$LINK -o $TARGET $LINKFLAGS $__RPATH ${_long_sources_hook(__env__, SOURCES)} $_LIBDIRFLAGS $_LIBFLAGS`
* `LINKCOMSTR` - The line of text output to inform the user which target is being linked (may be unevaluated)
    * E.g. `Linking $TARGET`
* `LINKFLAGS` - The flags passed to the linker by default

## Shared linker info

* `SHLINK` - The name of the linker (may be unevaluated)
    * E.g. `$LINK`
* `SHLINKCOM` - The command line used to process the linker (may be unevaluated)
    * E.g. `$SHLINK -o $TARGET $SHLINKFLAGS $__SHLIBVERSIONFLAGS $__RPATH $SOURCES $_LIBDIRFLAGS $_LIBFLAGS`
* `SHLINKFLAGS` - The flags passed to the linker by default
    * E.g. `$LINKFLAGS -shared`

## Archiver info

* `AR` - The name of the archiver
    * E.g. `arm-none-eabi-ar`
* `ARCOM` - The command line used to process the archiver (may be unevaluated)
* `ARCOMSTR` - The line of text output to inform the user which target is being archived (may be unevaluated)
* `ARFLAGS` - The flags passed to the archiver by default

## Object file info

* `OBJCOPY` - The name of the object copy executable
    * E.g. `arm-none-eabi-objcopy`
* `OBJPREFIX` - The prefix to prepend to object files
* `OBJSUFFIX` - The suffix to append to object files
    * E.g. `.o`

## LD module info

* `LDMODULE` - ???
    * E.g. `$SHLINK`
* `LDMODULECOM` - ???
    * E.g. `$LDMODULE -o $TARGET $LDMODULEFLAGS $__LDMODULEVERSIONFLAGS $__RPATH $SOURCES $_LIBDIRFLAGS $_LIBFLAGS`
* `LDMODULEFLAGS` - ???
    * E.g. `$SHLINKFLAGS`
* `LDMODULENOVERSIONSYMLINKS` - ???
    * E.g. `$SHLIBNOVERSIONSYMLINKS`
* `LDMODULEPREFIX` - ???
    * E.g. `$SHLIBPREFIX`
* `LDMODULESUFFIX` - ???
    * E.g. `$SHLIBSUFFIX`
* `LDMODULEVERSION` - ???
    * E.g. `$SHLIBVERSION`
* `LDMODULEVERSIONFLAGS` - ???
    * E.g. `$SHLIBVERSIONFLAGS`
* `LDMODULEEMITTER` - ???
    * E.g. `[<function ldmod_emitter at 0x00000000037974A8>]`
* `LDSCRIPT_PATH` - ???
    * E.g. `['.pioenvs\\pokitto\\LPC11U68.ld.link_script.ld']`

## Library system info

* `LIB_DEPS` - ???
    * E.g. `['mbed-mbedtls']`
* `LIB_COMPAT_MODE` - The state of the [Library Dependency Finder](https://docs.platformio.org/en/latest/librarymanager/ldf.html#ldf)'s [compatibility mode](https://docs.platformio.org/en/latest/librarymanager/ldf.html#compatibility-mode)
    * Either `off`, `soft` or `strict`

## Libraries

* `LIBSOURCE_DIRS` - A list of directories to search for library files
    * E.g. `['i:\\Documents\\PlatformIO\\Projects\\Minesweeper\\lib', 'i:\\Documents\\PlatformIO\\Projects\\Minesweeper\\.piolibdeps', '$PIOHOME_DIR\\lib']`
* `LIBPATH` - ???
    * E.g. `['$BUILD_DIR']`
* `LIBS` - ???
    * E.g. `[[<SCons.Node.FS.File object at 0x0000000004CF7488>], [<SCons.Node.FS.File object at 0x0000000004CD7E68>], [<SCons.Node.FS.File object at 0x0000000004CDA088>], [<SCons.Node.FS.File object at 0x0000000004CDD148>], u'stdc++', u'supc++', u'm', u'c', u'gcc', u'nosys', 'c', 'stdc++']`

## Static libraries

* `LIBDIRPREFIX` - A prefix used as an argument to the compiler when specifying a directory to look in for library files
    * E.g. `-L`
* `LIBDIRSUFFIX` - A suffix used as an argument to the compiler when specifying a directory to look in for library files
* `LIBLINKPREFIX` - A prefix used as an argument to the compiler when specifying a static library to link to the executable
    * E.g. `-l`
* `LIBLINKSUFFIX` - A suffix used as an argument to the compiler when specifying a static library to link to the executable
* `LIBPREFIX` - The prefix to prepend to static library files
    * E.g. `lib`
* `LIBSUFFIX` - The suffix to append to static library files
    * E.g. `.a`
* `LIBPREFIXES` - A list of prefixes to prepend to static libaries
    * E.g. `['$LIBPREFIX']`
* `LIBSUFFIXES` - A list of suffixes to append to static libaries
    * E.g. `['$LIBSUFFIX']`

## Shared libraries

`SHLIBPREFIX` - The prefix to prepend to shared library files
`SHLIBSUFFIX` - The suffix to append to shared library files
    * E.g. `.dll`
`SHLIBVERSIONFLAGS` - ???
    * E.g. `-Wl,-Bsymbolic`

## Shared objects

`SHOBJPREFIX` - The prefix to prepend to shared object files
`SHOBJSUFFIX` - The suffix to append to shared object files
    * E.g. `.os`

## Size check

* `SIZETOOL` - The name of the tool used to determine the size of memory sections
    * E.g. `arm-none-eabi-size`
* `SIZECHECKCMD` - The shell command used for printing the size of data sections in compiled code
    * E.g. `$SIZETOOL -A -d $SOURCES`
* `SIZEDATAREGEXP` - A regular expression used to extract the size of data sections in compiled code
    * E.g. `^(?:\.data|\.bss|\.noinit)\s+(\d+).*`
* `SIZEPRINTCMD` - The shell command used for printing the size of of data sections in compiled code
    * E.g. `$SIZETOOL -B -d $SOURCES`
* `SIZEPROGREGEXP` - A regular expression used to extract the size of code sections in compiled code
    * E.g.`^(?:\.text|\.data|\.rodata|\.text.align|\.ARM.exidx)\s+(\d+).*`

## Ranlib?

* `RANLIB` - ???
    * E.g. `arm-none-eabi-ranlib`
* `RANLIBCOMSTR` - ???
    * E.g. `Indexing $TARGET`