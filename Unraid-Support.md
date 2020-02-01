Currently stash is supported in Unraid via the [CA](https://forums.unraid.net/topic/38582-plug-in-community-applications/) plugin.

Selecting **stash** and getting the latest update from dockerhub should get you the latest stable release from our docker image.

A sample container configuration is shown below.
![unraid-stash-docker](https://i.imgur.com/GzCIjA3.jpg)

Here we changed the default repository to `stashapp/stash:development-x86_64` to get the latest development docker image  as it provides a lot more features (optional but recommended for now) .

If needed you can change the `Network Type` from `bridge` to `host`.

You only need to adjust the volume settings.
* data: where your media collection is
* config: where the config file and the stash database file will be stored
* <del> transcodes: location of the transcoded files to be generated </del> transcodes isn't actually used here.The transcodes directory is created by default in the generated volume. 
* metadata: the main metadata folder , used for import/export functions
* cache: a folder to use as cache
* generated: where the previews,screenshots,transcoded files and sprites will be generated


