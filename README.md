# FrontEnd Practice


## Web 入門[ ( ref ) ](https://developer.mozilla.org/zh-TW/docs/Learn/Getting_started_with_the_web/CSS_basics)

### 與各式各樣檔案打交道[( ref )](https://developer.mozilla.org/zh-TW/docs/Learn/Getting_started_with_the_web/Dealing_with_files)

一個網站包含許多檔案：文字內容、程式碼、樣式表、多媒體內容等等。當建立網站時，你需要將這些檔案組合成清晰的架構，並確保它們能彼此互動溝通。

命名檔案或是資料夾時，只使用小寫並且避免使用空格，因為
- 許多的電腦尤其是網路伺服器，是大小寫區分的(case-sensitive)。
- 瀏覽器、伺服器、以及各種程式語言對於空格的處理並不是一致的。可能空白會變成%20

架構
HTML檔案與專門放圖片、樣式檔案、腳本檔案的資料夾們
1. index.html : 這個檔案會包含你的首頁內容
2. images : 所有網站會用到圖片的資料夾
3. styles : 這個資料夾包含了能夠設計你的網站的CSS碼(例如：設定文字與背景顏色)
4. scripts : 這個資料將包含能夠使網站具有互動性的JavaScript程式碼。(例如：按下按鈕後會載入資料)

### HTML 基本概念 [(ref)](https://developer.mozilla.org/zh-TW/docs/Learn/Getting_started_with_the_web#html_%E5%9F%BA%E6%9C%AC%E6%A6%82%E5%BF%B5)
超文字標籤語言 (Hypertext Markup Language；HTML) 是一種用來組織架構並呈現網頁內容的程式語言。網頁內容的組成，可能包含了段落、清單、圖片或表格...等。

HTML 元素的組成
![](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png)

元素還可以有「屬性（Attribute）」，可以利用屬性設定這個元素的色彩、對齊方式、圖表的格線等等。元素名稱和屬性之間有一個空格，屬性名稱後面接著等於符號「=」，屬性會包在起始標籤裡面，
![](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-attribute-small.png)
[HTML語法整理表](https://www.csie.ntu.edu.tw/~r91112/myDownload/WEB/html.html)

巢狀元素
```=HTML
<p>My cat is <strong>very</strong> grumpy.</p>
```
空元素 (有兩個屬性，但是沒有結束標籤，也沒有裡面的內容。)
```=HTML
<img src="images/firefox-icon.png" alt="My test image">
```
HTML 文件的架構
```=HTML
<!DOCTYPE html> 
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>
```
1. `<!DOCTYPE html>`文件類型（doctype）。 在 HTML 發展初期（約莫 1991/2 的年代）文件類型是用來連結一些應遵守的規則，有點像自動校正的功能。
2. `<html>` 元素，又被視為根元素（root element），包含了所有顯示在這個頁面上的內容。
3. `<head>` 元素，裡面放的是你想涵括的重要資訊，但不會顯示於網頁瀏覽者眼前的。例如，顯示於搜尋結果的關鍵字、頁面說明、CSS、字元實體集...等。
4. `<body>` 元素，包含了所有會顯示於網頁瀏覽者眼前的內容。 無論是文字、圖片、影面、互動遊戲...等。
5. `<meta charset="utf-8">` — 這個元素指定了你的文件使用utf-8這種字元編碼， 建議大家都要使用這個元素，它會幫助你免去許多文字無法正確呈現的煩惱。
6. `<title>` — 呈現於網頁瀏覽者眼前的網頁標題。

標記文字

- 文件標題 (heading) `<h1></h1> <h2></h2>`...
- 段落 (paragraph) `<p></p>`
- 清單 (list)
    - 無順序性清單（Unordered lists）`<ul></ul>`
    - 有順序性清單（Ordered lists）`<ol></ol>`

    ```
    <ul>
        <li>technologists</li>
        <li>thinkers</li>
        <li>builders</li>
    </ul>
    ```