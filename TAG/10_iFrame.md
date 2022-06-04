# 內置框架元素
iframe tag可以將其他website嵌入html page內，常用屬性如以下:  
1. src: 連結位置
2. scrolling:捲動，可設置為yes/no/auto
3. frameborder: 框線，可設置為0(隱藏)/1(顯示)
須注意並非所有網站都能嵌入，portal類型無法使用，例如:Google首頁。  


網站、地圖與影片的鑲嵌語法如下:  
```
<iframe src="https://www.pchome.com.tw" frameborder="0"></iframe>

<iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d11476.972758792164!2d121.54377484946242!3d25.033405751818826!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3442abd0b034e669%3A0x4cb66e4f3456a06!2z6byO5rOw6LGQIOW-qeiIiOW6lw!5e0!3m2!1szh-TW!2stw!4v1651653286137!5m2!1szh-TW!2stw"
        width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"></iframe>
        
<iframe width="1280" height="720" src="https://www.youtube.com/embed/RcMUacBSuXs" title="YouTube video player"
        frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen></iframe>
```

Googla Map的iframe不需要手動輸入，可以透過Google Map提供:  
在搜尋指定地標後，點擊分享 => 嵌入地圖即可看到 iframe語法，複製後直接貼上就行了!  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_img04.png)  

而YT影片直接在屏幕滑鼠右鍵 => 複製嵌入碼，即可在VScode直接貼上!  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_img06.png)  
