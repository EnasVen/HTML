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
複合使用的語法如下:  
```

```

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

# 文字樣式
文字樣式使用下列屬性作修改(只列出部分):  
1. text-decoration
2. text-transform
3. color
4. 字型
5. 字型粗細
6. 字型類型
7. 字型大小
