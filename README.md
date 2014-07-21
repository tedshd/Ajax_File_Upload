Ajax_File_Upload
================

### Introduction

利用 javascript 達到檔案上傳的功能

### Release

Beta(Now is prototype)

### Feature

* 顯示上傳進度
* 多檔上傳
* ~~取消上傳~~
* ~~拖拉上傳~~
* ~~**[斷點續傳??](http://www.resumablejs.com/)**~~
* ~~chrome 上傳資料夾~~
* ~~盡可能跨 browser(for IE8)~~
* 不依攋任一 javascript library

### Develop

* 單純用 javascript
* 利用 AJAX 上傳
* 處理 AJAX 上傳在 IE 的問題(利用 iframe 也許可解, [Refer](http://malsup.com/jquery/form/))
* 處理拖拉
* 處理拖拉資料夾
* 處理預設樣式

### DevLog

[Log & note](http://tedshd.logdown.com/posts/153606-javascript-file-upload)

### Issue

* [FormData](https://developer.mozilla.org/en-US/docs/Web/API/FormData)
  * AJAX 上傳(IE10 以上)
  * IE 利用 iframe 實作

#### Attribute

* inputFileNode(input type file element)
* fileName(```name=""```)
* server(the file upload to server url)
* dropArea(set the drop area)

#### Method

* upload
* ~~cancel~~

#### Event

Use [CustomEvent](https://developer.mozilla.org/en-US/docs/Web/API/CustomEvent) (IE 9 up)
[Refer - How to Create Custom Events in JavaScript](http://www.sitepoint.com/javascript-custom-events/)

* selectFiles
  * e.fileList (Array)
      * name
      * size
      * type
  * e.length (number)
* ~~uploadError~~
* uploadProgress
  * e.bytesLoaded (number)
  * e.bytesTotal (number)
  * e.percentLoaded (number)
* ~~uploadComplete~~
* ~~dragenter~~
* ~~dragover~~
* ~~drop~~
* ~~drag~~

#### About code

Get DOM use querySelector replace getElementById、getElementsByTagName...etc(IE8 up)
[document.querySelector](https://developer.mozilla.org/en-US/docs/Web/API/document.querySelector)
Use node method to reduce code
