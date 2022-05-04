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
