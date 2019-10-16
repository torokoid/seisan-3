# seisan-3
<html lang="ja">
<head>
<meta charset="UTF-8">
  <title>人数変動可能な会計（公金考慮）</title>
 
<style type="text/css">
p {
color: #0d0015;
font-size: 1.5em;
}
 
body { background-color: #33ff99; }
 
</style>
<link rel="stylesheet" href="../style.css/" type="text/css">
 
</head>
 
<body>
 
  <section>
<h2>会計計算（公金からの補助金額を反映）-JavaScriptバージョンアップ版_3</h2>
  <script>
    var selects = prompt('参加人数を入力！');
 
    var selectss = prompt('支払った人の人数を入力！');
 
    var koukin = prompt('公金補助額を入力！');
 
var nama = [];
    for (var i=0; i<selectss; i++){
      nama[i] = prompt("支払った人の名前を入力");
    }  
 
var menu = [];   
    for (var i=0; i<selectss; i++){
      menu[i] = prompt(nama[i] + "さんの支払金額を入力");
    }
 
document.write("各自の支払金額は<br>")
    for (var i=0; i<menu.length; i++){
      document.write(nama[i] + "さん：" + menu[i] + "円 <br>")
    }
 
//各自の会計額を計算
 
var kasann = [];
      kasann[0] = menu[0];
    for (var i=0; i<selectss-1; i++){
kasann[i+1] = Math.round (Number(kasann[i]) + Number(menu[i+1]));
      }
 
var kasan = Math.round (Number(kasann[i]) - Number(koukin))
 
//各自の分担分を計算
 
var buntan = Math.round (Number(kasan)/Number(selects));
 
//各自の割り勘分を計算
 
var wari = [];
    for (var i=0; i<selects; i++){
    wari[i] = Math.round (Number(menu[i]) - Number(buntan));
      }
 
var kasann = kasann[selectss-1]

document.write("<br>参加人数：" + selects + "人<br>")
      
document.write("支払った人の人数：" + selectss + "人<br>")
 
document.write("経費の総額：" + kasann + "円<br>")
 
document.write("公金補助額：" + koukin + "円<br>")
 
document.write("精算金額の総額：" + kasan + "円<br>")
 
document.write("一人当たりの分担：" + buntan + "円<br>")
 
document.write("<br>支払った人への払い戻し金額は<br>")
    for (var i=0; i<menu.length; i++){
      document.write(nama[i] + "さん：" + wari[i] + "円 <br>")
    }
 
document.write ("<br>以上、お帰りも気を付けて、来年も元気に再開～(^^)/");
</script>
</section>
 
</body>
</html>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<!-- フッタ -->
<footer>
Copyright 2018/12/11 S.Hada
</footer>
