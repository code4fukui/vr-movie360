# vr-moive360

- https://code4fukui.github.io/vr-movie360/

## ffmpeg

```
ffmpeg -i R0011033.MP4 -vf eq=brightness=0.3 -t 1 -y skijam.mp4
ffmpeg -i R0011033.MP4 -vf eq=contrast=1.2:gamma=2 -t 1 -ss 16 -y skijam.mp4
ffmpeg -i R0011033.MP4 -vf eq=contrast=1.2:gamma=2  -ss 16 -y skijam.mp4
```

### 分割

- https://tecsingularity.com/ffmpeg/movdiv/
- https://nico-lab.net/cutting_ffmpeg/

### フレーム切り出し

-r [fps] -q:v [quality (1:max, 5:little low)]
```
ffmpeg -i skijam.mp4 -r 2 -q:v 5 img/skijam-%06d.jpg
```

## 3D movie

to inject 3d meta data
- https://github.com/google/spatial-media

