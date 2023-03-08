# matterport downloader equirectangular

## What does

matterport-dl-equi downloads Skybox 360 panos photos of Matterport houses and turn them into equirectangular images automatically, this allows to view the pano in viewers like Ricoh Theta https://play.google.com/store/apps/details?id=com.theta360&hl=en&gl=US  

This project is a simple merge of two projects:

https://github.com/fdd4s/matterport-downloader  
https://github.com/fdd4s/skybox2equirectangular  

## Dependencies

php, php-curl, curl, imagemagick, ffmpeg (last version with v360 filter), exiftool  

this code is designed to work over linux (as /dev/shm ram tmpfs)  

## Usage

    $ php ./matterport-dl-equi.php <matterport id>  

e.g: If the url is https://my.matterport.com/show/?m=huhpm6maGbT&mls=1 you have to run the script this way:  

    $ php ./matterport-dl-equi.php huhpm6maGbT  

It will download all the skybox images with the highest quality available (4k, 2k or 1k) and turn them into equirectangular images.  

## Known issues

"montage-im6.q16: cache resources exhausted " can be resolved changing ImageMagick configuration, more info here: https://github.com/ImageMagick/ImageMagick/issues/396  

## Online downloader

https://openpano.rf.gd/download/ shows skybox images of matterport virtual tours, with the browser option "save web complete" it downloads all skybox images of a matterport virtual tour. It's the online version of the script https://github.com/fdd4s/matterport-downloader

## Viewers

Android: Ricoh Theta App https://play.google.com/store/apps/details?id=com.theta360&hl=en&gl=US  

PC: Linux/Mac/Windows: Panini https://github.com/lazarus-pkgs/panini  

Web Browser: Chrome and Firefox: Pannellum (webgl based), self hosted virtual tour, equirectangular and cubemap skybox: https://github.com/mpetroff/pannellum 

## Youtube 360 slideshow video

Equirectangular panoramas can be uploaded to Youtube as a 360º video slideshow. It can be created using FFmpeg (like a normal slideshow of jpg images), add the tag to the video of 360º panoramic using "spatial-media" and upload to youtube where the slideshow video will be shown as a 360º video.  

https://github.com/FFmpeg/FFmpeg  
https://github.com/google/spatial-media  

## Credits

Created by fdd  
Send feedback and questions to fdd4776s@gmail.com  
Support future improvements of this software https://www.buymeacoffee.com/fdd4s  
All files are public domain https://unlicense.org/  
