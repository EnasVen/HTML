# 超連結selector
針對hyperlink元素，常用以下4種selector:  
1. a:link 定義預設樣式
2. a:visited 定義瀏覽過的樣式
3. a:hover 定義滑鼠移過的樣式
4. a:active 定義滑鼠左鍵按住不放的樣式

以下為超連結selector+清單樣式CSS應用:  
```
<style>
        .list>li>a:link {
            text-decoration: none;
            color: aqua;
        }

        .list>li>a:visited {
            color: crimson
        }

        .list>li>a:hover {
            background-color: black;
            color: white;
            font-size: x-large;
        }

        /* .list a:active { */
        .list>li>a:active {
            color: blueviolet;
            text-decoration: underline;

        }
    </style>
```
下圖為套用CSS的執行結果:  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_img02.png)  
可以看到滑鼠hover造成的放大效果以及已造訪的紅色字體超連結。  
