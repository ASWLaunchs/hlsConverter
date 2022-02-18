# hlsConverter
hlsConverter can convert video to hls.

usage
```go
	ffmpegPath := "E:/env/pkg/ffmpeg-master-latest-win64-gpl-shared/bin/ffmpeg.exe"
	srcPath := "static/assets/videos/example.mp4"
	targetPath := "static/assets/hls"
	framePosition := "1"
	targetFilename := "video.m3u8"
	resOptions := []string{"480p", "720p"}

	//create final targetPath.
	str := strings.Split(srcPath, "/")
	targetPath = path.Join(targetPath, models.MD5(str[len(str)-1]))

	//call HLS converter.
	hlsConverter.Init(targetPath)
	hlsConverter.GeneratePoster(ffmpegPath, srcPath, targetPath, framePosition)
	hlsConverter.HlsConverter(ffmpegPath, srcPath, targetPath, targetFilename, resOptions)
```
