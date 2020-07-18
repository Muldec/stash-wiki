# Inspecting files

You can use the ffprobe command to gather useful information about a video file:

```
ffprobe -show_format -show_streams big_buck_bunny.mkv
```

This can be useful for example, when filing bug reports, or discussing in chat.

# Remuxing files

Another good test, is to see if remuxing the file into a new video file helps:

```
ffmpeg -i big_buck_bunny.mkv -c:v copy -c:a copy remuxed_file.mkv
```

The above command copies the video and audio streams out, and places it into a new file.