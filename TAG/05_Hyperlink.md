# HTML - 超連結元素
超連結元素tag代號為a，必須搭配href屬性指定路徑。  
語法如下:  
```
<a href="https://www.yahoo.com.tw/"> XXX </a>
```
超連結可以在同一page內作連動，但必須預先在該tag設置id，例如跳到網頁的某一個段落，在連結網址後面加上#並打上該id名稱。  
以下分別為指定路徑是否與.html檔案同層(資料夾):  
```
<a href="../hyperlink3.html#bookmark1">跳到另一頁的特定段落1</a>  該網站在.html檔的上一層
<a href="./hyperlink3.html#bookmark1">跳到另一頁的特定段落1</a>  該網站與.html檔同層
<a href="./Art/hyperlink3.html#bookmark1">跳到另一頁的特定段落1</a>  該網站在.html檔的下一層
```

超連結也可以使用email位置，與法如下:  
```
<a href="prophet0630@outlook.com"> mail_2_ME </a>
```
