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


# How audio and video are played?
Ans:-

   start| 
------- | 

    |
    V

Media Extractor |
--------------- |

    |
    V

Media Codec |
----------- |
    |
    V

End | 
--- | 


Media Extractor | 
--------------- | 
examine the container type of the media file **-->** create the appropriate extractor **-->** extract the encoded frames. 

Media Codec | 
----------- | 
create the appropriate codec **-->** read the encoded frames **<===>** decode data **-->** end


## Example:-
For Playing an video first we need examine whether it is MP3 container or MP4 container 
Once we know the container we need appropriate experience extractor 
For example if it is MP4 then it contains jpeg4 & avc3 frames.
We need appropriate extractor for that format to fetch it.

Once extractor are ready we can extract the encoded frames from the container.

In order to play we need to decode or decompress the frames so we create a appropriate codec(stands for encode or decode a digital stream)
To decode the frames/read the encoded frames.
Decide the data within frames (literally translated to converting digital data to analog signals).

### Android Media Architecture Extras
- Stagefright is a native-level media playback engine with built-in software-based codecs for several media format.
- Stagefright feature for audio and video playback include integrator with Open Max codecs,session management,time syncronization rendering,transport control and DRM.
- Stagefright supports integration with custom hardware codec (integrated has openmax integration layer IL component)

# imp info
- **OpenCore** is a media framework witch is replaced by Stagefright in Android 2.x. **Stagefright** relies only on OpenMAX interface for all the codecs.
- **StagefrightPlayer** is an implement of AwesomePlayer, it call AwesomePlayer’s API. StagefrightPlayer Constructor
- **NuPlayer** and **AwesomePlayer** both are a **player**. At first NuPlayer is designed for **stream playback**, but it **replaces** AwesomePlayer in Android 5.1 (Lollipop)










http://oopsmonk.github.io/blog/2016/06/16/android-media-framework

refer this for basic.
 
gstreamer coming soon.

https://quandarypeak.com/2013/08/androids-stagefright-media-player-architecture/
