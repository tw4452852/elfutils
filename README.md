# libelf

This is [libelf](https://github.com/arachsys/libelf),
packaged for [Zig](https://ziglang.org/).

## How to use it

First, update your `build.zig.zon`:

```
zig fetch --save https://github.com/tw4452852/libelf_zig/archive/refs/tags/0.190.0.tar.gz
```

Next, add this snippet to your `build.zig` script:

```zig
const libelf_dep = b.dependency("libelf", .{
    .target = target,
    .optimize = optimize,
});
your_compilation.linkLibrary(libelf_dep.artifact("elf"));
```