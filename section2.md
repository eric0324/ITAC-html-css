# 初探HTML-撰寫第一個HTML

### 挑選編輯器
撰寫網頁時，為了寫出乾淨的程式碼，通常我們會避免使用各種現成拖拉元件的網頁編輯器(如 Dreamwave 、 VisualStudio 等)，取而代之使用文字編輯器來撰寫。

文字編輯器種類很多，常見的包含有：
* Windows 的記事本
* [Vim](http://www.vim.org) & [Vi](http://thomer.com/vi/vi.html)
* [Sublime Text 3](http://www.sublimetext.com/3)
* [Atom](https://atom.io)
* [Brackets](http://brackets.io)

目前社團成員大部分是使用 Sublime Text  3 和 Atom 為主。下面簡單介紹這兩款編輯器的 plugin 安裝方法。

#### Sublime Text 3

  ![sublime download][1]
  依照自己的作業系統選擇對應的版本下載，
  Windows user 推薦下載 portable 的，這樣把套件裝完之後，把整個資料夾放在隨身碟就可以帶著走。

  ![sublime main][2]
  打開 Sublime 後可以看到這樣的畫面

  首先我們要先安裝 [Package control](https://packagecontrol.io) ，在sublime的主畫面按下<kbd>ctrl</kbd> + <kbd>`</kbd>開啟console

  ![sublime console][3]

  在 console 貼上 Package Control 的安裝指令（你可以在[這裡](https://packagecontrol.io/installation#st3)找到)，按下<kbd>Enter</kbd>就會開始安裝了。安裝完畢後請把Sulime重新打開。

  按下<kbd>cmd</kbd> + <kbd>shift</kbd> + <kbd>P</kbd>（MAC) 或 <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>P</kbd> 打開 Sublime 的 Command Palette。輸入`Package Control: Install Package`，接著輸入 plugin 名稱在按下 <kbd>Enter</kbd> 就可以安裝 Plugin 囉。

  Plugin 可以參考[前一篇](section1.md)推薦的必裝清單

### Atom

Atom在進入官網後就可以看到一個大大的 Download ，直些下載下來安裝即可。

Atom的操作相對 Sublime 親和許多，按下<kbd>cmd</kbd> + <kbd>,</kbd> 可以打開設定頁面，點一下`Install`，在搜尋框輸入 Package 名稱進行搜尋，對搜尋結果點一下 `Install` 就可以安裝囉。

同樣的必裝 Plugin 可以參考[前一篇](section1.md)推薦的必裝清單。

特別注意建議不要安裝 Facebook 推出的 nuclide 系列套件，目前該套件還不穩，容易使 Atom crash

### 撰寫第一個HTML網頁

還記得在前一篇提到網頁的基本架構嗎？
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>網頁標題</title>
  </head>
  <body>

  </body>
</html>
```
在文字編輯器開一個新的檔案，將上述程式碼貼上，副檔名記得儲存為 `.html` 喔。

![web][4]
打開它後你會發現一片空白，除了視窗上的標題。

首先我們可以修改標題，將 `<title>網頁標題</title>`  改成你自己想要的標題，例如 `<title>Hi World~</title>`。

試著加一點東西吧，例如插入圖片`<img />`、增加清單`<ul></ul>`。

![web][5]

詳細的各種Tag說明你可以參考：
* [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
* [W3SCHOOL](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

### 裝飾你的網頁

網頁看起來有點單調怎麼辦？通常網頁設計師會幫網頁套上樣式表 (CSS) ，藉由設定樣式表來美化網頁。

但我們還不會寫 CSS 呀，該怎麼辦呢？別擔心，網路上很多大神都幫我們寫好了一些簡單的套件讓我們快速使用。像是 [bootstrap](http://getbootstrap.com) ，以下簡單介紹他的使用方法吧。

打開官網後點一下 **Getting started** ，往下捲可以看到 Bootstrap CDN

![bootstrap][6]

將程式碼copy下來貼到 網頁中的`<head></head>`當中吧
```
<!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

<!-- Optional theme -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">

<!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
```
bootstrap裡面有非常多現成的樣式可以使用，點一下官網的 CSS 就可以看到有很多能夠使用的樣式

例如，把圖片修為圓形：

這是原本的圖片HTML程式
```
<img src="路徑" alt="" />
```

加入 `class="img-circle"`後變成
```
<img src="路徑" alt="" class="img-circle" />
```

圖片就變成圓角了
![bootstrap-image][7]

bootstrap裡面還有非常多能夠使用的樣式喔，請大家練習使用看看。

###範例程式碼

所有的範例程式碼可以在[這裡](https://github.com/eric0324/ITAC_html_css/tree/master/example/section2/)找到

[1]: https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/sublime_download.png
[2]: https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/sublime_main.png
[3]: https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/sublime_console.png
[4]:https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/web1.png
[5]:https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/web2.png
[6]:https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/bootstrap1.png
[7]:https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/bootstrap2.png
