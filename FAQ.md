# What is Stash?
Stash is a Go app with a web front-end which organizes and serves your porn. Stash supports macOS, Linux, and Windows. Download the latest version [here](https://github.com/stashapp/stash/releases).

# How is Stash installed?
Run the executable (double click the exe on Windows or run `./stash-osx` / `./stash-linux` from the terminal on macOS / Linux) and navigate to either https://localhost:9999 or http://localhost:9998 to get started.

_Note for Windows users_: Running the app might present a security prompt since the binary isn't signed yet. Just click more info and then the "run anyway" button.

## FFMPEG
If stash is unable to find or download FFMPEG then download it yourself from the link for your platform:

* [macOS](https://ffmpeg.zeranoe.com/builds/macos64/static/ffmpeg-4.0-macos64-static.zip)
* [Windows](https://ffmpeg.zeranoe.com/builds/win64/static/ffmpeg-4.0-win64-static.zip)
* [Linux](https://johnvansickle.com/ffmpeg/releases/ffmpeg-release-amd64-static.tar.xz)
The `ffmpeg(.exe)` and `ffprobe(.exe)` files should be placed in `~/.stash` on macOS / Linux or `C:\Users\YourUsername\.stash` on Windows.

# I'm unable to run the app on OSX or Linux
Try running `chmod u+x stash-osx` or `chmod u+x stash-linux` to make the file executable.

# I have a question not answered here.
Join the Stash [Discord server](https://discord.gg/2TsNFKt).