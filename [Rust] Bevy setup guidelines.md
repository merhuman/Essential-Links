# Bevy Game Engine setup

This is a brief guidelines for compiling Bevy project using x86_64-pc-windows-gnu on Windows OS.

Follow this instruction until you reach command <code>cargo run</code>
[Bevy setup](https://bevyengine.org/learn/book/getting-started/setup/)

If you decide not to use MSVC but Mingw then type following commands into terminal (if you compile a Rust file for the first time)
```console
rustup uninstall toolchain stable-x86_64-pc-windows-msvc
rustup toolchain install stable-x86_64-pc-windows-gnu
rustup default stable-x86_64-pc-windows-gnu
```

Then rerun command <code>cargo run</code> and do the rest of instruction in Bevy setup link. If you encounter error while compiling again, follow the link below instruction and try again.

After compiling, to debug follow the setup in this link below to create launch.json configuration:
[Debugging Rust with VS Code](https://dev.to/rogertorres/debugging-rust-with-vs-code-11dj)

```
// File copied from MacOS X
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "lldb",
            "request": "launch",
            "name": "Debug unit tests in library 'yourprogram'",
            "cargo": {
                "args": [
                    "test",
                    "--no-run",
                    "--lib",
                    "--package=yourprogram"
                ],
                "filter": {
                    "name": "yourprogram",
                    "kind": "lib"
                }
            },
            "args": [],
            "cwd": "${workspaceFolder}"
        }
    ]
}
```
or
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "(Windows) Launch",
            "type": "cppvsdbg",
            "request": "launch",
            "program": "${workspaceRoot}/target/debug/yourprogram.exe",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "console": "externalTerminal"
        }
    ]
}
```

