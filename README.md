# kalkulator
script_kalkulator
<?php
 if (isset($_POST['proses'])) {
 $pertama = $_POST['pertama'];
 $kedua = $_POST['kedua'];
 $operasi = $_POST['operasi'];
  switch ($operasi) {
   case 'tambah':
    $hasil = $pertama + $kedua;
   break;
   case 'kurang':
    $hasil = $pertama - $kedua;
   break;
   case 'kali':
    $hasil = $pertama * $kedua;
   break;
   case 'bagi':
    $hasil = $pertama / $kedua;
   }
}
 ?>
<!DOCTYPE HTML>
<html>
<head>
  <meta charset="utf-8">
  <title>Kalkulator</title>
  <link href="style.css" rel="stylesheet" type="text/css">

 <body>
 <div class="kalkulator">
  <h1>KALKULATOR</h1>
  <form action="" action="" method="post">
   <input class="number" type="number" name="pertama" placeholder="Masukkan Bilangan Pertama">
   <input class="number" type="number" name="kedua" placeholder="Masukkan Bilangan Kedua">
   <select class="option" name="operasi">
    <option value="tambah">+</option>
    <option value="kurang">-</option>
    <option value="kali">x</option>
    <option value="bagi">/</option>
   </select>
   <input type="submit" name="proses" class="tombol" value="Hitung">
  </form>

  <?php if(isset($_POST['proses'])){ ?>
   <input type="text" value="<?php echo $hasil; ?>" class="number">
  <?php }else{ ?>
   <input type="text" value="0" class="number">
  <?php } ?> <br>
    
</div>
 </body>
 </html>

