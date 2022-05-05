# 清單樣式
清單元素ul和ol也可以套用CSS，比較特殊屬性如下:  
1. 清單符號: list-style-type (none/disc/circle/square/upper-alpha/lower-roman...etc)
2. 清單圖片: list-style-image (url:("路徑"))
3. 清單符號位置: list-style-position (inside/outside)
首先載入清單樣式:  
```
<style>
        .list1 {
            list-style-type: circle;
            background-color: yellowgreen;
            list-style-position: inside;
            border: 5px dotted orange;
            /* border-radius: 20px 15px 10px 5px; */
            /* border-radius: 20px 0px 10px 0px; */
            border-top-left-radius: 55px 25px;
        }

        .list2 {
            list-style-type: none;
            list-style-image: url("Art/arrow.png");
            background-color: palegreen;
            text-decoration: line-through;
        }

        .in {
            color: blueviolet;
            background-color: black;
            list-style-position: inside;
        }

        .out {
            color: blueviolet;
            background-color: black;
            list-style-position: outside;
        }

        ul>li>ol>li#A {
            background-color: blueviolet;
        }
    </style>
```
接著套用到先前介紹的清單元素上:  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_img01.png)  
可以看到inside屬性值會把圖片放在li內；而outside則將圖片放在li外。  
