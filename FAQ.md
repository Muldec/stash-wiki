# Frequently Asked Questions Index
- [What Is Stash?](#what-is-stash)
- [How Is Stash Installed?](#how-is-stash-installed)
- [How do I recover a forgotten username or password?](#how-do-i-recover-a-forgotten-username-or-password)
- [How do I add galleries?](#how-do-i-add-galleries)
- [What's the best way to add metadata to Stash?](#whats-the-best-way-to-add-metadata-to-stash)
- [How do I run stash on OSX or Linux?](#how-do-i-run-stash-on-osx-or-linux)
- [I have a question not answered here.](#i-have-a-question-not-answered-here)

## What is Stash?
Stash is a Go app with a web front-end which organizes and serves your porn. Stash supports macOS, Windows, and Linux (including Docker). Download the latest version [here](https://github.com/stashapp/stash/releases).

## How is Stash installed?
Run the executable (double click the exe on Windows or run `./stash-osx` / `./stash-linux` from the terminal on macOS / Linux) and navigate to either https://localhost:9999 or http://localhost:9998 to get started.

_Note for Windows users_: Running the app might present a security prompt since the binary isn't signed yet. Just click more info and then the "run anyway" button.

_Note for macOS / Linux users_: You might need to run `chmod u+x stash-osx` or `chmod u+x stash-linux` to make the file executable.

If you prefer Docker, see [these instructions](https://github.com/stashapp/stash/blob/develop/docker/production/README.md).

### FFMPEG
If Stash is unable to find or download FFMPEG, then download and install it yourself:

* [macOS](https://ffmpeg.zeranoe.com/builds/macos64/static/ffmpeg-4.0-macos64-static.zip)
* [Windows](https://ffmpeg.zeranoe.com/builds/win64/static/ffmpeg-4.0-win64-static.zip)
* [Linux](https://johnvansickle.com/ffmpeg/releases/ffmpeg-release-amd64-static.tar.xz)

The `ffmpeg(.exe)` and `ffprobe(.exe)` files should be placed in `~/.stash` on macOS / Linux or `C:\Users\YourUsername\.stash` on Windows.

## How do I recover a forgotten username or password?
User authentication was added as of Stash build 707bd09. Stash saves login credentials in the config.yml file. You must reset both login and password if you have forgotten your password by doing the following:
* Close your Stash process
* Open the `config.yml` file found in your Stash directory with a text editor
* Delete the `login` and `password` lines from the file and save
Stash authentication should now be reset with no authentication credentials.

## How do I add galleries?
For gallery related issues check the relevant Wiki [section](https://github.com/stashapp/stash/wiki/Galleries).

## What's the best way to add metadata to Stash?

* Stash includes a single scraper, but you can add more via the [CommunityScrapers repo](https://github.com/stashapp/CommunityScrapers). See the README for installation and usage instructions.
* Pierre Delecto wrote [a Python script](https://github.com/pierre-delecto/stash_theporndb_scraper) for scraping from ThePornDB. This is arguably the fastest way to mass create studios / performers and populate scene data.
* Stash-Box is a separate application from Stash itself - the intent is to allow for crowdsourcing of porn metadata. Right now, Stash-Box is under heavy development. Unless you're planning to contribute code, there isn't much reason to run this yourself for the moment. However, check the pinned messages in the #stash-box channel in Discord to try the client-side interface.

## How do I run stash on OSX or Linux?

Try running `chmod u+x stash-osx` or `chmod u+x stash-linux` to make the file executable.

## How can I connect to my server from elsewhere within my network?

Change the address of the server from 0.0.0.0 to the IP address of the computer on which you are running Stash.

## How do I rename or relocate my library folder?
**If you need to move or rename a folder**, you can remove the existing directory from your library and readd the new location. Stash will recognize the files and re-link to the new location. **Do not run a Clean in between these steps, or you will lose the information from your relocated folders** (your files will not be affected).

> **⚠️ Note:** Don't forget to click `Save` after updating these directories!

## Known Issues
- Performer images uploaded in WebP format will not display on versions of Safari prior to version 13 or on anything earlier than MacOS Big Sur. This is a [limitation of Safari](https://caniuse.com/webp).  As a workaround, ensure you are uploading performer images in jpg or png format.

## I have a question not answered here.
Join the Stash [Discord server](https://discord.gg/2TsNFKt).