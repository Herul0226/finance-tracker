CARA KONFIGURASI PROGRAMNYA AGAR BISA DIBUILD MENJADI .APK 
**1. Inisialisasi Project & Instalasi Capacitor
**Buka CMD atau Terminal, pastikan Anda sudah berada di dalam folder project aplikasi Anda, lalu jalankan:

npm init -y
npm install @capacitor/core
npm install @capacitor/cli --save-dev

**2. Membuat Konfigurasi Capacitor
**
npx cap init
Catatan: Saat perintah ini dijalankan, terminal akan meminta Anda memasukkan:

App name: Ketik Keuanganku (atau nama aplikasi Anda)

App Package ID: Ketik com.walletkun.app (atau ID pilihan Anda)

Web directory: Ketik www (tempat Anda akan menyimpan file index.html)

**3. Menambahkan Platform Android
**Setelah inisialisasi selesai, instal dan tambahkan platform Android ke dalam project:

npm install @capacitor/android
npx cap add android

**4. Sinkronisasi File Web ke Android
**Pastikan file index.html yang baru saja Anda edit sudah dimasukkan ke dalam folder www. Setelah itu, jalankan perintah ini agar file HTML tersebut disalin ke dalam sistem Android:

npx cap sync

**5. Buka di Android Studio (Untuk Build APK)
**

npx cap open android
Perintah Rutin (Jika ada update kode di masa depan):
Setiap kali Anda mengedit atau memperbarui kode di file index.html, Anda tidak perlu mengulang instalasi dari awal. Cukup jalankan perintah ini di CMD:

DOS
npx cap sync
