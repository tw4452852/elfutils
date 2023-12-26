# elfutils

This is [elfutils](https://sourceware.org/elfutils/),
packaged for [Zig](https://ziglang.org/).

## How to use it

First, update your `build.zig.zon`:

```
zig fetch --save https://github.com/tw4452852/elfutils/archive/refs/tags/1.3.0.tar.gz
```

Next, add this snippet to your `build.zig` script:

```zig
const elfutils_dep = b.dependency("elfutils", .{
    .target = target,
    .optimize = optimize,
});
your_compilation.linkLibrary(elfutils_dep.artifact("<lib_name>"));
```

Current supported libs:

[x] libelf

This will provide the specified artifact as a static library to `your_compilation`.