# build-plugin-nsunzip

Test fixture for [nsis-dev/build-plugin](https://github.com/nsis-dev/build-plugin).

**Covers:** The large outlier. Info-ZIP UnZip plus a wrapper: ~40 files in 4 subdirectories, `../` includes, defines the old project file passed on the command line, and its own NSIS stack code (StackFunc.h) that defines `g_stacktop`, `g_stringsize` and `g_variables`. Since build-plugin always compiles `pluginapi.c` in, linking currently fails with multiple definitions.

**Changed from upstream:** The `.dsp` defines `WINDLL`, `DLL`, `USE_EF_UT_TIME` moved to the top of `unzip.h`; backslashes in `#include` paths became slashes. The Info-ZIP license is the top-level LICENSE.
