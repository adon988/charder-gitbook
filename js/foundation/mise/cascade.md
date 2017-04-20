# Cascade / Chain

有一些方法沒有回傳值，以設定或改變物件狀態的方法為例，他們通常不會有回傳值。如果我們讓這類的例子改為回傳 this，可以設計出 cascade style。

```js
$("#p1").css("color", "red").slideUp(2000).slideDown(2000);
```