# video-cut-detection
JavaScript video player that plays a ding sound on every cut

## What is a "cut" in video editing?
A "cut" is one of the most fundamental techniques in video editing.
It's essentially a transition from one clip to another, and it’s the simplest
and most straightforward way to move between scenes.

The most common kind of cut is a "straight cut", where one shot instantly changes
to another. No fancy effects—just a simple, clean transition.

## Why play a ding when we detect a cut?
Often when we watch videos, we are not aware that the video has a cut.
We are so used to the "language" of video editing, which in some styles has a lot
of fast cuts. Some TV commercials, documentaries, or other videos, make use of
many straight cuts.

By playing a ding as soon as every cut is detected, this tool allows for insight
into the rhythm, timing, and style of how the video was edited.

## Instructions and how to use
1. To get started, [click here to load up the video player](https://geoff604.github.io/video-cut-detection/).
2. Select your video. (Not to worry, it won't be uploaded anywhere, it just loads it locally in your browser.)
3. Then start playing the video, and you'll hear a ding sound when a cut is detected in the video.

- You can try adjusting the sensitivity slider if the dings are happening too often or not enough.
- You can select a custom ding sound if you want a different "ding" than the default.

## Don't have a video to try?
You can try [this video](https://geoff604.github.io/video-cut-detection/videos/Awesome%20Food%20at%20Lonsdale%20Quay%20Market%20in%20North%20Vancouver%20BC%20Canada%20-%20geoffmobile.mp4) I made, which makes use of a lot of straight cuts.
- [Download it to
your computer first](https://geoff604.github.io/video-cut-detection/videos/Awesome%20Food%20at%20Lonsdale%20Quay%20Market%20in%20North%20Vancouver%20BC%20Canada%20-%20geoffmobile.mp4), and then you can select it in the [web app](https://geoff604.github.io/video-cut-detection/).

## Want a different "ding" sound?
Some more example ding sounds can be found at:
https://github.com/geoff604/video-cut-detection/tree/main/sounds

## How does the cut detection algorithm work?
The CutDetector class implements a video cut detection algorithm using frame differencing and adaptive thresholding.

The algorithm analyzes pixel data from the currently displayed frames as they progress, to detect significant changes between frames.

To improve performance, downscaling and converting to grayscale is done prior to comparing frames in order to
determine if the difference is over the threshold.

Changing the sensitivity slider affects the threshold calculation to make the detection more or less sensitive.

Finally, the class CutDetector fires an event when a cut is detected, and a ding sound is played when the
event is received.

## Who wrote this tool?
[video-cut-detection](https://github.com/geoff604/video-cut-detection/) was written by [Geoff Peters](https://github.com/geoff604/) a software developer based in Vancouver BC Canada.
Initial release was on January 31st 2025.
Feel free to contact Geoff on X at https://x.com/gpeters or email him at geoff@gpeters.com

Thanks for checking out video-cut-detection and have a great day.
