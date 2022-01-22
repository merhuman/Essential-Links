# Bevy Game Engine setup

Follow this instruction until you reach command <code>cargo run</code>
[Bevy setup](https://bevyengine.org/learn/book/getting-started/setup/)

If you decide not to use MSVC but Mingw then type following commands into terminal
<code>
rustup uninstall toolchain stable-x86_64-pc-windows-msvc
rustup toolchain install stable-x86_64-pc-windows-gnu
rustup default stable-x86_64-pc-windows-gnu
</code>

Then rerun command <code>cargo run</code>
