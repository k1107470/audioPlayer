h5 audio 播放器
==============

## 使用  
* 代码
    
        <!DOCTYPE html>
        <html lang="en">
        
        <head>
            <meta charset="UTF-8">
            <title>..</title>
            <!-- 播放器样式 -->
            <link rel="stylesheet"  href="./player.css">
        </head>
        
        <body>
            <audio id="myAudio" preload="auto" src="">
                你的浏览器不支持html5播放器
            </audio>
            <div id='playerContainer' ></div>
        </body>
        <!-- 播放器对象 -->
        <script src="./player.js"></script>
        <script type="text/javascript">
        //实例化播放器对象
            var player = new Player({
                container: 'playerContainer',//容器的id
                audio: 'myAudio'//audio的id
            })
        </script>
        
        </html>   

*  方法
    
        内置播放器列表对象数组，传入的对象形式举例{
            'id': 0,
            'songId': ,
            'name': "你就不要想起我 (Live) (原唱：田馥甄)",
            'src': "http://ws.stream.qqmusic.qq.com/201040845.m4a?fromtag=46"
            } 
        常用方法属性：播放列表 this.list //有缓存功能
                    播放/暂停 playAndPause() 
                    上一首/下一首 playPrev(),playNext();
                    同步更新时间 updateTime()
                    储存缓存 save();
        其他功能具体查看js中Player.prototype中方法                      


