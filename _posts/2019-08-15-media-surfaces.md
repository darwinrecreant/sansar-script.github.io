---
layout: post
author: "Binah"
title:  "Media Surfaces"
date:   2019-08-12 00:00:00 -0700
categories: media
---

## Media Surface

A `Media Surface` is a shader that uses open source, Chromium Ebeded Framework (CEF),  to embed a web browser onto objects in Sansar. Any object can be used as media surface, you can upload your own or get one in the store. 

### Creating a media surface

For this demo we'll get a [cube](https://store.sansar.com/listings/7da07036-5c29-46ba-b100-51a496eee289/basic-mesh-cube) and a [sphere](https://store.sansar.com/listings/b9b9c54a-9089-4171-9faf-dcdb87d59191/prim-sphere) from the store. Enter or create a scene and drag out the cube and the sphere. 

Right click the sphere and choose `Materials` option, or select cube and use `Ctrl + Shift + M` to open Materials Settings.

![Materials editor]({{ site.baseurl }}/assets/images/streaming-media/right-click-materials.png)

Using the top right dropdown labeled `Use Shader` select `Media Surface` option. You can optionally apply maps to your shader but they may affect media playback.

![Materials editor]({{ site.baseurl }}/assets/images/streaming-media/materials-media-surface.png)

Do the same for the sphere object but this time choose `Media Surface + Stereographic`. Stereographic is a special shader capable of displaying stereographic video for a 3D effect in VR, while in desktop mode only the left eye is shown. The orientation of the left and right can be adjusted using the `Rotation Factor` setting - [rotation factor specifications](https://help.sansar.com/hc/en-us/articles/360028946151-Shaders#Media-Surface-+-Stereographic). 

![Materials editor]({{ site.baseurl }}/assets/images/streaming-media/rotation.png)

### Streaming Media to surface

Media stream urls can be set through the `Scene Settings` panel in the `Media Surfaces` section.

![Media Surface Settings in Scene Settings]({{ site.baseurl }}/assets/images/streaming-media/media-surfaces.png)

Only one media stream can be played at a time in a scene, but a scene may have multiple media surfaces playing the same media.

Note the Initial Width & Height settings if a video looks blurry, especially if it's being played on a large surface, increase these values in multiples to start. For YouTube videos on a 16x9-ish surface, setting this to 1920x1080 will give a lot clearer quality.

You must add an audio emitter and audio stream to hear the audio. You may have up to 4 different audio streams in an experience. 

Add the audio stream url (the same as the media url) in the `Audio Streams` section of `Scene Settings` just above the `Media Surfaces` section. Then drag an audio emitter from your System Inventory and set the `Sound Source` to `Stream`.

![Materials editor]({{ site.baseurl }}/assets/images/streaming-media/audio-emitter-settings.png)

With Audio/Video Preview ON, changing settings will update the media surface in realtime, making it easy for you to fine-tune results.

![Audio Video Preview]({{ site.baseurl }}/assets/images/streaming-media/audio-video-preview.png)

### Formatting a YouTube embed URL for media surfaces

YouTube (including live content) is officially supported for video playback. For the best playback experience, you need to format your Media Stream URL using specific flags:

http://www.youtube.com/embed/**[VIDEO_ID]**?autoplay=1&loop=1&controls=0&allowfullscreen=1&playlist=**[VIDEO_ID]**

**[VIDEO_ID]** - the unique ID for the video

**autoplay=1** - starts the video

**loop=1** - assumes you want your video to loop over and over

**controls=0** - optional, to hide controls, the controls at the bottom of the player are not interactive in Sansar

**allowfullscreen=1** - takes up the whole screen (note not all videos will play with this setting)

**playlist[VIDEO_ID]=** - note the video ID must be repeated twice

[more options can be found here](https://developers.google.com/youtube/player_parameters#Parameters)

To find the video id, click the share lnk for your video.

![YouTube share link]({{ site.baseurl }}/assets/images/streaming-media/yt-share.png)

The id will be after the `/`.

![YouTube share link]({{ site.baseurl }}/assets/images/streaming-media/yt-video-id.png)

### YouTube - livestream

Similar to a single video, except the video ID refers to a livestream instead of a recorded video.

Also, YouTube channels have fixed URLs that may be simpler to embed. You'll need to get its channel ID, then put it in a format like this:

https://www.youtube.com/embed/live_stream?channel=**[[CHANNEL_ID]]**

You can find you share link at the top of your streaming page.

![YouTube Live]({{ site.baseurl }}/assets/images/streaming-setup/yt-share-link.png)

[(read more about how to setup your own free YouTube streaming here)]({{ site.baseurl }}/streaming/media/2019/08/08/youtube-streaming-setup.html)

### YouTube - playlists
You can play a playlist of multiple videos in Sansar, too.

If you're embedding a playlist, make sure to test the whole playlist in a web browser and Sansar first. Some videos on the playlist may not play back as expected, depending on permissions restrictions. For example, if this is the playlist:

![YouTube playlist link]({{ site.baseurl }}/assets/images/streaming-media/yt-playlist.png)

then the media surface URL is:

https://www.youtube.com/embed?%20listType=playlist%20&list=**[[PLAYLIST_ID]]**&autoplay=1&loop=1&controls=0


It should play fine for the first few videos in Sansar, but eventually you may get content errors like this:

![YouTube content error]({{ site.baseurl }}/assets/images/streaming-media/yt-content-error.png)

### For Twitch - livestream

Recommended settings 
- Resolution = 1920x1080 (or 2048x1158 for a wee bit more, hardly noticeable)
- Media surface material emissive intensity between 0.15 and 0.50 (default is 1.0, glows too much and washes out video)
- Use the following format, where the green text is the channel name:
http://player.twitch.tv/?channel=**[[CHANNEL_NAME]]**&quality=source&volume=1

**quality=source** - tries to enforce the highest original recording quality. 

**volume=1** -  sets it so Twitch plays at maximum volume. (By default, it plays at 50%.)

### Twitch - single pre-recorded videos
A similar format to livestreams

http://player.twitch.tv/?video=**[[VIDEO_ID]]**&quality=source&volume=1

http://player.twitch.tv/?video=**[[VIDEO_ID]]**&quality=source&volume=1

The number is the video ID you see in the URL when browsing videos.

![YouTube playlist link]({{ site.baseurl }}/assets/images/streaming-media/twitch-id.png)

For pre-recorded videos at a specific time

http://player.twitch.tv/?video=**[[VIDEO_ID]]**&quality=source&volume=1&time=0h0m0s

### Vimeo
Popular site for curated short films and more "artistic" endeavors. The format is like this:

https://player.vimeo.com/video/**[[VIDEO_ID]]**?autoplay=1&loop=1&autopause=0

### Mixer
Website for streaming games live, comparable to Twitch:

https://mixer.com/embed/player/**[[VIDEO_ID]]**



#### Useful links

[Creating a media surface](https://help.sansar.com/hc/en-us/articles/360000144963-Creating-a-media-surface)

[Detailed information on shaders](https://help.sansar.com/hc/en-us/articles/360028946151-Shaders)

[Using and previewing streams](https://help.sansar.com/hc/en-us/articles/115003259666-Using-and-previewing-media-streams)


