step 1

首先將檔案放在你要建置的網資料夾中

step 2(如果直接使用整包範例檔可以跳過)

確認nodejs已經正確安裝後用終端機跑指令碼

npm run build

將資料夾全部建置完成

step 3

輸入指令

npm i 將目前套件安裝

step 4(如果直接使用整包範例檔可以跳過)

在建立起來的dev文件內建立 index.html 檔案

step 5

輸入 npm run watch 開啟監聽

step 6

如果有無法轉譯的情況請直接在終端機按下 Ctrl+C 結束監聽

然後重新跑一次 npm run watch 有問過老師他說偶爾會這樣



說明


========================================================================


Html引入等可以使用include方式製作

利用名為 jsLink.html 的檔案

```html

<script src="@@jsLink"></script>

```

然後再要include的js檔案內利用下方這段直接引入

        @@loop('html/jsLink.html',[
        {"jsLink" : "js/TweenMax.min.js"},
        {"jsLink" : "js/TimelineMax.min.js"},
        {"jsLink" : "js/ScrollMagic.min.js"},
        {"jsLink" : "js/animation.gsap.min.js"},
        {"jsLink" : "js/debug.addIndicators.min.js"}
        ])

記得注意順序

========================================================================

scss請全部打包成一個名為main.css的檔案,記得html全部引入這個檔案

記得將自己的scss在main.scss中import注入

記得注意順序

========================================================================

請將要引入的外部css或是js等放入對應lib資料夾進行引入,可以利用上方include或是直接使用cdn進行引入

注意cdn方式會受限於網路連線狀態等外部因素引響

========================================================================

有問題可以直教詢問