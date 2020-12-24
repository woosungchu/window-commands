
### 비디오 용량 줄이기
```
$ffmpeg -i input.mp4 -vcodec h264 -acodec mp2 output.mp4
```
```
//디렉토리 내 모든 동영상 용량 줄이기
$ for /F %i in ('dir /b *.mp4') do ffmpeg -i %i -vcodec h264 -acodec mp2 (output)%i
```


### 비디오 합치기
```
ffmpeg -i intro.mp4 -c copy -bsf:v h264_mp4toannexb -f mpegts temp1.ts
ffmpeg -i 3.mp4 -c copy -bsf:v h264_mp4toannexb -f mpegts temp2.ts
// now join
ffmpeg -i "concat:temp1.ts|temp2.ts" -c copy -bsf:a aac_adtstoasc output3.mp4
```

### 유튜브 - 파일 확장자 변환
```
ffmpeg.exe -i .\\video${index}.webm .\\video${index}.mp4 -y`
```
