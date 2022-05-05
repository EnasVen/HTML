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
