# lab7Web
1. Persiapan Awal
Install XAMPP:

Unduh XAMPP dari situs resmi XAMPP.
Pilih versi yang sesuai dengan sistem operasi Anda (Windows/Linux/MacOS).
Instal XAMPP di direktori (misalnya: d:\xampp).
Jalankan Web Server:

Buka XAMPP Control Panel.
Start Apache dan MySQL.

![image](https://github.com/user-attachments/assets/c6f65d9f-2fea-48d7-a6cd-bc69aa5135ff)

Uji Server:

Buka browser dan akses http://localhost.
Jika halaman utama XAMPP muncul, server berhasil dijalankan.

![image](https://github.com/user-attachments/assets/06ff6506-c718-4d59-b969-ec96c44e9af5)

2. Buat Direktori dan File PHP
Buat Folder Project:

Di direktori htdocs (misalnya: d:\xampp\htdocs), buat folder bernama lab7_php_dasar.
Buat File PHP:

![image](https://github.com/user-attachments/assets/b7f1068c-6d88-4b1f-aac4-224ae6f4a19d)

Di dalam folder lab7_php_dasar, buat file baru bernama php_dasar.php.
Gunakan editor seperti Visual Studio Code atau Notepad++.
Tulis Kode Dasar PHP:

Tambahkan kode berikut di file php_dasar.php untuk menguji PHP:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World!";
    ?>
</body>
</html>

![Screenshot 2024-11-17 071048](https://github.com/user-attachments/assets/008e5401-647b-4aca-96da-a227ac9cd45a)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World!";
    ?>
</body>
</html>

<h1>Menggunakan Variabel</h1>
<?php
$nim = "312310763";
$nama = 'Sidik Ghozali';
echo "NIM : " . $nim . "<br>";
echo "Nama : $nama";
?>

![Screenshot 2024-11-17 072221](https://github.com/user-attachments/assets/667fe322-747e-4538-8039-704188fa9ee4)

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
<form method="post">
<label>Nama: </label>
<input type="text" name="nama">
<input type="submit" value="Kirim">
</form>
<?php
echo 'Selamat Datang ' . $_POST['nama'];
?>
</body>
</html>

![Screenshot 2024-11-17 072345](https://github.com/user-attachments/assets/c8125a18-0b57-4f47-9f9a-c83c055220e1)

Operator
<?php
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji * $pajak);
echo "Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp";
?>
![Screenshot 2024-11-17 074032](https://github.com/user-attachments/assets/47a8b033-4280-4fba-b76e-5ec40816cafe)

<?php
$nama_hari = date("l");
if ($nama_hari == "Sunday") {
    echo "Minggu";
} elseif ($nama_hari == "Monday") {
    echo "Senin";
} else {
    echo "Selasa";
}
?>
![Screenshot 2024-11-17 074236](https://github.com/user-attachments/assets/f70c8596-94ff-47de-bfaf-f95b86c19026)

<?php
$nama_hari = date("l");
switch ($nama_hari) {
    case "Sunday":
        echo "Minggu";
        break;
    case "Monday":
        echo "Senin";
        break;
    case "Tuesday":
        echo "Selasa";
        break;
    default:
        echo "Sabtu";
}
?>
![image](https://github.com/user-attachments/assets/1435a93b-2ec3-40b1-a975-1fa2d49d9fa2)

<?php
echo "Perulangan 1 sampai 10 <br />";
for ($i = 1; $i <= 10; $i++) {
    echo "Perulangan ke: " . $i . '<br />';
}

echo "Perulangan Menurun dari 10 ke 1 <br />";
for ($i = 10; $i >= 1; $i--) {
    echo "Perulangan ke: " . $i . '<br />';
}
?>
![image](https://github.com/user-attachments/assets/9b4116df-3958-479b-ae23-63934e5329b1)

<?php
echo "Perulangan 1 sampai 10 <br />";
$i = 1;
while ($i <= 10) {
    echo "Perulangan ke: " . $i . '<br />';
    $i++;
}
?>

![image](https://github.com/user-attachments/assets/2f55d8f8-a972-425b-921a-199e203071fb)

<?php
echo "Perulangan 1 sampai 10 <br />";
$i = 1;
do {
    echo "Perulangan ke: " . $i . '<br />';
    $i++;
} while ($i <= 10);
?>
![image](https://github.com/user-attachments/assets/8601efb0-3efd-4e52-81fb-fdcb3ad1a44f)

*Pertanyaan dan Tugas*
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan
nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung
umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang
berbeda-beda sesuai pilihan pekerjaan.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Input</title>
</head>
<body>
    <h2>Form Input</h2>
    <form method="post">
        <label>Nama:</label>
        <input type="text" name="nama" required><br><br>

        <label>Tanggal Lahir:</label>
        <input type="date" name="tanggal_lahir" required><br><br>

        <label>Pekerjaan:</label>
        <select name="pekerjaan" required>
            <option value="Programmer">Programmer</option>
            <option value="Desainer">Desainer</option>
            <option value="Manager">Manager</option>
        </select><br><br>

        <input type="submit" value="Submit">
    </form>

    <?php
    if ($_SERVER['REQUEST_METHOD'] === 'POST') {
        $nama = $_POST['nama'];
        $tanggal_lahir = $_POST['tanggal_lahir'];
        $pekerjaan = $_POST['pekerjaan'];

        // Menghitung umur
        $birthDate = new DateTime($tanggal_lahir);
        $today = new DateTime();
        $age = $today->diff($birthDate)->y;

        // Gaji berdasarkan pekerjaan
        $gaji = 0;
        switch ($pekerjaan) {
            case 'Programmer':
                $gaji = 8000000;
                break;
            case 'Desainer':
                $gaji = 6000000;
                break;
            case 'Manager':
                $gaji = 10000000;
                break;
        }

        echo "<h3>Hasil:</h3>";
        echo "Nama: $nama<br>";
        echo "Tanggal Lahir: $tanggal_lahir<br>";
        echo "Umur: $age tahun<br>";
        echo "Pekerjaan: $pekerjaan<br>";
        echo "Gaji: Rp. " . number_format($gaji, 0, ',', '.') . "<br>";
    }
    ?>
</body>
</html>

![image](https://github.com/user-attachments/assets/783f553c-1f37-442d-a149-6eb96508b3ea)
