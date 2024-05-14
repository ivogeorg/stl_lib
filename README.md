### stl_lib

#### `clang++` C++ standard version

To find out what version of the C++ standard `clang++` is executing, preprocess an empty file and extract the `__cplusplus` definition:
`echo | clang++ -dM -E -x c++ - | grep __cplusplus`

The result is something like:
`#define __cplusplus 201402L`

This means C++14.

#### Ignoring executables without extensions

1. Tried `**` but it didn't work.
2. At the end of work with repo, find all files without extensions and add `git rm` them.