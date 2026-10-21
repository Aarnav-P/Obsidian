Quick reference on how to use ffmpeg in terminal for Linux users with examples 

Note: Linux is case-sensitive so .mp4 is **incorrect** ­— it's .MP4 instead.
Note: The timestamp for milliseconds is a point not a colon because it's decimalised, bozo.
### Extracting frames from a video

#### Extract one frame at timestamp

``ffmpeg -ss 00:01:23.500 -i input.mp4 -frames:v 1 frame.png

#### Extract one frame by frame number
Frame numbers start at 0.

``ffmpeg -i input.mp4 -vf "select=eq(n\,10)" -frames:v 1 frame_150.png

#### Extract all frames

``mkdir frames  
``ffmpeg -i input.mp4 frames/frame_%06d.png

#### Extract one frame per second

``mkdir frames  
``ffmpeg -i input.mp4 -vf fps=1 frames/frame_%06d.png

#### Extract $n$ frames per second

``mkdir frames  
``ffmpeg -i input.mp4 -vf fps=$n$ frames/frame_%06d.png

#### Extract frames from a time range

``mkdir frames  
``ffmpeg -ss 00:01:00 -to 00:01:10 -i input.mp4 frames/frame_%06d.png

#### Extract every 10th frame

``mkdir frames  
``ffmpeg -i input.mp4 -vf "select='not(mod(n,10))'" -vsync vfr frames/frame_%06d.png

#### Extract as JPEG instead of PNG

``mkdir frames  
``ffmpeg -i input.mp4 frames/frame_%06d.jpg

#### Extract as JPEG with quality setting
Lower number = better quality.

``ffmpeg -i input.mp4 -q:v 2 frames/frame_%06d.jpg

#### Notes
- Use PNG for lossless frames.  
- Use JPG for smaller files.  
- Timestamps use HH:MM:SS.milliseconds.  
- %06d creates numbered files like frame_000001.png.