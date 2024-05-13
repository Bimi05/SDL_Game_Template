# SDL Game Template

## **Tools we're going to use**
- Visual Studio Code
- mingw64
- 7-zip
- SDL 2.0

## **Instructions**

### Downloads
- [**Download**](https://code.visualstudio.com/) Visual Studio Code.
- [**Download**](https://www.7-zip.org) 7-zip.
- [**Download**](https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win64/Personal%20Builds/mingw-builds/8.1.0/threads-win32/seh/x86_64-8.1.0-release-win32-seh-rt_v6-rev0.7z/download) mingw64.
- [**Download**](https://github.com/Bimi05/SDL_Game_Template/archive/refs/heads/master.zip) the repository.
- [**Download**](https://github.com/libsdl-org/SDL/releases) the latest SDL release. You should be looking for a `SDL2-devel-2.x.x-mingw.tar.gz`-like file.

This repository comes with the [`SDL2_image`](https://github.com/libsdl-org/SDL_image/releases), [`SDL2_mixer`](https://github.com/libsdl-org/SDL_mixer/releases) and [`SDL2_ttf`](https://github.com/libsdl-org/SDL_ttf/releases) libraries. If you want to download these as well, look for a similar file to the aforementioned one in each repository above.

In the case you don't want one/more of the above libraries, simply delete the respective `.dll` files from the `SDL2.zip` file, as well as remove the necessary `#include` lines.

### Setting Up
- Unzip the downloaded `.7z` (mingw64) file with 7-zip.
- Cut the unzipped `mingw64` folder and paste it in the local `C:` disk. (Recommended: on the same directory as the `Windows` folder)
- Copy the folder's new location and add it to your system's environment variables (a short guide on that can be found [**here**](https://support.semarchy.com/support/solutions/articles/43000653441-set-environment-variables-using-windows-ui-)).
- Unzip the repository.
- On the local `C:` disk, create a folder, with any name that you want (note that it will contain *__all__* the SDL files)
- Unzip the main SDL `.tar.gz.` archive, and select the `bin`, `include` and `lib` folders inside the `x86_64-w64-mingw32` (or similar) folder.
- Copy the three selected folders in the folder with the SDL files.
- Unzip the `SDL2.zip` file and place its contents in both the `/bin/debug/` and the `/bin/release/` folders.

**If you installed no additional libraries, you can skip the following two steps.**
- Unzip all the SDL libraries you installed, and from a similarly named folder copy the three same folders.
- Paste the folders inside the local disk folder containing the SDL files. In case an overwrite is prompted, select the `Replace all files in destination` option.

### Verify Functionality
- Open Visual Studio Code.
- Select `File > Open Workspace from File` and select the repository's `.code-workspace` file.
- Press `Ctrl+Shift+B` and choose either the `Build (Debug)` or the `Build (Release)` option. You should prefer using the former option, as it's mostly meant for free developer use with all code debugging compiler flags enabled.
- If compilation is successful, a terminal with the text "YIPPEE" should open.