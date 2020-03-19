Stash offers support for image galleries.
Here are some remarks on using them:

- **Galleries are zip-folders with images (e.g. jpeg or png) in them.**
- Stash searches for zip galleries in the same paths it searches for videos.
- If you want to add a gallery to a scene, make sure that the zip file and the video file are in the same folder.
- As of commit **9dacad7** stash adds a gallery to its related scene during the scanning process if they have matching names. Gallery `/my/stash/collection/media_filename.zip` will be auto assigned to `/my/stash/collection/media_filename.mp4` (where **mp4** can be _avi_, _mkv_, _wmv_ ... or any other media file we support).
- Stash always reads image files directly from the zip files. With huge images, this can be slow and cause visual errors in the ui.