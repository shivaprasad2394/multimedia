# multimedia
http://oopsmonk.github.io/blog/2016/06/16/android-media-framework

refer this for basic.
 
gstreamer coming soon.

https://quandarypeak.com/2013/08/androids-stagefright-media-player-architecture/
 
How audio and video are played?
Ans-
Start -->examine the container type of the media file -->create the appropriate extractor -->extract the encoded frames -->create the appropriate codec-->read the encoded frames-->decode data-->end

For Playing an video first we need examine whether it is MP3 container or MP4 container 
Once we know the container we need appropriate experience extractor 
For example if it is MP4 then it contains jpeg4 & avc3 frames.
We need appropriate extractor for that format to fetch it.

Once extractor are ready we can extract the encoded frames from the container.

In order to play we need to decode or decompress the frames so we create a appropriate codec(stands for encode or decode a digital stream)
To decode the frames/read the encoded frames.
 Decide the data within frames (literally translated to converting digital data to analog signals).

