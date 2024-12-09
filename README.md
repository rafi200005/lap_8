# Muhammad Rafi Albani Rasyin 
# 312410316
# TI.24.A.4
# Bahasa Pemograman

## Tugas Praktikum
Tugas Praktikum

Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan: • Method tambah() untuk menambah data • Method tampilkan() untuk menampilkan data • Method hapus(nama) untuk menghapus data berdasarkan nama • Method ubah(nama) untuk mengubah data berdasarkan nama

• Buat diagram class, flowchart dan penjelasan programnya pada README.md. • Commit dan push repository ke github.

## Lap 8
```python
class Mahasiswa:
    def _init_(self, nama, nilai):
        self.nama = nama
        self.nilai = nilai

class DaftarNilaiMahasiswa:
    def _init_(self):
        self.daftar_nilai = {}

    def tambah(self, nama, nilai):
        """Menambahkan data mahasiswa"""
        self.daftar_nilai[nama] = Mahasiswa(nama, nilai)
        print(f"Data {nama} berhasil ditambahkan.")

    def tampilkan(self):
        """Menampilkan data mahasiswa"""
        print("Daftar Nilai Mahasiswa:")
        for mahasiswa in self.daftar_nilai.values():
            print(f"Nama: {mahasiswa.nama}, Nilai: {mahasiswa.nilai}")

    def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama"""
        if nama in self.daftar_nilai:
            del self.daftar_nilai[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def ubah(self, nama, nilai_baru):
        """Mengubah data mahasiswa berdasarkan nama"""
        if nama in self.daftar_nilai:
            self.daftar_nilai[nama].nilai = nilai_baru
            print(f"Data {nama} berhasil diubah.")
        else:
            print(f"Data {nama} tidak ditemukan.")
            
daftar_nilai = DaftarNilaiMahasiswa()

while True:
    print("\nMenu:")
    print("1. Tambah Data")
    print("2. Tampilkan Data")
    print("3. Hapus Data")
    print("4. Ubah Data")
    print("5. Keluar")

    pilihan = input("Pilih menu: ")

    if pilihan == "1":
        nama = input("Masukkan nama: ")
        nilai = input("Masukkan nilai: ")
        daftar_nilai.tambah(nama, nilai)
    elif pilihan == "2":
        daftar_nilai.tampilkan()
    elif pilihan == "3":
        nama = input("Masukkan nama: ")
        daftar_nilai.hapus(nama)
    elif pilihan == "4":
        nama = input("Masukkan nama: ")
        nilai_baru = input("Masukkan nilai baru: ")
        daftar_nilai.ubah(nama, nilai_baru)
    elif pilihan == "5":
        break
    else:
        print("Pilihan tidak valid.")
````

## Penjelasan Code

  1.  DaftarNilaiMahasiswa adalah kelas yang mengelola daftar mahasiswa. Kelas ini memiliki metode untuk menambah, mengubah, menghapus, dan menampilkan daftar nilai mahasiswa.

  2.  Method tambah(self, nama, nilai) Menambahkan data mahasiswa baru ke dalam daftar.

  3.  Method tampilkan(self) Menampilkan semua data mahasiswa yang tersimpan dalam daftar.

  4.  Method hapus(self, nama) Menghapus data mahasiswa berdasarkan nama.

  5.  Method ubah(self, nama, nilai_baru) Mengubah nilai mahasiswa yang sudah ada berdasarkan nama.

  6.  Metode daftar_nilai menampilkan daftar nilai semua mahasiswa

Mencetak menu dengan lima opsi yang dapat dipilih pengguna tersebut:

  1.  Tambah data: untuk menambahkan data mahasiswa baru

  2.  Tampilkan data: untuk menampilkan semua data mahasiswa yang telah dimasukkan

  3.  Hapus data: Menghapus data mahasiswa berdasarkan nama

  4.  Ubah data: Mengubah nilai mahasiswa berdasarkan nama

  5.  keluar: berhenti dari program

Dan ini diagram dari class tersebut:
![393856636-c3d0c999-5d54-4079-b140-739a2131b0f9](https://github.com/user-attachments/assets/9ca55a9a-b4f1-4a66-9733-b22eacbc8d5b)

Dan ini hasil flowchartnya:
![393856280-7f26dc9b-92e2-46ef-b97b-e0e200464a5e](https://github.com/user-attachments/assets/3b675940-9885-49e5-86f4-2e39f8b9737f)
