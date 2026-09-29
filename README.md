# Pertemuan 05 Perulangan Python
Nama: Vanisya Nur Khalimah  
NIM: 2225520201  
Kelas: S1 Pendidikan Matematika FKIP Untirta  

## Tujuan
Menggunakan perulangan `for` dan `while` untuk menyelesaikan masalah iteratif, khususnya pada kasus deret aritmetika.

## Cara Menjalankan
```bash
python3 kuis/kuis2_deret_aritmetika.py

# Algoritma Kuis 2

# 1. Menerima input suku pertama (a), beda (d), dan jumlah suku (n).
a = int(input("Masukkan suku pertama (a): "))
d = int(input("Masukkan beda (d): "))
n = int(input("Masukkan jumlah suku (n): "))

# 2. Menggunakan perulangan for untuk menampilkan deret aritmetika dan menghitung jumlahnya.
print("\n=== Menggunakan for loop ===")
jumlah_for = 0
for i in range(n):
    suku = a + i * d
    print(suku, end=" ")
    jumlah_for += suku
print(f"\nJumlah deret (for) = {jumlah_for}")

# 3. Menggunakan perulangan while sebagai alternatif untuk menampilkan deret aritmetika.
print("\n=== Menggunakan while loop ===")
jumlah_while = 0
i = 0
while i < n:
    suku = a + i * d
    print(suku, end=" ")
    jumlah_while += suku
    i += 1
print(f"\nJumlah deret (while) = {jumlah_while}")

# Hasil Pengujian (dengan kode)
def uji_coba(a, d, n, expected_sum):
    jumlah = sum([a + i * d for i in range(n)])
    print(f"Input: a={a}, d={d}, n={n}")
    print(f"Deret: {[a + i * d for i in range(n)]}")
    print(f"Jumlah aktual = {jumlah}")
    print(f"Jumlah yang diharapkan = {expected_sum}")
    print("Status:", "Sesuai" if jumlah == expected_sum else "Tidak sesuai")
    print("-" * 40)

# Contoh pengujian
uji_coba(2, 3, 5, 40)   # Deret: 2, 5, 8, 11, 14 → Jumlah = 40
uji_coba(1, 2, 4, 16)   # Deret: 1, 3, 5, 7 → Jumlah = 16

# Refleksi (dengan kode)
# ==============================

print("\n=== Refleksi Kesalahan Perulangan ===")

# Contoh kesalahan: while loop tanpa kondisi penghentian
# (JANGAN dijalankan terlalu lama, karena akan looping terus)
# i = 0
# while i < 5:
#     print("Looping tanpa i bertambah")  # i tidak pernah bertambah → infinite loop

print("Contoh kesalahan: while loop tanpa i bertambah → infinite loop")

# Perbaikan: tambahkan variabel penghitung i yang bertambah setiap iterasi
i = 0
while i < 5:
    print(f"Iterasi ke-{i+1}")
    i += 1

print("Perbaikan: while loop berhenti setelah 5 iterasi")
