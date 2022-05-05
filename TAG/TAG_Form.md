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

2. **input:** input元素提供鍵盤單列輸入的功能，常用屬性如下:  
  - type: text(單行文字輸入)、password(密碼輸入)、button(按鈕)、submit(送出表單資料)、reset(清除表單資訊)  
  - value: 預設呈現的文字  
  - size: 輸入列的寬度，決定其顯示多少字元寬度  
  - maxlength: 最多輸入幾個字元
須注意按鈕後續的觸發動作，需要由JavaScript接手完成。  

3. **textarea:** 多行文字輸入，常用屬性如下:  
  - rows: 決定欄位高  
  - cols: 決定欄位寬
4. 



