# 文字陰影
text-shadow屬性可以讓文字有立體效果，必須要給定4個屬性值:  
1. h-shadow: 左右陰影偏移程度(可以為負數，代表反方向)
2. v-shadow: 上下陰影偏移的程度(可以為負數，代表反方向)
3. blur: 陰影模糊程度，數值呈現，越小代表越清晰
4. color: 陰影顏色

# 區塊陰影
相比於text-shadow，box-shadow屬性則提供區塊陰影的效果，同樣也需給予4個屬性值:
1. h-shadow: 左右陰影偏移程度(可以為負數，代表反方向)
2. v-shadow: 上下陰影偏移的程度(可以為負數，代表反方向)
3. blur: 陰影模糊程度，數值呈現，越小代表越清晰
4. color: 陰影顏色

語法範例如下:  
```
h1 {
    text-shadow: -100px 5px 3px peru;
}

.div01 {
    box-shadow: 20px 5px 3px peru;
}
```
上述語法執行後結果如下:  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_Img14.png)  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_Img15.png)
