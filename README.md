# Proyek CI/CD menggunakan GitHub Actions

Proyek ini menerapkan **Continuous Integration (CI)** dan **Continuous Deployment (CD)** menggunakan **GitHub Actions**. Setiap kali ada perubahan pada branch `main`, *pipeline* akan dijalankan untuk memastikan kode diuji dan dideploy secara otomatis.

## Proses CI/CD

### 1. **Continuous Integration (CI)**

*Pipeline* CI akan secara otomatis dijalankan setiap kali terjadi perubahan pada branch `main`. Berikut adalah tahapan yang dilalui dalam *pipeline* **CI**:

- **Checkout Kode:** Mengambil versi kode terbaru dari repository.
- **Setup Node.js:** Menyiapkan environment Node.js sesuai dengan versi yang dibutuhkan.
- **Instal Dependensi:** Menginstal semua dependensi dengan menjalankan perintah `npm install`.
- **Pengujian Otomatis:** Menjalankan pengujian dengan menggunakan Jest melalui perintah `npm test` untuk memastikan tidak ada bug dalam aplikasi.

### 2. **Continuous Deployment (CD)**
Jika *pipeline* **CI** berhasil, *pipeline* **CD** akan dijalankan secara otomatis. Berikut langkah-langkah dalam proses **CD**:

- **Build Aplikasi:** Membangun aplikasi menggunakan perintah `npm run build`, yang akan menghasilkan file build di folder `out`.
- **Deploy ke GitHub Pages:** Menggunakan action `peaceiris/actions-gh-pages@v3` untuk mengunggah hasil build ke GitHub Pages.

GitHub Pages akan menggunakan branch `gh-pages` sebagai sumber deployment, sehingga aplikasi web dapat diakses melalui URL yang disediakan oleh GitHub.

### **3. Link Hasil Deployment**
Aplikasi yang telah dideploy dapat diakses melalui GitHub Pages dengan menggunakan link berikut:
[Link Halaman Aplikasi GitHub Pages](https://github.com/LuckyAb13/ci-cd-21060122130091-elektro)
