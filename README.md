# js 書く

```
$(function(){

//処理

});
```

の形の話。。。。
関数内で定義した変数は外部では使えない。
関数外、つまり<script></script>内（jsファイル内）
の関数に入ってないところで定義したものは「グローバル変数」として保存され、
関数内部でも使える。。ただ、危険。。



$(function(){});      ()で括られていると、即時関数：定義と実行を同時に行う。



これがreadyのタイミング　　他には、、

```
$(document).ready(function() {});

jQuery(function() {});//省略系

document.addEventListener('DOMContentLoaded', function(){},false);
```

DOMツリーの構築が完了したら実行。－＞更新したときに元のデザインが一瞬移ったりする。

***

次にload、、

```
$(window).on('load',function(){});

$(window).load(function(){});

window.onload = function(){}
```

画像、動画など関連データの読み込みが完了したら実行。

***

こういう処理が複数存在する場合は、
順番によって、機能しないものがある。


ex)　load  の物
　　 readyの物
　　 load  の物
   

最初のloadは表示されない。。（飛ばされる？）

参考ＵＲＬ
https://qiita.com/mimoe/items/74cb3a01a30162759fdd
