# HTML
網頁上的文字、表單、圖片都是透過HTML tag組成。  
每一個HTML都會有預設樣式。  
在HTML內，元素(tag)的語法為:  
```
<tag attr='value" attr='value'> 內容文字 </tag>
```
不同屬性以空白間隔!  

HTML將元素(tag)區分為:  
1. block元素
2. inline元素

block元素內能放block & inline元素；但**inline元素內只能放inline元素。**  

# HTML - 標題元素
從h1~h6(沒有h7)，標題元素為預設粗體且字型較大，最大為1；最小為6。  
標題元素用於製作文章/段落/區塊的標題。  
例如:  
```<h1> Title </h1>```  
```<h2> Title </h2>```  
```<h3> Title </h3>```  
```<h4> Title </h4>```  
```<h5> Title </h5>```  
```<h6> Title </h6>```  
<h1> Title </h1>
<h2> Title </h2>
<h3> Title </h3>
<h4> Title </h4>
<h5> Title </h5>
<h6> Title </h6>
這邊也能看出markdown在h2之後就沒有預設分隔線了!  

# HTML - 段落元素
段落元素包含div、span與p  
div與p為block元素，而span則為inline元素。  
兩者差異如下:  
```
aaa
<div> XXX </div>
bbb
```
aaa
<div> XXX </div>
bbb

可以看到div預設是換行的，因為它佔了一整列。  
而span則會將前後文字整在同一列上:  
```
aaa
<span> XXX </span>
bbb
```
aaa
<span> XXX </span>
bbb

p用來表示一個段落，常用於文章存放。  
例如:
```
<p>
〔記者林惠琴／台北報導〕過去外界可能認為腺病毒載體的AZ疫苗，效力不如mRNA的莫德納、輝瑞／BNT疫苗，但一份最新專家審查79項真實世界數據的發現，AZ疫苗與mRNA疫苗施打兩劑後，於預防住院及死亡具有相同的保護力。
</p>
```
<p>
〔記者林惠琴／台北報導〕過去外界可能認為腺病毒載體的AZ疫苗，效力不如mRNA的莫德納、輝瑞／BNT疫苗，但一份最新專家審查79項真實世界數據的發現，AZ疫苗與mRNA疫苗施打兩劑後，於預防住院及死亡具有相同的保護力。
</p>

# HTML - 清單元素
清單元素包含以下三種:  
1. 項目清單(ul)
2. 序號清單(ol)
3. 定義清單(dl)
注意li並不是清單元素，它只是附屬品!  

項目清單內的子項目不具備順序性，屬於一般性條列。  
其語法如下:  
```
<ul>
  <li>A</li>
  <li>B</li>
</ul>
```
在VSCode可使用Emmet做快速輸入:  
```
ul>li*2
```


序號清單內的子項目則有順序性，常用於排名的條列。  
其語法如下:  
```
<ol>
  <li>A</li>
  <li>B</li>
</ol>
```
在VSCode可使用Emmet做快速輸入:  
```
ol>li*2
```

定義清單內除了子項目元素，多了一個清單項目說明元素，用於解釋清單項目。  
其語法如下:  
```
<dl>
  <dt>A</dt>
  <dd>B</dd>
  <dd>C</dd>
  <dt>A</dt>
  <dd>B</dd>
  <dd>C</dd>
</dl>
```
在VSCode可使用Emmet做快速輸入:  
```
dl>(dt+dd*2)*2
```
每一個dt必須搭配至少一個dd元素。  
每個dl dd dt都是block元素!  

如果要在清單內新增清單，則必須在li或dd內做新增!  
巢狀多層清單語法如下:  
```
ol>(li>(ul>li*2)*3)*2   ol底下創建2個li，每一個li底下包含3個ul，這3個ul每一個包含2個li
```

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
# HTML - 圖片元素
圖片元素使用img作為tag名稱，網頁內加入圖片的語法如下:
```
<img src="你的路徑" alt="沒顯示圖片時的替代文字" title="滑鼠移到上面時顯示的文字" height="自訂高度" width="自訂高度">
```

當然，圖片可以與超連結的方結合:  
```
<a href="path"> <img src="path"> </a>
```

# HTML - Figure元素
figure元素用於定義網頁結構，其於網頁上顯示的初始位置與一般元素不同。  
figcaption元素為figure元素的標題，必須寫在figure元素內，且一個figure元素內只能放一個figcaption!  

# HTML - 表格元素
table標籤可製作表格，裡面包含以下相關元素:  
1. tr:宣告一個row
2. th:存放標題的儲存格
3. td:存放資料的儲存格
4. caption:表格標題
5. thead、tbody與tfoot用來群組化儲存格，方便辨識與管理。

須注意rowspan與colspan屬性需要放在td內。指定該儲存格往後多少格需要以row/col方式合併。  
另外，caption標籤需要放在table內的首位。  
語法範例如下:  
```
<table class="tb1">
        <caption>
            <h2>表格練習</h2>
        </caption>
        <thead>
            <tr>
                <th>Col1</th>
                <th>Col2</th>
                <th>Col3</th>
                <th>Col4</th>
            </tr>
            <tr>
                <th colspan="2">Col1+Col2</th>
                <!-- <th>Col2</th> -->
                <th colspan="2">Col3+Col4</th>
                <!-- <th>Col4</th> -->
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="tb2">1</td>
                <td class="tb2">2</td>
                <td class="tb2" rowspan="2">3</td>
                <td class="tb2">4</td>
            </tr>
            <tr>
                <td class="tb2">1</td>
                <td class="tb2">2</td>
                <!-- <td class="tb2">3</td> -->
                <td class="tb2">4</td>
            </tr>
            <tr>
                <td class="tb2">1</td>
                <td class="tb2">2</td>
                <td class="tb2">3</td>
                <td class="tb2">4</td>
            </tr>
            <tr>
                <td class="tb2">1</td>
                <td class="tb2">2</td>
                <td class="tb2">3</td>
                <td class="tb2">4</td>
            </tr>
            <tr>
                <td class="tb2">1</td>
                <td class="tb2">2</td>
                <td class="tb2">3</td>
                <td class="tb2">4</td>
            </tr>
        </tbody>


    </table>
```


# 其他功能
HTML註解 : ```<!-- XXX -->``` HoyKey: Ctrl+/  
CSS註解 : ```/* XXX */```
