
# 📲 Tutorial Setup Firebase untuk Proyek ESP32, MIT App, dan Web

Berikut langkah-langkah lengkap untuk mengatur Firebase sebagai backend komunikasi antara ESP32, MIT App Inventor, dan Web:

---

## 🔧 Langkah-langkah Setup Firebase

1. Buka website Firebase: [https://firebase.google.com](https://firebase.google.com), lalu klik **"Go to console"**
2. Klik **"Create Firebase Project"**
3. Masukkan nama project
4. Aktifkan semua pengaturan yang diminta (enable all)
5. Untuk konfigurasi Google Analytics, pilih **"Gunakan akun default"**, lalu klik **"Create"**
6. Setelah berhasil, klik **"Continue"**

---

## 🔗 Setup Realtime Database

7. Masuk ke menu **"Build"** dan pilih **"Realtime Database"**
8. Klik **"Create Database"**
9. Pilih lokasi server (misalnya asia-southeast1), lalu klik **"Next"**
10. Pilih **"Start in locked mode"**, lalu klik **"Enable"**
11. Salin dan simpan **URL** project kamu, contohnya:
   ```
   https://belajar-cc445-default-rtdb.firebaseio.com/
   ```

### 📌 NOTE:
Pada bagian **Rules**, ubah menjadi seperti berikut jika kamu ingin Firebase digunakan untuk komunikasi (dari MIT App atau ESP32):
```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

---

## 🔐 Setup Authentication

15. Masuk ke **"Build" > "Authentication"**, lalu klik **"Get Started"**
16. Setelah masuk ke tab **"Sign-in method"**, pilih opsi **"Anonymous"**
17. Aktifkan **Anonymous login** dengan klik selector ke **Enable**, lalu klik **Save**

---

## 🔑 Dapatkan API Key & Token

18. Klik ikon ⚙️ di samping **"Project Overview"**, lalu pilih **"Project Settings"**

### a. Firebase Token (untuk MIT App / Web Interface)
19. Masuk ke tab **"Service accounts"**, lalu pilih **"Database secrets"**
20. Salin token yang muncul, contoh:
   ```
   dVIiUG5wYPwNc1Brf8TysoxPCGuluVLYn1MTAL3e
   ```

### b. API Key & Database URL (untuk ESP32)
21. Kembali ke tab **"General"** di project settings
22. Scroll ke bawah hingga menemukan ikon `</>` (Add Firebase to your web app)
23. Masukkan nama register (bebas), centang **"Also set up Firebase Hosting for this app"**, lalu klik **"Register"**
24. Akan muncul data penting seperti:

```js
apiKey: "AIzaSyXXXXXXX",
authDomain: "belajar-cc445.firebaseapp.com",
databaseURL: "https://belajar-cc445-default-rtdb.firebaseio.com",
projectId: "belajar-cc445",
...
```

25. Klik **Next → Next → Continue to Console**

---

## 📝 Ringkasan

| Jenis Token       | Digunakan Untuk           |
|-------------------|---------------------------|
| 🔐 **Firebase Token**  | MIT App / Web Interface |
| 🔑 **API Key**         | Kode ESP32              |
| 🌐 **Database URL**    | Kode ESP32              |

---

**✅ Setup Firebase berhasil!**  
Sekarang kamu bisa mulai menghubungkan Firebase dengan ESP32 dan MIT App Inventor.

---

🛠 *Tutorial ini dibuat oleh Mardinata Indra K. untuk keperluan proyek IoT monitoring duduk berbasis Firebase.*
