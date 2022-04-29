# base-cmake

# Configure through command

```bash
mkdir build
cd build
cmake .. -DCMAKE_C_COMPILER=arm-linux-gcc
```

# Choose build targets

The following command shows the targets in CMakeLists.txt that can be compiled.
```bash
cmake --build . --target help
```

```bash
cmake --build . --target xxx
```
