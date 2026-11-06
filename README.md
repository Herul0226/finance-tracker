
# 📱 Cara Konfigurasi Project Menjadi APK

Ikuti langkah-langkah berikut untuk mengonfigurasi project agar dapat dibuild menjadi aplikasi Android (`.apk`) menggunakan **Capacitor**.

## 1. Inisialisasi Project & Instalasi Capacitor

Buka CMD atau Terminal, kemudian pastikan Anda sudah berada di dalam folder project aplikasi.

Jalankan perintah berikut secara berurutan:

```bash
npm init -y
npm install @capacitor/core
npm install @capacitor/cli --save-dev
```

## 2. Membuat Konfigurasi Capacitor

Jalankan perintah berikut untuk memulai konfigurasi Capacitor:

```bash
npx cap init
```

Setelah perintah dijalankan, Anda akan diminta mengisi beberapa informasi berikut:

| Konfigurasi | Contoh |
|---|---|
| App Name | Keuanganku |
| App Package ID | com.walletkun.app |
| Web Directory | www |

**Keterangan:**
- **App Name:** Nama aplikasi yang akan ditampilkan pada perangkat.
- **App Package ID:** Identitas unik aplikasi Android.
- **Web Directory:** Folder yang berisi file aplikasi web, seperti `index.html`.

## 3. Menambahkan Platform Android

Instal dan tambahkan platform Android ke dalam project dengan menjalankan perintah berikut:

```bash
npm install @capacitor/android
npx cap add android
```

## 4. Sinkronisasi File Web ke Android

Pastikan seluruh file aplikasi, termasuk `index.html`, CSS, JavaScript, dan aset lainnya sudah berada di dalam folder `www`.

Selanjutnya, jalankan perintah berikut untuk menyinkronkan file web ke project Android:

```bash
npx cap sync
```

Perintah ini akan menyalin dan memperbarui file aplikasi web ke dalam project Android.

## 5. Membuka Project di Android Studio

Setelah proses sinkronisasi selesai, buka project Android menggunakan Android Studio dengan perintah:

```bash
npx cap open android
```

Selanjutnya, Anda dapat melakukan proses build APK melalui Android Studio.

---

## 🔄 Perintah Rutin Setelah Update Aplikasi

Jika terdapat perubahan atau pembaruan pada kode aplikasi, Anda **tidak perlu mengulangi seluruh proses instalasi** dari awal.

Cukup jalankan perintah berikut melalui CMD atau Terminal:

```bash
npx cap sync
```

Perintah tersebut akan memperbarui file aplikasi web ke dalam project Android.

Setelah sinkronisasi selesai, buka kembali Android Studio untuk melakukan build APK terbaru.

---

## 📦 Proses Build APK

Setelah project terbuka di Android Studio:

1. Tunggu hingga proses Gradle Sync selesai.
2. Pilih menu **Build**.
3. Pilih **Build Bundle(s) / APK(s)**.
4. Klik **Build APK(s)**.
5. Tunggu hingga proses build selesai.
6. Klik **Locate** untuk menemukan file APK yang telah dibuat.

File APK biasanya tersimpan di direktori:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

---

**🎉 Selesai!**

Project aplikasi Anda kini sudah dikonfigurasi menggunakan Capacitor dan siap dibuild menjadi aplikasi Android (`.apk`).
