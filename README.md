# bazel-cake

## Configure toolchain
Create `.bazelrc` in the project root and include the following:
```
build --cxxopt="-std=c++14"
build --cxxopt="-Wpedantic"
build:debug --cxxopt="-g"
```

## Building
All targets in all package directories:
```
bazel build //...:all

# Debug build
bazel build --config debug //...:all
```

Clean up:
```
bazel clean
```
