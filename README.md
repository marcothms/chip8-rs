chip8-rs
========

Yet another chip8 emulator written in rust \o/

If you encounter any problems, I encourage you to open a PR!

![PONG](pong.png)

## Games
Due to legal reasons, I can't provide any games nor links to them.
But they can be easily found by using a search engine!

## System Dependencies
`sdl2` together with its dependencies are required to be installed on your host machine.
On Arch-based distros you can use these packages:
`sdl2 sdl2_gfx sdl2_image sdl2_mixer sdl2_ttf`

## On Windows
0. Make sure you have an installation of Visual Studio with the English language pack!
1. Install Rustup from the official website https://www.rust-lang.org/tools/install
2. Download the following `sdl2` dependencies:
    1. https://www.libsdl.org/release/SDL2-devel-2.0.14-VC.zip
    2. https://www.libsdl.org/projects/SDL_image/release/SDL2_image-devel-2.0.5-VC.zip 
    3. https://www.libsdl.org/projects/SDL_mixer/release/SDL2_mixer-devel-2.0.4-VC.zip
    4. https://www.libsdl.org/projects/SDL_ttf/release/SDL2_ttf-devel-2.0.15-VC.zip
3. Unpack the downloaded files.
4. Copy all the files from the `lib` directory of the respective extracted folder to `C:\user\%USERNAME%\.rustup\toolchains\stable-x86_64-pc-windows-msvc\lib\rustlib\x86_64-pc-windows-msvc\lib`.
6. `sdl2_gfx` needs to be compiled for windows manually. Download and Install GitBash https://git-scm.com/downloads
7. Create an empty folder, right-click in it and select "Git Bash Here".
8. Copy and Paste the following command and press Enter `git clone https://github.com/microsoft/vcpkg`. Wait for the download to complete.
9. Close Git Bash and open the new "vcpkg" folder. Run `bootstrap-vcpkg.bat` as administrator. If done correctly a "vcpkg.exe" file should appear.
10. Shift-right-click and select "Open PowerShell Window Here" in the "vcpkg" folder. A command prompt will open.
11. Copy and Paste the following command and press Enter `vcpkg.exe install sdl2-gfx --triplet x64-windows`(It'll give you an error if you're missing VS). 
12. Navigate to \installed\x64-windows\lib in your vcpkg folder and copy `SDL2.lib` and `SDL2_gfx.lib` to `C:\user\%USERNAME%\.rustup\toolchains\stable-x86_64-pc-windows-msvc\lib\rustlib\x86_64-pc-windows-msvc\lib`.
13. Download the source code by clicking the download button at the top of this page and selecting "Download Zip". Extract the file anywhere on your machine.
14. Open a PowerShell Window by shift-right-clicking in the "chip8-rs-master" folder.
15. Copy and Paste the following command and press Enter `cargo build`.

You can now use the emulator by opening a command prompt in your "chip8-rs-master" folder and using the command `cargo run [PATH_TO_FILE]`.
If the emulator doesn't recognize your dump, try putting it in the "chip8-rs-master" folder and use `cargo run [FILENAME]`.

## TODO
[ ] Add Beeper Sound

## Credits
For this project I used help from the following sites:
+ [Chip-8 Technical Reference](http://devernay.free.fr/hacks/chip8/C8TECH10.HTM#3.0)
+ [How to write an emulator (CHIP-8 interpreter)](http://www.multigesture.net/articles/how-to-write-an-emulator-chip-8-interpreter/)
