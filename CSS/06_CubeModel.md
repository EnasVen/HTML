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
