# ProgrammerLifeHacks

## Speed up youtube videos

1. Go to the video.
2. Press [[CTRL]] + [[SHIFT]] + [[J]] or [[COMMAND]] + [[OPTION]] + [[J]] to open the JavaScript Console.
3. Copy and paste the following:
```
document.getElementsByTagName("video")[0].playbackRate = x
```
x equals the speed you want; you can have it very specific, f.e. 1,15312 still works
4. Press ENTER.
5. Close the Console with [[CTRL]] + [[SHIFT]] + [[J]] or [[COMMAND]] + [[SHIFT]] + [[C]].
