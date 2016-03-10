# notes-for-streaming-video

notes for streaming video

## HLS

- HTTP Live Streaming Examples
  - https://developer.apple.com/streaming/examples/
  - https://developer.apple.com/streaming/examples/basic-stream.html
  - https://developer.apple.com/streaming/examples/advanced-stream.html
  - https://developer.apple.com/streaming/examples/advanced-stream-tvos.html

- Apple HTTP Live Streaming (HLS)
  - https://walterebert.com/playground/video/hls/

### MIME Type

| File Extension | MIME Type             |
|----------------|-----------------------|
| .M3U8          | application/x-mpegURL |
| .M3U8          | vnd.apple.mpegURL     |
| .ts            | video/MP2T            |

### HTML example

```html
<video width="640" height="480" preload="none" controls>
  <source type="application/x-mpegURL" src="http://domain/path/filename.m3u8" />
</video>
```

### videojs-media-sources

- https://github.com/videojs/videojs-contrib-media-sources

### Video.js HLS Source Handler

- http://videojs.github.io/videojs-contrib-hls
- https://github.com/videojs/videojs-contrib-hls

## RTMP

- RTMP
  - http://wiki.multimedia.cx/?title=RTMP
- RTMP Samples
  - http://wiki.multimedia.cx/?title=RTMP#Samples

### HTML example

```html
<video width="640" height="480" preload="none" controls>
  <!-- via Amazon CloudFront -->
  <source type="rtmp/mp4" src="rtmp://domain/cfx/st/path/filename.mp4" />
  <!-- with video.js -->
  <source type="rtmp/mp4" src="rtmp://domain/cfx/st/&mp4:path/filename.mp4" />
</video>
```

### Video.js

- http://blog.videojs.com/post/60471080014/videojs-420-released-rtmp-css-designer-and

> &lt;source src="rtmp://your.streaming.provider.net/cfx/st/&mp4:path/to/video.mp4" type="rtmp/mp4"&gt;
>
> The connection and stream parts are determined by splitting the URL on the first ampersand (&) or the last slash (/).

- https://github.com/videojs/video.js/blob/v5.8.2/docs/guides/tech.md#enabling-streaming-playback

> In order to force the Flash tech to choose streaming playback, you need to provide a valid streaming source before other valid Flash video sources.
>
> &lt;source src="rtmp://your.streaming.provider.net/cfx/st/&mp4:path/to/video.mp4" type="rtmp/mp4"&gt;
>
> &lt;source src="http://your.static.provider.net/path/to/video.mp4" type="video/mp4"&gt;
>
> &lt;source src="http://your.static.provider.net/path/to/video.webm" type="video/webm"&gt;

## video.js API

- video.js API Documentation Index
  - http://docs.videojs.com/docs/api/index.html
- videojs
  - http://docs.videojs.com/docs/api/video.html
- Player
  - http://docs.videojs.com/docs/api/player.html
