Stash offers support for image galleries.
Here are some remarks on using them:

- **Galleries are zip-folders with images (e.g. jpeg or png) in them.**
- Stash searches for zip galleries in the same paths it searches for videos.
- If you want to add a gallery to a scene, make sure that the zip file and the video file are in the same folder.
- When storing images in zip file make sure to disable compression ( copy , store or no compression options depending on the software you use). This impacts **heavily** on the zip read performance.
- Stash uses the golang native ( pure go ) image decoders ( more suitable for cross compilation ). With huge images, decoding and converting to thumbnails can be slow and  in cases cause visual errors or delays in the gallery page.
- As of commit **9dacad7** stash adds a gallery to its related scene during the scanning process if they have matching names. Gallery `/my/stash/collection/media_filename.zip` will be auto assigned to `/my/stash/collection/media_filename.mp4` (where **mp4** can be _avi_, _mkv_, _wmv_ ... or any other media file we support).
- As of commit **29336d1** a cover image is supported. If an image called xxxxxx**cover.jpg** (where xxxxxx can be any filename) exists in the zip file it will be treated like a cover and presented first in the gallery view page and as a gallery cover in the gallery list view. If more than one images match the name the first one found in natural sort order is selected.