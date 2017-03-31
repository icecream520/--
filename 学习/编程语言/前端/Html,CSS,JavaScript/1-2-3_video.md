# video #
## ELEMENTS & ATTRIBUTES WE WILL LOOK AT ##//与音频类似
<video> src attribute
autoplay attribute
controls attribute
loop attribute
alt attribute
ADDING A VIDEO
## Handling video is very similar to handling audio ##
    <video> adds a video to the web page, but doesn't play it//类似
    <video src="walking_video.mp4"></video>
## PLAYING VIDEO ##
    autoplay makes the video start as soon as the page loads
    <video src="walking_video.mp4" autoplay></video>
## ADDING VIDEO CONTROLS ##
Add controls to give the user some video controls
<video src="walking_video.mp4" controls></video>
## SOME WAYS OF HANDLING VIDEO ##
Use loop if you want the video to repeat
    <video src="walking_video.mp4" loop></video>
Use alt for search engines and disabled people
    <video src="walking_video.mp4" alt="Walking the High Junk Peak trail"></video>//类似音频无法加载时此区域会显示这个
Handle older browsers with a message
    <video src="walking_video.mp4" controls>
    <p>Sorry! Your browser does not support the <i>video</i> tag</p>
    </video>