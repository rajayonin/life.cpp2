# life.cpp2
An implementation of Conway's Game of Life in [C++2](https://hsutter.github.io/cppfront/).

## Compilation

### Building cppfront
Make sure the `cppfront` git submodule is initialized. You can do this by cloning the repository
with the `--recurse` flag, otherwise run `git submodule update --init`.

To build it, run:
```
cd cppfront/source
g++ cppfront.cpp -std=c++20 -o cppfront
cd ../..
```

### Compiling the executable
You must first transpile from C++2 to C++, with:
```
cppfront/source/cppfront life.cpp2 -p
```

Now you can compile and execute:
```
export CPPFRONT_INCLUDE=$(pwd)/cppfront/include  # path to cppfront header files
g++ life.cpp -std=c++20 -ICPPFRONT_INCLUDE -o life
./life
```


## More information
- [C++2 & cppfront documentation](https://hsutter.github.io/cppfront/)
- [CMake wrapper for cppfront](https://github.com/modern-cmake/cppfront) (requires CMake 3.30+, make, and GCC 14+)
- This was inspired by [my buddy's awful C implementation](https://github.com/Z4na14/Game-Of-Life)
