# 表單元素
表單使用form tag製作表單，所有的表單相關元素都必須寫在form tag底下。  
表單有3個重要的屬性:  
1. action: 伺服器等待接收資料的url
2. method: 傳送表單資料的方式，這個屬性值有兩種:  
  - get: 用網址傳送資料(危險性較高)  
  - post: 用封包傳出(安全性較高)
3. enctype: 資料傳送時的編碼設定(encoding)，裡面包含3種屬性值:  
  - application/x-www-form-urlencoded: 預設值
  - multipart/form-data: 表單有上傳檔案時需要使用
  - text/plain: 傳送純文字表單

# 常見子元素
表單內的常用元素如下:
1. **label:** label元素提供滑鼠user額外的功能，每當點擊label內的內容，滑鼠會觸發對應的控制元件。
```
<label for="account1" class="t1">Name:</label>
        <input type="text" name="account" id="account1" size="10" placeholder="guest" autofocus autocomplete="off">
```
上面的例子利用for指定id=account1的input tag，使用者以滑鼠點擊Name:文字時，便會自動選取這個input欄位!  
後面的placeholder代表無實際填入deault值(灰色)；autocomplete則代表網頁不會記憶先前的使用者資訊(安全性提升!)  
不需要給予對應值的屬性還有例如: disabled(直接讓該功能變灰色)、readonly(無法操作但是可被選取，JS的mouseover事件仍然可觸發)  

2. **input:** input元素提供鍵盤單列輸入的功能，常用屬性如下:  
  - type: text(單行文字輸入)、password(密碼輸入)、button(按鈕)、submit(送出表單資料的按鈕)、reset(清除表單資訊的按鈕)、radio(單選欄)、checkbox(多選欄)  
  - value: 預設呈現的文字  
  - size: 輸入列的寬度，決定其顯示多少字元寬度  
  - maxlength: 最多輸入幾個字元
須注意按鈕後續的觸發動作，需要由JavaScript接手完成。  
單選欄位語法如下:  
```
<label for="" class="t1">Gender:</label>
<label>
     <input type="radio" name="gender" id="" value="male">Male
</label>
<label>
      <input type="radio" name="gender" id="" value="female">Female
</label>
```
多選欄位語法如下:  
```
<label for="" class="t1">Hobby:</label>
<label>
    <input type="checkbox" name="hobby" id="" value="sport">Sport
</label>
<label>
    <input type="checkbox" name="hobby" id="" value="music">Music
</label>
<label>
    <input type="checkbox" name="hobby" id="" value="travel">Travel
</label>
<label>
     <input type="checkbox" name="hobby" id="" value="movie">Movie
</label>
```
單選和多選欄位的name值要設定成一樣!(代表同一欄內的選項)  
題外話，Emmet支援VScode內複雜的設置，這樣的結構當然也可以用簡寫快速完成:  
```
div.div01>label.t1+(input:checkbox)*3
```


3. **textarea:** 多行文字輸入，常用屬性如下:  
  - rows: 決定欄位高  
  - cols: 決定欄位寬
4. **select:** 下拉式選單，可以設定單選或複選，選項使用option元素呈現，常用屬性如下:  
  - multiple: 不須給屬性值，設定後該下拉式選單即為多選。
  - value: 此屬性值設定在option元素內，為每一個選項的背後設定值
  - selected: 不須給定屬性值，用來設定初始選取的目標。  
語法範例如下:  
```
<label for="" class="t1">Location:</label>
<label>
   <select name="add1" multiple size="2">
           <option value="A">Planet-A</option>
           <option value="B" selected>Planet-B</option>
           <option value="A">Planet-C</option>
           <option value="A">Planet-D</option>
           <option value="A">Planet-E</option>
   </select>
</label>
```



