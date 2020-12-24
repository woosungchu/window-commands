###### Create File
> echo some-text  > filename.txt

###### For loop
```
//임의 파일 5개 만들기
$ for /L %i in (1,1,5) do echo %i > test%i.log
=>result
$ echo 1  1>test1.log
$ echo 2  1>test2.log
$ echo 3  1>test3.log
$ echo 4  1>test4.log
$ echo 5  1>test5.log
```

```
//모든 로그파일 열기
$ for /F %i in ('dir /b *.log') do notepad %i
```

```
//디렉토리 내 모든 동영상 용량 줄이기
$ for /F %i in ('dir /b *.mp4') do ffmpeg -i %i -vcodec h264 -acodec mp2 (output)%i
```
