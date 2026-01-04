# P9-WSE-API-Integration-23010404126

![Status](https://img.shields.io/badge/Status-Completed-success)
![Course](https://img.shields.io/badge/Course-Web%20Service%20Engineering-blue)

[cite_start]Repositori ini berisi proyek praktikum ke-9 mata kuliah **Web Service Engineering (WSE)** yang berfokus pada pembangunan backend Node.js menggunakan arsitektur modular untuk mengintegrasikan API eksternal[cite: 1, 7, 8]. [cite_start]Proyek ini mencakup implementasi struktur *routes-controllers-services*, *caching*, *logging*, *error handling*, serta dokumentasi interaktif menggunakan Swagger[cite: 10].

## 📋 Deskripsi Proyek
[cite_start]Mahasiswa membangun layanan backend yang stabil dan terstruktur dengan mengintegrasikan dua API eksternal utama[cite: 8, 11]:
* [cite_start]**REST Countries**: Digunakan untuk mendapatkan data informasi negara melalui berbagai filter[cite: 9, 28].
* [cite_start]**OpenWeatherMap**: Digunakan untuk mendapatkan data cuaca real-time berdasarkan query kota[cite: 9, 29].

## 🎯 Tujuan Praktikum
1. [cite_start]**Memahami Arsitektur Modular**: Memisahkan komponen aplikasi menjadi *routes, controllers, services, middleware, utils,* dan *docs*[cite: 16].
2. [cite_start]**Integrasi API Eksternal**: Mengonsumsi data dari REST Countries dan OpenWeatherMap dengan parameter yang aman[cite: 17].
3. [cite_start]**Menerapkan Caching**: Menggunakan `NodeCache` untuk mengurangi latensi dan beban panggilan API[cite: 18, 30].
4. [cite_start]**Logging & Error Handling**: Monitoring setiap request dengan `morgan` serta penanganan respons error yang konsisten[cite: 19, 31].
5. [cite_start]**Penyusunan Dokumentasi API**: Menyajikan Swagger UI sebagai sarana uji coba dan eksplorasi endpoint[cite: 20].

## 🛠️ Tools & Teknologi
* [cite_start]**Node.js LTS**: Runtime JavaScript utama untuk server[cite: 37].
* [cite_start]**Express**: Framework HTTP untuk manajemen routing dan middleware[cite: 38].
* [cite_start]**Axios**: HTTP client untuk melakukan panggilan ke API eksternal[cite: 39].
* [cite_start]**NodeCache**: Sistem caching in-memory untuk meningkatkan performa[cite: 40].
* [cite_start]**Morgan**: Middleware untuk logging request/respons di terminal[cite: 41].
* [cite_start]**Swagger UI Express**: Dokumentasi API interaktif berbasis OpenAPI[cite: 42].
* [cite_start]**Dotenv**: Manajemen variabel lingkungan atau file `.env`[cite: 42].

## 📂 Struktur Folder Proyek
[cite_start]Proyek ini mengikuti struktur folder modular sesuai dengan instruksi modul praktikum[cite: 60, 61]:

```text
P9-API-Integration-23010404126/
├── server.js               # Entry point utama aplikasi [cite: 62]
├── package.json            # Konfigurasi dependensi proyek [cite: 63]
├── .env                    # Variabel lingkungan (API Key & Port) [cite: 64]
└── src/                    # Folder sumber kode utama [cite: 65]
    ├── routes/             # Definisi routing endpoint [cite: 66]
    ├── controllers/        # Logika pemrosesan respons dan validasi [cite: 69]
    ├── services/           # Logika panggilan ke API eksternal [cite: 72]
    ├── middleware/         # Penanganan error global dan 404 [cite: 75]
    ├── utils/              # Fungsi pembantu (Caching & HttpClient) [cite: 78]
    └── docs/               # Konfigurasi dokumentasi Swagger [cite: 81]
```

## ⚙️ Instalasi & Penggunaan

### 1️⃣ Clone Repositori
```bash
git clone https://github.com/Vygmy/P9-WSE-API-Integration-23010404126.git
cd P9-WSE-API-Integration-23010404126
2️⃣ Inisialisasi & Instalasi Dependensi
bash
Salin kode
npm init -y
npm install express axios morgan node-cache swagger-ui-express dotenv
3️⃣ Konfigurasi Environment
Buat file .env di root folder, lalu isi dengan konfigurasi berikut:

env
Salin kode
PORT=3000
OWM_API_KEY=isi_dengan_api_key_openweathermap_anda
💡 Catatan:
API Key dapat diperoleh dari situs resmi
https://openweathermap.org/api

4️⃣ Jalankan Server
bash
Salin kode
npm start
📍 Endpoint API
Setelah server berhasil dijalankan, Anda dapat menguji endpoint berikut menggunakan Browser atau Postman:

🌍 Data Negara
Semua Negara
```
bash
Salin kode
http://localhost:3000/api/countries
Negara Berdasarkan Region

bash
Salin kode
http://localhost:3000/api/countries/region/asia
Negara Berdasarkan Nama

bash
Salin kode
http://localhost:3000/api/countries/name/indonesia
🌦️ Data Cuaca
Cuaca Berdasarkan Kota

bash
Salin kode
http://localhost:3000/api/weather?city=Palangkaraya
📘 Dokumentasi API
Swagger UI

bash
Salin kode
http://localhost:3000/docs

👨‍🏫 Dosen Pengampu
Muhayat, M.IT
