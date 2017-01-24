# js-video-player

JavaScript-based video player that can play `mp4`, `mkv` and `webm` with it's own demuxers for MP4 and MKV.

It should have it's own software audio decoders so that it can properly play `mkv` files with AC3/DTS audio.

It can also be extended with software decoders for h264, vp9 and HEVC as a fallback in case the browser does not support them. This is questionable since video decoding is much harder than software decoding on HW and in terms of implementation.

Resources that can be used, all are pure JS:

https://github.com/dailymotion/hls.js - example of a full player that has a demuxer/internal muxer and MediaSource API usage

https://github.com/audiocogs/aurora.js/ - audio decoding framework

https://github.com/gpac/mp4box.js - mp4 demuxer

https://github.com/oeuillot/node-matroska - matroska demuxer

https://github.com/mbebenita/Broadway - h264 decoder 

https://github.com/strukturag/libde265.js - h265 (HEVC) decoder 

https://github.com/audiocogs/aac.js - aac decoder 

## Motivation

There are plenty of videos being encoded in the `mkv` format, in order to take advantage of it's more advanced features and the ability to include AAC/DTS audio. This player will act as pollyfill to browsers which do not support the `mkv` container, and would obviously allow playing the audio in all cases too.
