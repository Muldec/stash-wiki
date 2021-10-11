# Stash F.A.Q.s - Frequently Asked Questions (and Answers)
[Installing and Configuring](#launching) • 
[Logging In](#logging-in)  • 
[Working With Content](#working-with-content)  • 
[Troubleshooting](#troubleshooting) •
[Other](#other)



## Launching
- [How do I get into Stash once installed?](#How-do-I-get-into-Stash-once-installed)
## Logging In
- [How do I recover a forgotten username or password?](#how-do-i-recover-a-forgotten-username-or-password)
- [How can I connect to my server from elsewhere within my network, or via the internet?](#how-can-i-connect-to-my-server-from-elsewhere-within-my-network-or-via-the-internet)
## Working With Content
- [What's the best way to add metadata to Stash?](#whats-the-best-way-to-add-metadata-to-stash)
- [How do I add galleries?](#how-do-i-add-galleries)
- [How do I rename or relocate a content folder?](#how-do-i-rename-or-relocate-a-library-folder)

## Troubleshooting
- [Known Issues](#known-issues)
- [FFMPEG Errors](#stash-is-showing-a-ffmpeg-not-found-error)
## Other
- [I have a question not answered here.](#i-have-a-question-not-answered-here)



# Installing and Launching
The installation instructions are available from the [README.md](https://github.com/stashapp/stash).
## How do I get into Stash once installed?
#### Windows
- Run the executable (typically "stash-win.exe"). The app will start up in a terminal window, read in your configuration and then give you a URL to connect with in your browser.
- _Note for Windows users_: Running the app might present a security prompt since the binary isn't signed yet. Just click more info and then the "run anyway" button.
#### Mac OS / Linux
-  Run `./stash-osx` / `./stash-linux` from the terminal on macOS / Linux)
-   _Note for Mac/Linux users_: If you have trouble, try running `chmod u+x stash-osx` or `chmod u+x stash-linux` to make the file executable.


** Navigate to http://localhost:9999 to get started. **

# Logging In
## How do I recover a forgotten username or password?
Stash saves login credentials in the config.yml file. You must reset both login and password if you have forgotten your password by doing the following:
* Close your Stash process
* Open the `config.yml` file found in your Stash directory with a text editor
* Delete the `login` and `password` lines from the file and save
Stash authentication should now be reset with no authentication credentials.

## How can I connect to my server from elsewhere within my network?

Find the local IP address of your Stash Server (guides for [Windows](https://support.microsoft.com/en-us/windows/find-your-ip-address-in-windows-f21a9bbc-c582-55cd-35e0-73431160a1b9), [MacOS](https://support.apple.com/guide/mac-help/find-your-computers-name-and-network-address-mchlp1177/11.0/mac/11.0), [Linux](https://wiki.archlinux.org/title/Network_configuration#IP_addresses)). Then, on another device on your local network, open a browser to http://SERVER.IP.ADDRESS.HERE:9999/


# Working With Content

## What's the best way to add metadata to Stash?

* Stash includes a single scraper, but you can add more via the [CommunityScrapers repo](https://github.com/stashapp/CommunityScrapers). See the README for installation and usage instructions.
* Pierre Delecto wrote [a Python script](https://github.com/ThePornDatabase/stash_theporndb_scraper) for scraping from ThePornDB. This is arguably the fastest way to mass create studios / performers and populate scene data.
* StashDB is a service that allows for crowdsourcing of porn metadata. Check the pinned messages in the #stash-box-qa2 channel in Discord to start using it.

## How do I rename or relocate a library folder?
**If you need to move or rename a folder**, you can remove the existing directory from your library and readd the new location. Stash will recognize the files on the next scan and re-link to the new location. **Do not run a Clean in between these steps, or you will lose the information from your relocated folders** (your files will not be affected).

> **⚠️ Note:** Don't forget to click `Save` after updating these directories!

## How do I add galleries?
For gallery-related issues check the relevant Wiki [section](https://github.com/stashapp/stash/wiki/Galleries).
# Troubleshooting
## Known Issues
- Performer images uploaded in WebP format will not display on versions of Safari prior to version 13 or on anything earlier than MacOS Big Sur. This is a [limitation of Safari](https://caniuse.com/webp).  As a workaround, ensure you are uploading performer images in jpg or png format.

## Stash is showing a "FFMPEG Not Found" error
If Stash is unable to find or download FFMPEG, then download and install it yourself:

You can find links to pre-compiled binaries [here](https://github.com/stashapp/stash#pre-compiled-binaries).

The `ffmpeg(.exe)` and `ffprobe(.exe)` files should be placed in `~/.stash` on macOS / Linux or `C:\Users\YourUsername\.stash` on Windows.


# Other FAQs

## I have a question not answered here.
Join the Stash [Discord server](https://discord.gg/2TsNFKt).