# 結構語意元素
HTML5新增了一些網頁結構元素，簡潔地讓使用者能有效定義版型。  
這些元素分別為:  
1. section
2. nav
3. header
4. article
5. aside
6. footer
7. figure
8. address

如下圖:  
![iImage](https://github.com/EnasVen/HTML/blob/main/HTML_img07.png)  

這些tag名稱不同，具備的意義也不同。  
而設定結構元素能讓全部使用HTML5的人有統一的版型定義，例如: 標題區就該用header/hgroup/nav tag，而不是使用一堆div，容易造成讓看程式碼的人識別錯誤。  

# 新屬性值
input元素多了一些新功能:  
1. **日期選擇器:** 提供不同時間樣式的選擇
```
<p>
    <label class="t1" for="">date:</label>
    <input type="date" name="date1">
</p>
<p>
    <label for="" class="t1">datetime:</label>
    <input type="datetime-local" name="dt1">
</p>
<p>
    <label for="" class="t1">month:</label>
    <input type="month" name="month1">
</p>
<p>
    <label for="" class="t1">time:</label>
    <input type="time" name="time1">
</p>
<p>
    <label for="" class="t1">week:</label>
    <input type="week" name="week1">
 </p>
```
2. **文字方塊類型:** email、url都會做簡易的檢查，但細部檢查還是需要JavaScript來做!
```
<p>
    <label class="t1">URL:</label>
    <input type="url" name="url1">
</p>
<p>
    <label class="t1">Search:</label>
    <input type="search" name="sch1">
</p>
```
3. **一般類型:** color、range以及number的顯示，color直接能選取顏色；而range提供拉bar的功能(但是default沒有顯示數值，要顯示數值需搭配JS!)  

4. **表單屬性類型:** 範圍驗證屬性(min/max/step) 與 一般驗證屬性(required/maxlength/pattern)
此功能搭配range與number可以透過JS完成簡易的網頁互動:  
```
<div>
    Number:<input type="number" id="numberInput" min="-60" max="60" step="2" onchange="numberChange()" value="17" />
    <input id="numberText" />
</div>
<div>
    Range:<input type="range" id="rangeInput" min="-40" max="40" step="2" onchange="rangeChange()" />
    <input id="rangeText" />
</div>
<script>
    // JS寫在這裡
    function numberChange() {
        var n = document.getElementById('numberInput').value;
        document.getElementById('numberText').value = n;
    }
    function rangeChange() {
        var n = document.getElementById('rangeInput').value;
        document.getElementById('rangeText').value = n;
    }
</script>
```
實際demo會產生如下的畫面:  
![iImage](https://github.com/EnasVen/HTML/blob/main/HTML_img08.png)  

5. **特殊屬性:** placeholder、autofocus、autocomplete、datalist、readonly、size、multiple
  - autofocus: 無須給予屬性值，在標籤內加註即可，代表滑鼠初始位置要停在哪一個選項。
  - size: 設定select清單內要顯示多少個option

須注意datalist為input元素的候選項目，不能放在input元素前面，也不能單獨存在。  
語法範例如下:  
```
<label for="" class="t1">PreferWebpage:</label>
<input type="url" name="web1" list="hpurls">
<datalist id="hpurls">
    <option value="https://www.google.com.tw">谷哥</option>
    <option value="https://www.facebook.com.tw">臉書</option>
    <option value="https://www.yahoo.com.tw">雅虎</option>
</datalist>
```
實際demo會產生如下的畫面:  
![iImage](https://github.com/EnasVen/HTML/blob/main/HTML_img09.png)  
