# CSS 图片 #
本章节将为大家介绍如何使用 CSS 来布局图片。
圆角图片
实例
圆角图片:
img {
    border-radius: 8px;
}
实例
椭圆形图片:
img {
    border-radius: 50%;
}
缩略图
我们使用 border 属性来创建缩略图。
实例
img {
    border: 1px solid #ddd;
    border-radius: 4px;
    padding: 5px;
}

<img src="paris.jpg" alt="Paris">
实例
a {
    display: inline-block;
    border: 1px solid #ddd;
    border-radius: 4px;
    padding: 5px;
    transition: 0.3s;
}

a:hover {
    box-shadow: 0 0 2px 1px rgba
    (0, 140, 186, 0.5);
}

<a href="paris.jpg">
  <img src="paris.jpg" alt="Paris">
</a>
响应式图片
响应式图片会自动适配各种尺寸的屏幕。
实例中，你可以通过重置浏览器大小查看效果:
如果你需要自由缩放图片，且图片放大的尺寸不大于其原始的最大值，则可使用以下代码：
实例
img {
    max-width: 100%;
    height: auto;
}
卡片式图片
实例
div.polaroid {
    width: 80%;
    background-color: white;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

img {width: 100%}

div.container {
    text-align: center;
    padding: 10px 20px;
}
## 图片滤镜 ##
SS filter 属性用为元素添加可视效果 (例如：模糊与饱和度) 。
注意: Internet Explorer 或 Safari 5.1 (及更早版本) 不支持该属性。
实例
修改所有图片的颜色为黑白 (100% 灰度):
img {
    -webkit-filter: grayscale(100%); /* Chrome, Safari, Opera */
    filter: grayscale(100%);
}
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
<style>
img {
    width: 33%;
    height: auto;
    float: left;
    max-width: 235px;
}

.blur {-webkit-filter: blur(4px);filter: blur(4px);}
.brightness {-webkit-filter: brightness(250%);filter: brightness(250%);}
.contrast {-webkit-filter: contrast(180%);filter: contrast(180%);}
.grayscale {-webkit-filter: grayscale(100%);filter: grayscale(100%);}
.huerotate {-webkit-filter: hue-rotate(180deg);filter: hue-rotate(180deg);}
.invert {-webkit-filter: invert(100%);filter: invert(100%);}
.opacity {-webkit-filter: opacity(50%);filter: opacity(50%);}
.saturate {-webkit-filter: saturate(7); filter: saturate(7);}
.sepia {-webkit-filter: sepia(100%);filter: sepia(100%);}
.shadow {-webkit-filter: drop-shadow(8px 8px 10px green);filter: drop-shadow(8px 8px 10px green);}
</style>
</head>
<body>

<p><strong>注意:</strong> Internet Explorer <span lang="no-bok">或 Safari 5.1 (及更早版本)</span> 不支持该属性。</p>

<img src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="blur" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="brightness" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="contrast" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="grayscale" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="huerotate" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="invert" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="opacity" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="saturate" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="sepia" src="77777.jpg" alt="Pineapple" width="300" height="300">
<img class="shadow" src="77777.jpg" alt="Pineapple" width="300" height="300">

</body>
</html>
## 响应式图片相册 ##
.responsive {
    padding: 0 6px;
    float: left;
    width: 24.99999%;
}

@media only screen and (max-width: 700px){
    .responsive {
        width: 49.99999%;
        margin: 6px 0;
    }
}

@media only screen and (max-width: 500px){
    .responsive {
        width: 100%;
    }
}
## 图片 Modal(模态) ##
本实例演示了如何结合 CSS 和 JavaScript 来一起渲染图片。
首先，我们使用 CSS 来创建 modal 窗口 (对话框), 默认是隐藏的。
然后，我们使用 JavaScript 来显示模态窗口，当我们点击图片时，图片会在弹出的窗口中显示：
实例
// 获取模态窗口
var modal = document.getElementById('myModal');

// 获取图片模态框，alt 属性作为图片弹出中文本描述
var img = document.getElementById('myImg');
var modalImg = document.getElementById("img01");
var captionText = document.getElementById("caption");
img.onclick = function(){
    modal.style.display = "block";
    modalImg.src = this.src;
    modalImg.alt = this.alt;
    captionText.innerHTML = this.alt;
}

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
    modal.style.display = "none";
}
//alt属性是当图片不显示的时候，显示的字符