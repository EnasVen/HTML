# 多欄版型
CSS可透過以下屬性變更段落樣式:  
1. column-count: 指定要幾段
2. column-width: 指定欄位寬度
3. column-gap: 指定欄位留白
4. column-rule: 指定分隔線

實際操作範例如下:  
```
<head>
    <style>
        .box1 {
            column-count: 2;
            column-width: 20%;
            column-gap: 2em;
            column-rule: 5px dashed yellowgreen;
            width: 1000px;
        }
    </style>
</head>
```
上述語法執行後如下:  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_Img11.png)  

# 背景設定
CSS可透過以下屬性變更背景樣式:  
1. background-image: 指定背景圖片
  - 屬性值: none、url
```
body {
  background-image: url(./Art/pic01.png);
}
```
2. background-repeat: 指定重複與否，可設定不同方位重複(例如:x方向、y方向)
  - 屬性值: repeat-x、repeat-y、repeat、no-repeat
3. background-attachment: 指定是否附著，避免因滑鼠滾輪滾動造成背景移動
  - 屬性值: scroll、fixed
4. background-position: 指定背景位置，須給2個屬性值，如果只給一個，另一個屬性值必定為center
  - 屬性值: top、bottom、center、left、right
```
h1 {
  background-position: right bottom;
}
```
5. background-size: 指定背景圖片大小
  - 屬性值: px、%、em...etc
