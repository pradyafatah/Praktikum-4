Berikut adalah penjelasan yang bisa Anda tulis dalam file `README.md` di GitHub untuk menjelaskan program ini secara mendetail:

---

# Program Sederhana untuk Menambah Data Mahasiswa dan Menghitung Nilai Akhir

## Deskripsi Program
Program ini adalah aplikasi sederhana yang meminta pengguna memasukkan data mahasiswa, menghitung nilai akhir berdasarkan tiga komponen nilai (tugas, UTS, dan UAS), lalu menampilkan daftar data mahasiswa dalam bentuk tabel. Program ini dibuat menggunakan bahasa pemrograman Python.

## Fitur Program
1. **Input Data Mahasiswa**: Pengguna dapat memasukkan nama, NIM, nilai tugas, nilai UTS, dan nilai UAS mahasiswa.
2. **Menghitung Nilai Akhir**: Program akan menghitung nilai akhir setiap mahasiswa berdasarkan bobot:
   - Tugas: 30%
   - UTS: 35%
   - UAS: 35%
3. **Pengulangan Input Data**: Program memungkinkan pengguna untuk menambahkan data mahasiswa sebanyak yang diinginkan.
4. **Tampilan Data dalam Bentuk Tabel**: Setelah selesai memasukkan data, program menampilkan daftar data mahasiswa dalam format tabel.

## Cara Kerja Program
1. **Memasukkan Data**: Pengguna diminta untuk menginput data mahasiswa satu per satu. Setiap mahasiswa memiliki informasi berupa:
   - `Nama`
   - `NIM`
   - `Nilai Tugas`
   - `Nilai UTS`
   - `Nilai UAS`
   
2. **Perhitungan Nilai Akhir**: Program menghitung nilai akhir untuk setiap mahasiswa dengan formula berikut:
   \[
   \text{Nilai Akhir} = (0.3 \times \text{Nilai Tugas}) + (0.35 \times \text{Nilai UTS}) + (0.35 \times \text{Nilai UAS})
   \]

3. **Pengulangan**: Setelah memasukkan data satu mahasiswa, program menanyakan kepada pengguna apakah ingin menambah data mahasiswa lain. Jika pengguna menjawab `y` atau `Y`, program akan meminta input data lagi. Jika pengguna menjawab `t` atau `T`, program akan menampilkan daftar data mahasiswa yang sudah dimasukkan.

4. **Menampilkan Tabel**: Ketika pengguna selesai memasukkan data, program menampilkan seluruh data mahasiswa dalam bentuk tabel yang rapi, dengan kolom-kolom sebagai berikut:
   - Nomor urut
   - Nama
   - NIM
   - Nilai Tugas
   - Nilai UTS
   - Nilai UAS
   - Nilai Akhir

## Struktur Kode
Berikut adalah struktur dari kode program:

```python
# List untuk menyimpan data mahasiswa
data_mahasiswa = []

while True:
    # Input data mahasiswa
    nama = input("Nama: ")
    nim = input("NIM: ")
    nilai_tugas = float(input("Nilai Tugas: "))
    nilai_uts = float(input("Nilai UTS: "))
    nilai_uas = float(input("Nilai UAS: "))
    
    # Menghitung nilai akhir
    nilai_akhir = (0.3 * nilai_tugas) + (0.35 * nilai_uts) + (0.35 * nilai_uas)
    
    # Menyimpan data ke dalam list
    data_mahasiswa.append({
        "nama": nama,
        "nim": nim,
        "tugas": nilai_tugas,
        "uts": nilai_uts,
        "uas": nilai_uas,
        "akhir": nilai_akhir
    })
    
    # Pertanyaan untuk menambah data
    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() != 'y':
        break

# Menampilkan data dalam format tabel
print("=" * 50)
print("| No | Nama       | NIM    | Tugas | UTS  | UAS  | Akhir |")
print("=" * 50)
for i, mhs in enumerate(data_mahasiswa, 1):
    print(f"| {i:2} | {mhs['nama']:<10} | {mhs['nim']:<6} | {mhs['tugas']:5.2f} | {mhs['uts']:4.2f} | {mhs['uas']:4.2f} | {mhs['akhir']:6.2f} |")
print("=" * 50)
```

## Contoh Tampilan Program
Berikut adalah contoh tampilan interaksi program:

```
Nama : Ari
NIM : 1234
Nilai Tugas : 70
Nilai UTS : 65
Nilai UAS : 80
Tambah data(y/t)? y

Nama : Bambang
NIM : 2345
Nilai Tugas : 65
Nilai UTS : 80
Nilai UAS : 90
Tambah data(y/t)? t

==================================================
| No | Nama       | NIM    | Tugas | UTS  | UAS  | Akhir |
==================================================
|  1 | Ari        | 1234   |  70.00 | 65.00 | 80.00 | 71.75 |
|  2 | Bambang    | 2345   |  65.00 | 80.00 | 90.00 | 79.00 |
==================================================
```

## Flowchart
Flowchart berikut menggambarkan proses kerja program ini:

1. **Mulai**
2. **Input Data Mahasiswa**
   - Meminta `Nama`
   - Meminta `NIM`
   - Meminta `Nilai Tugas`
   - Meminta `Nilai UTS`
   - Meminta `Nilai UAS`
3. **Hitung Nilai Akhir**:
   \[
   \text{Nilai Akhir} = (0.3 \times \text{Nilai Tugas}) + (0.35 \times \text{Nilai UTS}) + (0.35 \times \text{Nilai UAS})
   \]
4. **Tambah Data ke List**
5. **Tanyakan Apakah Ingin Menambah Data Lagi?**
   - Jika `Ya`: Kembali ke langkah 2
   - Jika `Tidak`: Lanjutkan ke langkah berikutnya
6. **Tampilkan Data dalam Tabel**
7. **Selesai**

## Cara Menjalankan Program
1. Pastikan Anda memiliki Python terinstal di komputer Anda.
2. Buka terminal atau command prompt.
3. Jalankan program dengan perintah berikut:
   ```bash
   python nama_file.py
   ```
4. Ikuti instruksi pada layar untuk memasukkan data mahasiswa.

## Cara Menggunakan Repository
1. Clone repository ini ke komputer Anda dengan perintah:
   ```bash
   git clone <URL-repo-anda>
   ```
2. Buka folder repository yang sudah diclone.
3. Edit program jika perlu.
4. Commit perubahan Anda:
   ```bash
   git add .
   git commit -m "Menambahkan program input data mahasiswa"
   ```
5. Push ke repository GitHub:
   ```bash
   git push origin main
   ```

---

Dengan penjelasan ini, orang lain dapat memahami cara kerja program, menjalankannya, dan menavigasi kode serta alur logikanya dengan lebih mudah.
