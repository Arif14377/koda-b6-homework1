# Switc-Case dan Penggunaannya
## Pengertian
Switch Statement adalah mekanisme control flow yang lebih mudah dibaca sebagai alternatif dari banyaknya statement if...else if...else, terutama ketika berurusan dengan beberapa kemungkinan nilai.

## Syntax
switch (expression) {
    case x:
        //kode blok;
        break;
    case y:
        //kode blok;
        break;
    default:
        //kode blok;
}

## Cara kerja switch-case
1. switch expression dievaluasi sekali
2. nilai dari expression dibandingkan dengan nilai yang ada pada setiap case
3. jika ada kecocokan, maka kode blok akan dieksekusi
4. jika tidak ada yang cocok, maka tidak ada kode blok yang dieksekusi

## Break keyword
- ketika break keyword dijalankan, maka program akan keluar dari switc statement dan tidak ada lagi kode blok yang dijalankan.
- case terakhir tidak perlu menggunakan switch, karena eksekusi akan berhenti di akhir case.

## Default keyword
- default keyword akan menjalankan kode blok jika tidak ada case yang cocok.
- default keyword bersifat optional.
- default keyword tidak harus selalu ditulis diakhir, namun jika bukan diakhir perlu pakai break.

## Sharing kode blok
- jika ingin menjalankan kode blok yang sama pada case yang berbeda, maka bisa menambahkan case selanjutnya setelah case. contoh:

let jawaban = *input angka ganjil antara 1 sampai 5.

switch (jawaban) {
    case 1:
    case 3:
    case 5:
        console.log("Benar. Ini adalah bilangan ganjil");
        break;
    case 2:
    case 4:
        console.log("Coba lagi, ini adalah bilangan genap");
        break;
    default:
        console.log("input yang anda masukkan tidak sesuai. Masukkan angka antara 1 sampai 5");
}

## Strict Comparison
switch menggunakan perbandingan ketat ( === ), jadi tipe data dan nilai harus sama. contoh di bawah ini tidak ada yang cocok dengan nilai dari variabel x, dan akan menjalankan default.

let x = "0"

switch (x) {
    case 0:
        console.log("off");
        break;
    case 1:
        console.log("on");
        break;
    default:
        console.log("no value found")
}