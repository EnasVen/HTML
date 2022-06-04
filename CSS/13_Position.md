# position屬性
position用來定義元素在網頁的位置，有4種屬性值:  
1. absolute: 絕對位置，表示與父元素的距離
2. relative: 相對位置，不指定距離屬性的話與static相同
3. static: 靜態位置，依照html code順序來定位
4. fixed: 固定位置，捲動卷軸時不會移動
包覆其他元素的標籤稱為父元素，被包含的則稱子元素!  

# 位移屬性
指定position類型後，可透過以下屬性來變更位置:  
1. bottom 
2. top
3. left
4. right
這四種屬性代表與前一個元素border的距離，可套用數值單位做縮放，也可以用auto讓瀏覽器自行調整。  
須注意當父元素的position為relative時，如果子元素position設定為absolute，則位移屬性會根據屬性值在父元素內移動!(不會跑出父元素外面)  
反之，當父元素不是relative，那麼子元素的位移屬性會參照瀏覽器邊界做移動!!  

以下為CSS語法範例:  
```
.static1 {
    position:static;
    border:3px solid purple;  
}
       			
.relative1 {
    position:relative;
    border:3px solid green;
}
       			
.relative2 {
    position:relative;
    border:3px solid red;
    top: 20px;/*-30*/
    left: 670px;
    background-color: #dfa5a5;
    width: 500px;
}
				
.fixed1	{
    position:fixed;
    width:200px;				
    border:3px solid #9999CC;
    bottom:50px;
    right:100px;
}
			
.relative3 {
    /* position: relative;  */
    position:static;
    width: 600px;
    height: 400px;
    border:3px solid #0080FF;
}
				
.absolute1 {
    position: absolute;
    top: 220px;
    right: 0;
    width: 300px;
    height: 150px;
    border:3px solid #FF8040;
}	
.parent {
    width: 500px;
    height: 400px;
    position: static;
    border: 1px solid purple;
}  

```
body區塊設定如下:  
```
<div class="static1">static</div>
<div class="relative1">relative1</div>
<div class="relative2">relative2</div>
<div class="fixed1">fix</div>
<div class="parent"> parent
  <div class="absolute1">
     absolute
  </div>
</div>
```
執行結果如下圖:  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_Img16.png)
