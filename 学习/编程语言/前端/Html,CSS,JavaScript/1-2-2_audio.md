# audio #
ELEMENTS & ATTRIBUTES WE WILL LOOK AT
<audio> src attribute
autoplay attribute
controls attribute
loop attribute
## HANDLING SOUND ##
    <audio> by itself adds a soundfile, but doesn't play it
    <audio src="beets_turnips.mp3"></audio>//只添加不播放，需要注意的是中文现在不行，等以后学的多了应该就会了
    autoplay makes the sound start as soon as the page loads//自动播放
    <audio src="beets_turnips.mp3" autoplay></audio> 
## SOUND CONTROLS ##音乐控制器
<audio src="beets_turnips.mp3" controls></audio>
Add controls to tell the browser to show playback controls//会有一个音乐控制器，可以控制音量等
## LOOPING SOUND ##
Add loop to repeat the sound indefinitely//添加循环属性无线循环，上面的控制器也可以添加
<audio src="drum_loop.mp3" autoplay loop></audio>
## SOUND IN OLDER BROWSERS ##
In general, for sound it's wise to use MP3 format sound
This is supposed to work in all modern browsers//mp3属性支持任何现代浏览器
## HANDLING NEW TAGS IN OLDER BROWSERS ##//给旧的浏览器标签提醒
Older browsers can't handle newer HTML tags
To be friendly, you can warn the user:
    <this_new_html_tag>
    <p>Sorry, your browser can't handle <i>this_new_html_tag</i>!</p>
    </this_new_html_tag>
An older browser ignores <this_new_html_tag> because it
doesn't understand it, but it does understand <p> so it correctly
displays the paragraph
A newer browser understands everything, but deliberately ignores
the paragraph//旧版本浏览器无法识别这段话，但能识别<p></p>所以会打印出那段话，但是新版本会自动的忽略
## AN EXAMPLE OF HANDLING OLDER BROWSERS ##如何处理就浏览器的例子
Here's an example using audio:
<audio src="drum_loop.mp3" autoplay>
<p>Sorry! Your browser does not support the <i>audio</i> tag</p>
</audio>//只能这么认为，应该也是这么认为自动忽视音频文件下的不是音频文件的内容
    <audio src="xixiang.mp3"  autoplay alt="A splashy 3 second drum piece">//alt属性指的是如果当前音频，图片没有加载正确，那么就会出现这样的提示
    <p>Sorry! Your browser does not support the <i>audio</i> tag</p>
    </audio>