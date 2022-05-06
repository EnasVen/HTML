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
