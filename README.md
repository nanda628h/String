# Tugas String

## Latihan 1
txt = 'Hello World'
• Hitung jumlah karakternya
• Ambil karakter terakhir
• Ambil karakter index ke-2 sampai index ke-4 (llo)
• Hilangkan spasi pada text tersebut (HelloWorld)
• Ubah text menjadi huruf besar
• Ubah text menjadi huruf kecil
• Ganti karakter H dengan karakter J

## kode program 
``` python
# Input text
txt = 'Hello World'

# Hitung jumlah karakternya
jumlah_karakter = len(txt)

# Ambil karakter terakhir
karakter_terakhir = txt[-1]

# Ambil karakter index ke-2 sampai index ke-4
karakter_2_4 = txt[2:5]

# Hilangkan spasi pada text tersebut
txt_tanpa_spasi = txt.replace(" ", "")

# Ubah text menjadi huruf besar
txt_upper = txt.upper()

# Ubah text menjadi huruf kecil
txt_lower = txt.lower()

# Ganti karakter H dengan karakter J
txt_ganti_h_j = txt.replace("H", "J")

# Cetak hasil
print("Jumlah karakter:", jumlah_karakter)
print("Karakter terakhir:", karakter_terakhir)
print("Karakter index ke-2 sampai ke-4:", karakter_2_4)
print("Teks tanpa spasi:", txt_tanpa_spasi)
print("Teks huruf besar:", txt_upper)
print("Teks huruf kecil:", txt_lower)
print("Ganti karakter 'H' dengan 'J':", txt_ganti_h_j)
```

## penjelasan kode
Kode ini melakukan serangkaian operasi pada string txt yang berisi 'Hello World'.
Menghitung Jumlah Karakter: Menggunakan fungsi len(txt) untuk menghitung panjang string, termasuk spasi. Hasilnya adalah 11.
Mengambil Karakter Terakhir: Dengan indeks -1, diambil karakter terakhir dari string, yaitu 'd'.
Mengambil Substring Tertentu: Menggunakan slicing [2:5], diambil substring dari indeks ke-2 hingga sebelum indeks ke-5, menghasilkan 'llo'.
Menghilangkan Spasi: Metode .replace(" ", "") mengganti spasi dengan string kosong, menghasilkan 'HelloWorld'.
Mengubah ke Huruf Besar dan Kecil: Metode .upper() dan .lower() mengubah semua huruf menjadi huruf besar ('HELLO WORLD') dan huruf kecil ('hello world').
Mengganti Karakter: Metode .replace("H", "J") mengganti huruf 'H' dengan 'J', menghasilkan 'Jello World'.
Mencetak Hasil: Semua hasil di atas dicetak dengan label yang sesuai untuk memudahkan pembacaan.

## output kode
``` python
Jumlah karakter: 11
Karakter terakhir: d
Karakter index ke-2 sampai ke-4: llo
Teks tanpa spasi: HelloWorld
Teks huruf besar: HELLO WORLD
Teks huruf kecil: hello world
Ganti karakter 'H' dengan 'J': Jello World
```
## Latihan 2

• Lengkapi kode berikut:
``` python
umur = 24
txt = 'Hello, nama saya john, dan umur saya adalah
... tahun'

print(txt.format(umur))
```
## hasil kode 
``` python
umur = 18
txt = 'Hello, nama saya Nanda, dan umur saya adalah {} tahun'

print(txt.format(umur))
```
## penjelasan 

Kode ini mendefinisikan sebuah variabel umur dengan nilai 18 dan sebuah string txt yang berisi teks dengan placeholder {}. Placeholder ini memungkinkan string untuk diisi dengan data dinamis. Metode .format(umur) digunakan untuk menggantikan {} pada string txt dengan nilai dari variabel umur. Ketika kode dijalankan, 
string yang sudah berisi data lengkap dicetak ke layar menggunakan fungsi print(). Output akhir dari program ini adalah:
## output 
Hello, nama saya Nanda, dan umur saya adalah 18 tahun

## Latihan 3
Studi Kasus: Validasi Form Input

Sebuah aplikasi pendaftaran online memerlukan validasi input. Anda
diminta membuat program untuk memvalidasi data berikut:
• Nama lengkap (harus hanya berisi huruf).
• Nomor telepon (harus hanya berisi angka).
• Email (harus mengandung karakter @ dan . ).
• Jika semua validasi berhasil, tampilkan pesan: Data pendaftaran
valid. Jika tidak, tampilkan pesan error untuk setiap kesalahan.

## kode program 
``` python
def validasi_form(nama, nomor_telepon, email):
    errors = []

    # Validasi nama lengkap (hanya huruf)
    if not nama.replace(" ", "").isalpha():
        errors.append("Nama lengkap harus hanya berisi huruf.")

    # Validasi nomor telepon (hanya angka)
    if not nomor_telepon.isdigit():
        errors.append("Nomor telepon harus hanya berisi angka.")

    # Validasi email (harus mengandung @ dan .)
    if "@" not in email or "." not in email:
        errors.append("Email harus mengandung karakter '@' dan '.'.")

    # Output validasi
    if not errors:
        print("Data pendaftaran valid.")
    else:
        print("Kesalahan ditemukan:")
        for error in errors:
            print(f"- {error}")


# Contoh input
nama = input("Masukkan nama lengkap: ")
nomor_telepon = input("Masukkan nomor telepon: ")
email = input("Masukkan email: ")

# Panggil fungsi validasi
validasi_form(nama, nomor_telepon, email)
```
## penjelasan kode 
Kode ini adalah fungsi Python yang digunakan untuk memvalidasi data input pengguna dalam sebuah aplikasi pendaftaran online. Fungsi validasi_form menerima tiga parameter: nama, nomor_telepon, dan email, lalu melakukan validasi dengan aturan sebagai berikut:

Validasi Nama: Nama harus hanya berisi huruf, termasuk spasi. Hal ini diperiksa dengan metode .replace(" ", "").isalpha(), yang menghapus spasi sebelum memeriksa apakah sisanya adalah huruf. Jika tidak valid, pesan kesalahan ditambahkan ke daftar errors.

Validasi Nomor Telepon: Nomor telepon harus hanya berisi angka, diperiksa dengan metode .isdigit(). Jika tidak valid, pesan kesalahan ditambahkan ke daftar errors.

Validasi Email: Email harus mengandung karakter '@' dan '.'. Jika salah satu karakter tersebut tidak ada, pesan kesalahan ditambahkan ke daftar errors.

Setelah semua validasi dilakukan:

Jika tidak ada kesalahan (errors kosong), program mencetak "Data pendaftaran valid.".
Jika ada kesalahan, setiap pesan kesalahan dalam errors dicetak satu per satu.
Program ini juga mencakup contoh input dari pengguna untuk nama, nomor_telepon, dan email, yang kemudian divalidasi dengan memanggil fungsi validasi_form.

## output
### input valid 
``` python
Masukkan nama lengkap: John Doe
Masukkan nomor telepon: 1234567890
Masukkan email: john.doe@example.com
Data pendaftaran valid.
```
### input tidak valid
``` python
Masukkan nama lengkap: John123
Masukkan nomor telepon: abc123
Masukkan email: johndoeexample.com
Kesalahan ditemukan:
- Nama lengkap harus hanya berisi huruf.
- Nomor telepon harus hanya berisi angka.
- Email harus mengandung karakter '@' dan '.'.
```



