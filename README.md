### Refleksi

List Code Quality Issue yang dihadapi:

- AvoidDuplicateLiterals, terjadi ketika literal berulang kali diketik dan muncul berkali kali
- EmptyStatementNotInLoop, terjadi ketika terdapat semicolon yang tidak mengakhiri apa apa (statement kosong)

Untuk AvoidDuplicateLiterals, strategi saya untuk memperbaikinya adalah mendaklarasikan variable konstan untuk menampung literal tersebut dan menggunakan variable tersebut

Untuk EmptyStatementNotInLoop, saya menghapus semicolon yang memiliki empty statement

Implementasi tersebut sudah memenuhi kriteria Continuous Integration karena setiap perubahan kode pada semua branch secara otomatis melakukan unit testing dan analisis untuk menjaga kualitas kode. Namun, aspek Continuous Deployment belum sepenuhnya terpenuhi karena proses rilis ke produksi (Koyeb) hanya berupa perintah echo dan belum merupakan skrip deployment yang mengeksekusi pembaruan aplikasi secara nyata. Skrip Workflow tersebut tidak benar benar memverifikasi apakah deployment di Koyeb berhasil