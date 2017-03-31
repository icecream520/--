# CSS3 文本效果 #
CSS3 文本效果
CSS3中包含几个新的文本特征。
在本章中您将了解以下文本属性：
text-shadow
box-shadow
text-overflow
word-wrap
word-break
CSS3的文本阴影
CSS3中，text-shadow属性适用于文本阴影。
Text shadow effect!
您指定了水平阴影，垂直阴影，模糊的距离，以及阴影的颜色：
OperaSafariChromeFirefoxInternet Explorer
实例
给标题添加阴影:
h1
{
text-shadow: 5px 5px 5px #FF0000;
//第一个是左偏移，第二个是下，第三个是阴影程度
}
## CSS3 box-shadow属性 ##
CSS3中CSS3 box-shadow属性适用于盒子阴影
实例
div { 
box-shadow: 10px 10px; 
}
接下来给阴影添加一个模糊效果
实例
div { 
box-shadow: 10px 10px 5px grey; 
}
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  div.card {
      width: 250px;
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
      text-align: center;
  }
  div.header {
      background-color: #4CAF50;
      color: white;
      padding: 10px;
      font-size: 40px;
  }
  div.container {
      padding: 10px;
  }
  </style>
  </head>
  <body>
  <h2>卡片</h2>
  <p>box-shadow 属性用来可以创建纸质样式卡片:</p>
  <div class="card">
    <div class="header">
      <h1>1</h1>
    </div>
    <div class="container">
      <p>January 1, 2016</p>
    </div>
  </div>
  </body>
  </html>
## CSS3 Text Overflow属性 ##
CSS3文本溢出属性指定应向用户如何显示溢出内容
实例
p.test1 { 
white-space: nowrap; 
width: 200px; 
border: 1px solid #000000; 
overflow: hidden; 
text-overflow: clip; 
} 

p.test2 { 
white-space: nowrap; 
width: 200px; 
border: 1px solid #000000; 
overflow: hidden; 
text-overflow: ellipsis; 
}
## CSS3的换行 ##
如果某个单词太长，不适合在一个区域内，它扩展到外面：
CSS3中，自动换行属性允许您强制文本换行 - 即使这意味着分裂它中间的一个字：
CSS代码如下：
OperaSafariChromeFirefoxInternet Explorer
实例
允许长文本换行:
p {word-wrap:break-word;}
### CSS3 Word Breaking ###
CSS3 Word Breaking属性指定换行规则：
CSS代码如下：
实例
p.test1 { 
word-break: keep-all; 
//单词与单词之间不允许换行
} 

p.test2 { 
word-break: break-all; 
//单词与单词之间允许换行，就是可以不是单个单词
}
## 新文本属性 ##
属性	描述	CSS
hanging-punctuation	规定标点字符是否位于线框之外。	3
punctuation-trim	规定是否对标点字符进行修剪。	3
text-align-last	设置如何对齐最后一行或紧挨着强制换行符之前的行。	3
text-emphasis	向元素的文本应用重点标记以及重点标记的前景色。	3
text-justify	规定当 text-align 设置为 "justify" 时所使用的对齐方法。	3
text-outline	规定文本的轮廓。	3
text-overflow	规定当文本溢出包含元素时发生的事情。	3
text-shadow	向文本添加阴影。	3
text-wrap	规定文本的换行规则。	3
word-break	规定非中日韩文本的换行规则。	3
word-wrap	允许对长的不可分割的单词进行分割并换行到下一行。