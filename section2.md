# 初探HTML-撰寫第一個HTML

### 挑選編輯器
撰寫網頁時，為了寫出乾淨的程式碼，通常我們會避免使用各種現成拖拉元件的網頁編輯器(如 Dreamwave 、 VisualStudio 等)，取而代之使用文字編輯器來撰寫。

文字編輯器種類很多，常見的包含有：
* Windows 的記事本
* Vim & Vi
* [Sublime Text 3](http://www.sublimetext.com/3)
* [Atom](https://atom.io)
* [Brackets](http://brackets.io)

目前社團成員大部分是使用 Sublime Text  3 和 Atom 為主，。下面簡單介紹這兩款編輯器的 plugin 安裝方法。

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
Atom在進入官網後就可以看到一個大大的Download，直些下載下來安裝即可。

Atom的操作相對 Sublime 親和許多，按下<kbd>cmd</kbd> + <kbd>,</kbd> 可以打開設定頁面，點一下`Install`，在搜尋框輸入 Package 名稱進行搜尋，對搜尋結果點一下 `Install` 就可以安裝囉。

同樣的必裝Plugin可以參考[前一篇](section1.md)推薦的必裝清單。

特別注意建議不要安裝 Facebook 推出的 nuclide 系列套件，目前該套件還不穩，容易使 Atom crash

[1]: https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/sublime_download.png
[2]: https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/sublime_main.png
[3]: https://raw.githubusercontent.com/eric0324/ITAC_html_css/master/img/section2/sublime_console.png
