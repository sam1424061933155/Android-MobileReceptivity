# Mobile-Receptivity<br><br>

## Version<br>
**4/13**<br>
1. questionnaire 增加disable機制，不需要填的會disable
2. 資料上傳部分，會檢查firebase最新一筆資料和sqlite上次上傳的最後一筆是否相同，相同才將舊的sqlite資料刪掉  

**4/15**<br>
1. 資料上傳，以時間為基準點，firebase上最後一筆資料的時間（millis）和sqlite裡面的相比，比firebase早的刪掉，晚的上傳

**4/18**<br>
1. 資料不會當下query的時候馬上上傳，會在下一次query(5秒後)才會上傳

## Problem<br>
**4/13**<br>
1. 管理app工具會阻檔app服務自動啟動
2. notification listener因為cache可能需要重開才可以連結<br>
http://stackoverflow.com/questions/33530807/why-is-this-notificationlistenerservice-not-working  

**4/15**<br>
1. datasnapshot.getvalue(class name) not working  

**4/18**<br>
1. IllegalState Exception, NumberFormat Exception.
