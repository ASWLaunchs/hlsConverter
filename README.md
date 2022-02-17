# hlsConverter
hlsConverter can convert video to hls.

```
ffmpegPath := "E:/env/pkg/ffmpeg-master-latest-win64-gpl-shared/bin/ffmpeg.exe"
	srcPath := "static/assets/videos/example.mp4"
	targetPath := "static/assets/videos"
	framePosition := "1"
	targetFilename := "example.m3u8"
	resOptions := []string{"480p"}

	hlsConverter.Init(targetPath)
	hlsConverter.GeneratePoster(ffmpegPath, srcPath, targetPath, framePosition)
	hlsConverter.HlsConverter(ffmpegPath, srcPath, targetPath, targetFilename, resOptions)
```
