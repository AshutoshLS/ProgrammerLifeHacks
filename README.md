# ProgrammerLifeHacks

## Speed up youtube videos

1. Go to the video.
2. Press [[CTRL]] + [[SHIFT]] + [[J]] or [[COMMAND]] + [[OPTION]] + [[J]] to open the JavaScript Console.
3. Copy and paste the following (let speed be 3x):
```
document.getElementsByTagName("video")[0].playbackRate = 3
```
x equals the speed you want; you can have it very specific, f.e. 1,15312 still works
4. Press ENTER.
5. Close the Console with [[CTRL]] + [[SHIFT]] + [[J]] or [[COMMAND]] + [[SHIFT]] + [[C]].

## Find a particular open port and kill it (in Windows)

Let's say it is port 3306 (SQL)
```
netstat -ano | findstr :3306
```
Note the PID xxxx
```
taskkill /pid xxxx /F
```

## Download YouTube video
```
pip install yt-dlp  
```
Use:
```
yt-dlp --verbose https://www.youtube.com/watch?v=[videoId]
```

