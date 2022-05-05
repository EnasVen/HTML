# float與clear樣式
float可將元素設置成浮動樣式，形成文繞圖的效果。  
HTML的元素預設都是無浮動。  
須注意當元素被設定成float時，必須要給寬度，且後方元素也會連動被float到同一row上。  
```
.t1 {
   float:right     
}
```

clear可以把被float的元素解除float狀態。屬性值可選none、left、right或both  
```
p {
   clear:both     
}
```
