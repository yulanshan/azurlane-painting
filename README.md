# azurlane-painting
碧蓝航线绘图日记画图工具

## 使用
### 基本使用
- 显示帮助信息
    ```./alpainting.exe -h```
- 合成图片
    ```./alpainting.exe -m image heres-an-image.jpg```
- 合成视频
    ```./alpainting.exe -m video heres-a-video.mp4```
### 详细参数
|指令|含义|默认|
|:---:|---|:---:|
|-m|指定模式,后面跟image或video来指定图片或视频模式|image|
|-o|在后面跟上输出路径来指定输出路径,图片请以.png结尾,视频请以.avi结尾| |
|-x|合成后的宽,后面跟数字,数字为几则横向用几块画板拼一起|1|
|-y|合成后的高,后面跟数字,数字为几则纵向用几块画板拼一起|1|
|-c|仅视频模式下有效,后面跟数字,数字为几则原视频每几帧取出一帧合成新视频|1|
|-b|边缘加粗,后面跟数字,数字越大则加粗越显著.不为0时,**只能为单数**|0
### 使用示例
- ```./alpainting.exe D:\neko.png -m image -o D:\neko_al.png -x 1 -y 1 -b 0```  
    指定输入文件为```D:\neko.png```,模式为```image```,输出到```D:\neko_al.png```,宽```1```个画板,高```1```个画板,不使用加粗边缘
    ![](http://pmplttpn9.bkt.clouddn.com/picgo/5J5O{]IO__SM$@YOMTCAAGM.png)
    ![](http://pmplttpn9.bkt.clouddn.com/picgo/neko2.png)
- ```./alpainting.exe D:\video.mp4 -m video -o D:\video_al.avi -x 4 -y 4 -c 2 -b 0```  
    指定输入文件为```D:\video.mp4```,模式为```video```,输出到```D:\video_al.avi```,宽```4```个画板,高```4```个画板,原视频每```2```帧取一帧添加到输出视频,不使用边缘加粗