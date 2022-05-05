# 標籤語法
HTML使用標籤(Tag)作為基礎元素，大部分都是成對(<tag>...</tag>)  
部分標籤為單一存在(例如:br hr img...etc)  

# 屬性與屬性值
元素內可以用屬性來標示或賦予該元素特定功能。(例如:```<h2 title='AAA'>xxx</h2>```)  
元素屬性之間需要以**半形空格**來區分。(例如:```<h1 title='A' color='red'>xxx</h1>```)  

# 網頁框架 
HTML的架構如下:  
首先是開頭宣告，用來告知瀏覽器我們使用的版本是HTML5(快捷鍵 !+TAB):  
```
<!DOCTYPE html> 
```
接著在html主體內，又分為head區以及body區:  
```
<html>
    <head>
    ...
    </head>
    <body>
    ...
    </body>
</html>
```
head區用來標示網頁相關資訊；body區則是網頁內容主體。  

# html根元素
```<html>```為網頁根元素，終點為```</html>```，可使用lang屬性設定網頁文件使用的語言! ```例如: <html lang="zh-Hant-TW">```  

# head元素
head內包含以下子元素:  
1. title : 網頁王建標題，也就是瀏覽器該視窗的名稱，這個元素在head內只能唯一存在，書籤存取所抓的名稱即為此!  
2. meta : 描述HTML文件資訊，並且由name與content屬性來決定。
3. style : 樣式宣告區，調整各元素的呈現風格。  
4. script : 程式碼宣告，JavaScript程式碼用。  

meta的name屬性值常用如下:  
```
<meta charset="UTF-8">
<title>Course01</title>
<meta name="author" content="peterwang">
<meta name="date" content="2022/05/03">
<meta name="description" content="測試">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta http-equiv="Refresh" content="3;url=https://tw.yahoo.com">
<meta http-equiv="content-type" content="text/html;charset=UTF-8">
```
須注意有name attr就必須有content attr，缺一不可!  
比較特殊的事項如下:  
1. keyword為關鍵字，用於網頁搜尋提供的預設資訊。  
2. date不能使用dash分隔只能用斜線。
3. generator代表開發工具。
4. http-equiv代表瀏覽器初始執行的動作，Refresh為重新整理，上例content=3代表3秒後重整一次網頁，後面url代表重整後的導向網站。(不給url就是原網頁重新整理)  
5. http-equiv="content-type"則是指定網頁編碼須為UTF-8

# body元素
網頁主要內容都寫在這區，例如段落文字、超連結、圖片影片、表格表單...etc  
