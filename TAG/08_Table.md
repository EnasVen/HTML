# HTML - 表格元素
table標籤可製作表格，裡面包含以下相關元素:  
1. tr:宣告一個row
2. th:存放標題的儲存格
3. td:存放資料的儲存格
4. caption:表格標題
5. thead、tbody與tfoot用來群組化儲存格，方便辨識與管理。(不可相互嵌入，必須互相分隔開!)

須注意rowspan與colspan屬性需要放在td內。指定該儲存格往後多少格需要以row/col方式合併。  
caption標籤需要放在table內的首位。  

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
上述語法執行後的結果如下:  
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
