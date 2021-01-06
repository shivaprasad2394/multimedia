# multimedia

## Android Multimedia Framework Overview
### Component
- Codec & Parser
- Player
- Streaming
- Broadcasting
- Audio
- Media db
- Media editor
- Media Scanner
- FM Radio
- Recorder

# Terms
 - Muxing
 - Demuxing
 - Digital Container format
 - Audio flinger
 - Surface Flinger

# What is multimedia Framework
- MMF is a Software framework that handles media on a computer and through a network ex:- streaming 

## MMF Architecture Supports 
- Audio 
- Video
- Container formats
- Transmission Format

## Used by
- Media Player Apps
- Audio Editor Apps
- Video Editor Apps
- Media Convertors

## History of Android Media Framework

- Android 1.0 -->Packet video-open core
- Android 1.6 -->Open core 2.0
- Android 2.0 -->Stagefright
- Android 2.1 -->Stagefright
- Android 2.3 -->Stagefright with enhancements
- Android 3.0 -->Stagefright +HLS for firsttime
- Android 4.1 -->SF Support for MediaCodec
- Android 5.0 -->MediaSession and MediaControllers introduces 
- Android 5.1 -->Nuplayer

Attempt | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
Seconds | 301 | 283 | 290 | 286 | 289 | 285 | 287 | 287 | 272 | 276 | 269

# How audio and video are played?
Ans
      Start |
      ---|
      |
      |
      v
    
examine the container type of the media file -->create the appropriate extractor -->extract the encoded frames -->create the appropriate codec-->read the encoded frames-->decode data-->end

For Playing an video first we need examine whether it is MP3 container or MP4 container 
Once we know the container we need appropriate experience extractor 
For example if it is MP4 then it contains jpeg4 & avc3 frames.
We need appropriate extractor for that format to fetch it.

Once extractor are ready we can extract the encoded frames from the container.

In order to play we need to decode or decompress the frames so we create a appropriate codec(stands for encode or decode a digital stream)
To decode the frames/read the encoded frames.
 Decide the data within frames (literally translated to converting digital data to analog signals).














http://oopsmonk.github.io/blog/2016/06/16/android-media-framework

refer this for basic.
 
gstreamer coming soon.

https://quandarypeak.com/2013/08/androids-stagefright-media-player-architecture/
