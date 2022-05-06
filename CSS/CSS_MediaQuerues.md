# MediaQueries 
這個屬性能讓會根據使用者的媒體裝置、特性來選擇不同的樣式。  
例如: 瀏覽器寬度、裝置(PC、手機App...etc)、列印...等等。  

原先的h1 selector為正常的CSS，而@media後面接的條件需要以小括號呈現，並用逗點分隔。  
範例的樣式就是當瀏覽器寬度限縮到500px的時候，原先的h1改以另一種CSS呈現!  

MediaFeatures相關的屬性值如下:  
1. width,height: 螢幕寬度與高度，可加上max或min來做變更
2. orientation: 螢幕旋轉方向，屬性值可使用portrait(直向)或者landscape(橫向)
3. ascpect-ratio: 螢幕長寬比，屬性值設定如: 1/1 1920/1080
4. color: 輸出螢幕的色彩位元數，屬性值若為0則代表黑白裝置
5. resolution: 螢幕解析度

MediaTypes相關的屬性值如下:  
1. all: 所有裝置
2. screen: 螢幕裝置
3. print: 印刷裝置，包含預覽列印畫面
4. speech: 偵測可讀出html的設備

使用方法為 MediaFeatures MediaTypes呈現，中間使用逗點代表or，使用and代表且，語法範例如下:  
```
<head>
    <style>
        h1 {color: white;}
        @media (max-width:500px),print {
            h1 {font-size: 100px;color:red;}
        }
    </style>
</head>
```
