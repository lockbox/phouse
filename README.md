# pee-house

setup to examine my cats business so she doesnt get nervous and we can
monitor the frequency and severity of individual visits due to her
bladder cancer.

## Setup

Running on a raspberry pi 4:
- [frigate](https://frigate.video)
- hostname: `pee-house.local`
- connected: 
  - coral-micro for object detection
    - afaics there is no support for coral micro...TBD
  - usb camera

## Camera Details

```bash
$ ffmpeg -f v4l2 -list_formats all -i /dev/video0
[video4linux2,v4l2 @ 0xaaaac726ead0] Compressed:       mjpeg :          Motion-JPEG : 2560x1440 1920x1080 1280x720 640x480 640x360 320x240
[video4linux2,v4l2 @ 0xaaaac726ead0] Raw       :     yuyv422 :           YUYV 4:2:2 : 640x480 640x360 320x240
[video4linux2,v4l2 @ 0xaaaac726ead0] Compressed:        h264 :                H.264 : 2560x1440 1920x1080 1280x720 640x480 640x360 320x240
```

Options:
 - MJPEG @ 2560x1440 1920x1080 1280x720 640x480 640x360 320x240
 - H264 @  2560x1440 1920x1080 1280x720 640x480 640x360 320x240
