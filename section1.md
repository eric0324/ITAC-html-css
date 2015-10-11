# 初探HTML-從觀察開始

###前言
這是一篇寫給ITAC社員用教材，主要依照社員的程度來撰寫，至於會寫幾篇暫時還不知道呵呵。
這一系列教學比較不會像傳統教材Step by Step的進行，主要是引導大家如何自主學習HTML。

###從觀察開始
![Imgur][1]
Dcard的首頁（未登入的狀況下）

這些東西到底怎麼做出來的呢？

首先打開瀏覽器的開發者工具跟著我一起觀察吧～

####開啟開發者工具

Mac 上的 Safari、Firefox、Chrome、Opera都可以透過
`command` + `option` + `I` 這個組合按鈕打開開發者工具

Windows則是
`Ctrl` + `Shift` + `I`

Mac上若按了組合鍵之後沒有反應可以參考下面的設定方法，再試一次
Safari: 按下`command` + `,` 打開`偏好設定`，點一下`進階`，將最下方的`在選單列中顯示「開發」選單`打勾
Opera: 按一下`檢視` -> `顯示「研發工具」選單`

當然你也可以對網頁上想要觀察的元件點一下右鍵選擇`檢視元件`(或者是`檢視元素`)，也可以直接打開開發者工具，並會直接在跳到該元件的原始碼上。

![Imgur][3]
Chrome的開發者工具

以下說明會用Chrome做為示範

####認識HTML
![][4]
首頁上最顯眼標語，在HTML看起來是什麼樣子呢？對他戳一下右鍵選擇`檢視元件`（或者是`檢視元素`）
![][5]
可以看到原始碼當中對應的位置的被選起來了。

由
```
<p>
				有些緣分，<br>
				只有短短 24 小時的機會。<br>
				一旦錯過，他就會永遠消失<br>
				再也不會出現。
</p>
```
這段程式碼構成畫面上的這段文字

程式碼當中的`p`通常會我們會稱作tag name

不同的tag name對應著不同的網頁物件

`p`對應是段落，其他還有像是`h1`對應的是第一級標題等。

大部分的寫法形式都會是

```
	<tag>內容</tag>
```

也有少部分會是

```
	<tag />
```

像是`<img />`

用法
```
<img src="路徑" />
```

例如放入Dcard網頁上的某張圖
```
<img src="//www.dcard.tw/img/dcard_index_res/dcard_city.svg">
```
<img src="//www.dcard.tw/img/dcard_index_res/dcard_city.svg">

這時候你可能會覺得他看起來超級大，想要設定一下他的寬高

```
<img src="//www.dcard.tw/img/dcard_index_res/dcard_city.svg" width="300" height="300">
```
<img src="//www.dcard.tw/img/dcard_index_res/dcard_city.svg" width="300" height="300">

有時候tag也可能包含一些設定值或稱為**屬性(attribute)**

```
	<tag attr="value" />
```
像是前面img tag用來設定寬高的`width`和`height`都是屬於img的屬性喔！

詳細的各種Tag說明你可以參考：
* [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
* [W3SCHOOL](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

在開發者工具中，你會看到很多像是這樣形式的程式碼，甚至不乏有tag中包含tag的狀況。

這樣的程式語言，被稱為標記語言 Markup Language，我們所看到的網頁就是由這樣的語言來構成的。

###網頁的基本架構

仔細觀察各個網頁基本上通常會包含以下的形式

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
* `<!DOCTYPE html>` 的作用是宣告以下的程式碼是HTML語言
* `<head></head>` 裡面包含的通常是在網頁尚未呈現於瀏覽器前預先告知的資訊，例如JavaScript和樣式表的載入、網頁標題、網頁編碼等等。
* `<body></body>` 裡面所包含的部分就是我們在網頁上往看到的內容。

####什麼是網頁編碼？
電腦上的資料都是由0和1組成的二進位資訊進行儲存的，中文字也不例外。不同的文字對應到不同的二進位數值。
將文字符號和一個二進位數值設定為對應關係的過程稱為編碼。若採用不同的二進位編碼，同樣的文字可能對應到不一樣的二進位數值，因此需要在在網頁開頭標明使用的編碼方式。
早期不同語言的網頁會採用不同的編碼方式，但現今為了在網頁上容納多國語言多採用"UTF-8"的方式進行編碼。

####DOM(Document Ojbect Model)

前面提到html當中，tag可以是一層包一層的關係，tag也可以包含屬性，若我們把html想成一棵樹可以看成像是這樣：
> ![DOM Tree][7]
> 取自W3School http://www.w3schools.com/js/js_htmldom.asp

這棵樹和之後我們學CSS、JavaScript和jQuery有很大的關聯度喔。

###預告

下一篇會開始進入動手寫HTML的階段，大家可以開始找自己喜歡的編輯器囉，以下推薦兩款編輯器，大家可以從中挑一款自己喜歡的。

####Atom - Github開發的文字編輯器
[官方網站](https://atom.io)

必裝套件
* [Emmet](http://emmet.io)
* [css-snippets](https://atom.io/packages/css-snippets)	超強大的自動完成（？
* [jquery-snippets](https://atom.io/packages/jquery-snippets)	jquery的自動補完工具
* [docblockr](https://atom.io/packages/docblockr)		寫註解專用，之後寫javascript會很常用到註解喔！

####Sublime Text 3

[官方網站](http://www.sublimetext.com/3)

必裝套件
 * [Package control](https://packagecontrol.io)	套件管理工具，先裝這個才能裝底下的東西喔
 * [Emmet](http://emmet.io)	超強大的自動完成（？
 * [docblockr](https://packagecontrol.io/packages/DocBlockr)	寫註解專用，之後寫javascript會很常用到註解喔！
 * [jQuery](https://packagecontrol.io/packages/jQuery)	jquery的自動補完工具
 


[1]: http://i.imgur.com/iR3zlte.png
[2]: http://i.imgur.com/hwZb23i.png
[3]: http://i.imgur.com/i0AyTzX.png "右方為chrome的開發者工具"
[4]: http://i.imgur.com/fgOJC9m.png
[5]: http://i.imgur.com/twH466X.png
[6]: http://i.imgur.com/vSdH8zt.png "css"
[7]: http://www.w3schools.com/js/pic_htmltree.gif "DOM Tree"