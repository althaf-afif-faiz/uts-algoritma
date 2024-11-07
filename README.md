# uts-algoritma
# project kasir
### NAMA : Althaf Afif Faiz
### NIM : 312410404 
### KELAS : TI.24.A.3

# Penjelasan mengenai project kasir ini
Mempunyai fitur pada kasir seperti :

a. Menambah barang ke dalam keranjang.

b. Menampilkan daftar barang.

c. Menghitung total harga.

d. Mencetak struk.

# Code Codingan Project Kasir 
```
class Barang:
    def __init__(self, nama_barang, harga_satuan, jumlah):
        self.nama_barang = nama_barang
        self.harga_satuan = harga_satuan
        self.jumlah = jumlah

    def total_harga(self):
        return self.harga_satuan * self.jumlah


class Keranjang:
    def __init__(self):
        self.daftar_barang = []

    def tambah_barang(self, barang):
        self.daftar_barang.append(barang)

    def tampilkan_barang(self):
        print("Daftar Barang dalam Keranjang:")
        for barang in self.daftar_barang:
            print(f"Nama: {barang.nama_barang}, Harga: {barang.harga_satuan}, Jumlah: {barang.jumlah}, Total: {barang.total_harga()}")

    def hitung_total_harga(self):
        total = sum(barang.total_harga() for barang in self.daftar_barang)
        return total

    def cetak_struk(self):
        print("\n===Struk Belanja===")
        self.tampilkan_barang()
        total_harga = self.hitung_total_harga()
        print(f"Total Harga: {total_harga}")
        print("Terimakasih Sudah Belanja di Toko Afif Serba Ada")


# Contoh penggunaan
if __name__ == "__main__":
    keranjang = Keranjang()

    # Menambah barang ke dalam keranjang
    keranjang.tambah_barang(Barang("Ice Cream", 12700, 7))
    keranjang.tambah_barang(Barang("Susu", 64300, 3))
    keranjang.tambah_barang(Barang("Permen", 5000, 12))

    # Menampilkan daftar barang
    keranjang.tampilkan_barang()

    # Menghitung total harga
    total_harga = keranjang.hitung_total_harga()
    print(f"Total Harga: {total_harga}")

    # Mencetak struk
    keranjang.cetak_struk()
```

# Contoh Hasil Dari Codingan Project
![hasil code program kasir](https://github.com/user-attachments/assets/3680c1ec-9832-462c-a046-c313e9371731)


# Penjelasan Singkat Mengenai Algoritma Pada Project Kasir 

- Membuat kelas Barang: Kelas Barang menyimpan data tentang barang, termasuk nama, harga satuan, dan jumlah.

- Membuat kelas Keranjang: Kelas Keranjang menyimpan daftar barang yang dibeli dan menyediakan fungsi untuk menambah barang, menampilkan barang, menghitung total harga, dan mencetak struk.

- Menambahkan barang ke keranjang: Program meminta pengguna untuk memasukkan nama barang, harga satuan, dan jumlah, lalu membuat objek Barang baru dengan data tersebut dan menambahkannya ke dalam keranjang.

- Menampilkan daftar barang: Program menampilkan daftar barang yang ada di keranjang, termasuk nama, harga satuan, jumlah, dan total harga per barang.

- Menghitung total harga: Program menghitung total harga semua barang di keranjang.

- Mencetak struk: Program mencetak struk yang berisi daftar barang, total harga, dan ucapan terima kasih.
