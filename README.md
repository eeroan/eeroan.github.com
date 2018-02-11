# Commands usefull for me (in fish shell)

### Create timelapse

```
brew install libvpx
brew install ffmpeg --with-libvpx
ffmpeg -start_number 1 -i FHD%04d.JPG -c:v libx264  timelapse.mp4
```

### Pass each row to a command

```
cat list.txt | while read i ; command $i; end
```

### Open file with TextEdit

```
open -e filename.txt
```

