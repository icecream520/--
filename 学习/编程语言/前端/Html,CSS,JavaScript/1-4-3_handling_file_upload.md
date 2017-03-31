# HANDLING FILE UPLOAD #//处理文件上传
ELEMENTS & ATTRIBUTES WE WILL LOOK AT
<input type="file">
## UPLOADING FILES ##
Two parts: the browser and the server
The server part is discussed later
    <form action="destination" method="post" enctype="multipart/form­data">
           . . . other form input elements go here, if any . . .
          <input type="file" name="fileToUpload">
          <input type="submit">
    </form>
例:
<form method="post" enctype="multipart/form-data" 
      action="http://ihome.ust.hk/~rossiter/cgi-bin/show_everything.php">

    <p>Select the file you want to upload</p>
    <input type="file" name="fileToUpload">	<!--这个指令是选择文件指令，打开文件夹，选择一个文件-->

    <p>Press this button to send it</p>
    <input type="submit" value="Upload the file"><!--文件上传-->

</form>
## THE SERVER PROGRAM ##<!--服务端代码-->
The file is given to the required server program
The server program may do several things
It may move the file into another directory
It may save the file in a database
该文件被提供给所需的服务器程序
服务器程序可以做几件事
它可以将文件移动到另一个目录
它可以保存在数据库中的文件