# 特殊字元
特殊字元用在顯示html code的場合，例如: 要在網頁上顯示html code源碼，他們的特點是&開頭，並以分號結尾:  
1. 版權符號 &copy; ```&copy;```
2. 空白 &nbsp; ```&nbsp;```
3. AND符號 &amp; ```&namp;```
4. 大於 &gt; ```&gt;```
5. 小於 &lt; ```&lt;```
6. 雙引號 &quot; ```&quot;```
7. 註冊商標 &reg; ```&reg;```
8. TM商標 &#8482; ```&#8482;```  

在VScode要把程式碼當作文字呈現，需要使用code元素，並且以figure元素呈現:  
```
<figure>
    <figcaption>特殊字元測試</figcaption>
    <code>
        &lt; label for="account1" class="t1">Name: &lt; /label &gt;
    </code>
</figure>
```

# 字型進階樣式
有時候我們會需要額外使用內建沒有的字型，這時候@符號可以提供類似import的功能:  
1. 字型檔案在local端:
```
<head>
    <style>
        @font-face {
            font-family: font1;
            src: url("範例/fonts/JustOldFashion.ttf");
        }
    </style>
</head>
```

2. 字型檔案在server端:
```
<head>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Water+Brush&display=swap');
    </style>
</head>
```

當然也可以使用link元素，以類似style sheet掛載css的方式載入(注意這段不是寫在style tag內):  
```
<head>
    <link href="https://fonts.googleapis.com/css2?family=Water+Brush&display=swap" rel="stylesheet">
</head>
```
這個link與import也可以直接由Google提供，無須手動輸入:  
搜尋Google Fonts => 隨便找一個想要的字型點進去 => 右手邊就有link或import的寫法，直接複製貼上就好!  
![Image](https://github.com/EnasVen/HTML/blob/main/HTML_img10.png)  
須注意link選其中一種寫法就行了，不用全部複製。  

圖片下方，Google也提供了CSS，因為前面只是載入字型，套用字型仍然需要透CSS指定!  
CSS的部分一樣直接複製貼上就完事了。  
```
h2 {
  font-family: 'Water Brush', cursive;
}
```

# 文字樣式
1. line-height: 段落的行距需要用line-height屬性設置，但這個值必須要大於字體高度(default字元高度為16px)
2. text-align: 文字水平對齊，屬性值有right、left以及center
3. vertical-align: 文字垂直對齊，在div中無效，只能作用於儲存格td，屬性值有bottom、top以及middle

# div文字垂直對齊
1. 直接將行高設定為div高度(只限無標籤文字或單列不超出div寬度的文字)
```
<style>
    .div01 {
        width:200px;
        height:100px;
        line-height:100px;
    }
</style>
```
2. 利用padding上下內縮，但要注意這2個值總和不能等於div高度(因為文字本身就有高度，要扣掉後再計算需要padding多少)  
```
<style>
    .div01 {
        width:200px;
        padding-top:50px;
        padding-bottom:50px;
    }
</style>
```
