# CSS
CSS為Cascading Style Sheet的縮寫，用來修改HTML元素樣式。  

# 基本語法
CSS基本語法為:  
```
selector {attr:value ; attr:value ; ... ; }
```
屬性間隔必須以分號;區隔，最後一組屬性可以不加分號結尾。  
屬性與屬性值之間必須以冒號:區隔。  
selector為一種選取器，用來搜索指定的HTML tag。  
常用的selector為:  
1. 標籤(使用tag元素名稱)
```
h1 {...}
```
2. 類別(使用class name)
```
.div {...}
```
3. 物件(使用id name)
```
#a {}
```
複合使用的語法範例如下:  
```
h1,h2 {...}
div.CLASSNAME {...}
ul>li>ol>li#A {...}
.list a:active {...}
.list>li>a:visited {...}
```
須注意>路徑要完整寫出，因為系統是一層一層往下找!  

# CSS基礎設定
修改長度或大小等數值時，必須指定單位。  
常用單位: 1em=100%=12pt=16px  

# CSS顏色設定
常用有3種方法:  
1. 名稱指定
```
background-color:black
```
2. Hex code
```
color: #00FF80
```
3. Decimal
```
color: **rgb(192,80,150)**
```
須注意使用第三種方法，rgb()不可省略!  
另外標籤的類別屬性內可以有多個class，例如:  
```
<h1 class="t1 t2 b-h">
```

# 文字樣式
文字樣式使用下列屬性作修改(只列出部分):  
1. text-decoration: none/underline/overline/line-through...
2. text-transform: none/capitalize/uppercase/lowercase...
3. color: red/green...
4. font-family: 標楷體/新細明體...
5. font-weight: 100~900/normal(400)/bold(700)/bolder/lighter...  
6. font-style: normal/italic/oblique...
7. font-size: 絕對大小(xx-small、medium、x-large、larger...)/相對大小(larger、smaller)/長度值(in、cm、pt、em...)/比例值(em、%)  

# 樣式套用
套用CSS的方法有3種:  
1. Inline(直接寫在tag內)
2. Embedding(寫在head內的style元素內)
3. Linking(寫在head內的link元素內，利用.css檔案載入)
```
<head>
<link rel="stylesheet" href="路徑&檔名">
<\head>
```
# 執行順序
CSS執行順序由上而下，先定義的會被後定義的覆蓋!!  
寫在head內的style區內的CSS，會被body區的CSS覆蓋。(if CSS reference到同一個指標，例如:id、tag...etc)
實務使用上，靜態CSS使用標籤元素的class屬性來抓取；而動態CSS則使用id屬性，理由是JavaScript指令抓id只能1對1，因此HTML文件內的id屬性最好不要重複。  

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

# 邊框樣式
border屬性提供設定多元素邊框的功能，以下列出2種簡介:  
1. border: border-width border-style border-color (寬度 樣式 顏色)，用來一次指定3種邊界樣式  
        - width為數值，套用先前講的單位設定。  
        - style為線條樣式，可使用dashed、solid、groove、outset、double...etc  
        - color為線條顏色<套用先前講的顏色設定。  
其語法範例如下:  
```
.h1 {
     border: 5px solid red
     }
```
2. border-radius: 指定元素邊角的呈現方式
        - border系列提供各方位的設定，例如:border-top-left-radius、border-bottom-right-radius...etc  
        - 可單一指定數值，也可以給4個數值，其順序為左上-右上-右下-左下  

# 方塊模型
CSS內的padding、margin屬性相當重要，圖解如下:  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_img03.png)  
padding表示元素和border的距離。  
margin表示元素和browser的預設距離+設定距離。(例如:設定margin:20px，內建1px => 整體就會是21px)  
由於預設距離無法透過設定消除，因此CSS提供一個初始化的方法，在載入HTML文件時優先觸發:  
```
* {
     margin:0;
     padding:0;
}
```
這個設置可以消除所有元素的內建距離，例如:標題元素h1 tag起始位置有預留空白...etc  

padding和margin的屬性值可以給1個數值，也能給4個數值，給4個數值就會有上下左右之分，由左至右依序為上-右-下-左  
```
#a1 {
     padding: 5px 10px 15px 20px;   
}
```
既然有方向之分，這兩個元素也像border-radius一樣有 -top / -right / -bottom / -left 的分支做單一設定。  

