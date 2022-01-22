# Bevy Game Engine setup

This is a brief guidelines for compiling Bevy project using x86_64-pc-windows-gnu on Windows OS.

Follow this instruction until you reach command <code>cargo run</code>
[Bevy setup](https://bevyengine.org/learn/book/getting-started/setup/)

If you decide not to use MSVC but Mingw then type following commands into terminal
```console
rustup uninstall toolchain stable-x86_64-pc-windows-msvc
rustup toolchain install stable-x86_64-pc-windows-gnu
rustup default stable-x86_64-pc-windows-gnu
```
Then rerun command <code>cargo run</code> and do the rest of instruction in Bevy setup link. If you encounter error while compiling again. Follow the link below instruction and try again.
