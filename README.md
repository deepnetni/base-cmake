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
make --build . --target help
```

```bash
make --build . --target xxx
```
