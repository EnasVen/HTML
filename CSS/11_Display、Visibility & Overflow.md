# display樣式
設定元素是否顯示，其屬性值如下: 
1. none: 不顯示元素，同時此元素不佔用任何html空間
2. block: 顯示，並將元素視為block存在
3. inline: 顯示，並將元素視為inline存在
4. list-block: (略)

# visibility樣式
設定元素是否可見，其屬性值如下:
1. visible: 顯示
2. hidden: 隱藏，但仍會佔用html空間
3. collapse: 用於表格
4. inherit: 若父元素為可見，則此元素為可見

# overflow樣式
設定容器元素的顯示方法，其屬性值如下:
1. auto: 自動設定，可出現捲軸(if needed)
2. scroll: 強迫出現捲軸，並使內部元素不超過border
3. hidden: 超出border的字強行截斷
4. visible: 全部顯示，無視區塊大小

我們以下面的範例說明這三種樣式，首先在body區建立nav導覽列以及h1標籤:  
```
<nav>
    <ul class="list">
        <li><a href="https://www.iSpan.com.tw">資展國際</a></li>
        <li><a href="https://www.yahoo.com.tw">雅虎奇摩</a></li>
        <li><a href="https://www.google.com">谷歌首頁</a></li>
    </ul>
</nav>
<h1>Test h1</h1>
<h2>Test h2</h2>
<div class="d1">測試測試測測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試試測試測試測測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試測試試</div>
```

接著在head內的style元素內建立以下CSS:  
```
.d1 {
    width: 250px;
    height: 50px;
    border: 1px solid red;
    /* overflow: auto; */
    overflow: hidden;
}

.list {
    list-style: none;
}

.list>li>a {
    display: block;
    text-align: center;
    border: 1px solid black;
    line-height: 2.5em;
}

.list>li>a:hover {
    text-decoration: none;
    background-color: blue;
    color: white;
}

h1 {
    /* visibility: hidden; */
    visibility: visible;
}
h2 {
    display: block;
}
.list {
    background-color: cornflowerblue;
    overflow: auto;
}
.list li {
    width:7em;
    float: left;
}
```
顯示與隱藏的部分比較簡單，交互註解一下就能看出差異，比較複雜的是導覽列的部分。  
原先的導覽列因為清單元素的緣故，呈現垂直展開。  
我們想要將這個導覽列變成水平展開，因此將各li元素指定寬度後給予float。  
這時，原先的h1標題跑到第一列了!  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_Img12.png)  
發生的原因在於li元素為block，經過float+width後，寬度限縮了。  
因此後方的空間就會由下一個元素補上，而h1為block元素，因此後面一整個空白都是h1的範圍。  
所以我們需要透過display樣式，將超連結元素a設定為block，並透過overflow將超出的部分自動調整。  
line-height樣式則是將整個文字做垂直置中!(設定行高=block高度)  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_Img13.png)  


