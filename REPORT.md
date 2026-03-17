# Laporan Assignment 0 - Hello World

## Deskripsi Tugas
Pada tugas ini, saya diminta untuk memodifikasi program "Hello World" sederhana dalam bahasa C++ yang sudah disediakan pada template. Program harus dapat menerima input berupa nama pengguna dan menampilkannya kembali ke layar dalam format sapaan. Karena terdapat kendala pada GitHub Classroom, pengumpulan dilakukan melalui repositori GitHub personal yang diatur sebagai publik.

## Langkah-Langkah Pengerjaan

### 1. Persiapan Lingkungan Kerja (Workspace) & Repositori
* Mengunduh file template `assignment0-master.zip` dari myITS Classroom dan mengekstraknya ke dalam direktori lokal.
* Membuat repositori baru di akun GitHub personal dengan status **Public** bernama `assignment0-hello-world-andra`.
* Membuka folder hasil ekstraksi (`assignment0-master`) menggunakan Visual Studio Code untuk memulai pengerjaan.

### 2. Modifikasi Kode Program C++
File utama yang diedit adalah `src/main.cpp`. Berikut adalah langkah modifikasi yang dilakukan:
* Menambahkan header `<string>` agar program dapat menggunakan tipe data teks (string) untuk menyimpan nama.
* Mendeklarasikan variabel `string nama;`.
* Menambahkan perintah `cout` untuk mencetak instruksi input ke layar.
* Menggunakan fungsi `getline(cin, nama)` untuk mengambil input dari pengguna. Penggunaan `getline` sangat penting dibandingkan `cin >>` biasa agar karakter spasi pada input nama (contoh: "Budi Ani") dapat ikut terbaca dengan sempurna.
* Mencetak hasil akhir sapaan menggunakan `cout`.

**Source Code (`src/main.cpp`):**
```cpp
#include <iostream>
#include <string>

using namespace std;

int main(int argc, char ** argv) {
    string nama;
    
    cout << "Silahkan inputkan nama Anda: ";
    getline(cin, nama);
    cout << "Hello " << nama << endl;

    return 0;
}