# imgui-impl-ctr

ImGui for Nintendo 3ds...

# Example
## Building
```powershell
git submodule update --init --recursive
cd example
make
```
# Portlib
## Building
```powershell
git submodule update --init --recursive
cd portlib
make
```
## Installing
Copy the generated `include/` and `lib/` folders `portlib/` to the 3ds portlibs folder of your DEVKITPRO instalation
```shell
${DEVKITPRO}\portlibs\3ds
```
Then, in your project's Makefile, add `-limgui-impl-ctr` and its dependencies to your `LIBS` option.
```makefile
LIBS	:= -limgui-impl-ctr -lstdc++ -lcitro3d -lctru -lm
```
## Info
The example is based on imgui v1.87 but you can use any other version ass well by just teting if it works...
# TODO
- [ ] Support ttf fonts/build font atlas
# Credits
- [Mathaeuz](https://github.com/Mathaeuz) : portlib fork
- [Tobi-D7](https://github.com/Tobi-D7) : make the code more imgui_impl like
- [mtheall](https://github.com/mtheall) : ftpd's imgui code
- [devkitpro](https://github.com/devkitPro) : libctru, citro3d 