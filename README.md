# pratikum8

# OOP (Object-Oriented Programming)
```diff
Nama  : Bayu Aji Yuwono
NIM   : 312310492
Kelas : TI.23.A.5
```
$${\color{lightblue}PYTHON}$$

## Program Class Data_Mahasiswa
* *Diagram Class*
* <img src="Diagram/ss Diagram (2).png">
* *Flowchart*
<img src="flowchart/ss flowchart.png">

### *Penjelasan dan kode Programnya*   
Program kita kali ini akan menggunakan sistem OOP(Object-Oriented Programming), apa itu OOP?
OOP(Object-Oriented Programming) merupakan sebuah cara untuk membangun sebuah aplikasi dengan memandang sebagai presentasi objek-objek yang saling mendukung serta berinteraksi dari satu objek ke objek yang lainnya, dan dapat dikatakan code program akan terbentuk berkelompok berdasarkan objek. 
Fungsi secara singkat yakni meringkas sebuah program yang berulang-ulang dengan menggunakan syntaks def nama_fungsi(argument). def diartikan sebagai definisi.
1. Kita akan mendeklarasikan atau menginput sebuah variabel bertipe data dictionary kosong data={} yang nantinya akan kita inputkan sebuah data yang terdiri dari: nama, nim, nilai_tugas, nilai_uts, nilai_uas dan nilai_akhir.
2. kita membuat class `data_mahasiswa()`
3. Membuat fungsi
    * Fungsi tambah(), untuk menambahkan data def tambah()
    * Fungsi tampilkan(), untuk menampilkan data def tampilkan()
    * Fungsi hapus(nama), untuk menghapus nama pada data def hapus(nama)
    * Fungsi ubah(nama), untuk mengubah nama pada data def ubah(nama)
    * Fungsi salah(), untuk inputan yang tidak sesuai perintah def salah()
4. Menggunakan Perulangan while (while loop)
while True:, dapat diartikan perulangan akan terus mengulang jika inputan benar dan masuk kedalam proses jika tidak maka perulangan berhenti atau lanjut ke proses selanjutnya. 
variabel lanjut kita gunakan untuk menginput perintah yang akan kita proses lanjut=input(str('(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar)), disini kita menggunakan statement if untuk memproses perintah yang di inginkan sesuai inputan pada variabel lanjut:
    * if lanjut.lower() == 'l':

        if data.items():

        tampilkan()

        else:

        salah()

    * if lanjut.lower() == 't':

        tambah()

    * if lanjut.lower() == 'h':

        nama = input(str('Nama\t: '))

        if nama in data.items():

        hapus(nama)

        else:

        salah()

    * if lanjut.lower == 'u':

        nama = input(str('Nama\t: '))

        if nama in data.items():

        ubah(nama)

        else:

        salah()
* *Kode Program*  
python 
data={} 
import os
class data_mahasiswa():
    def tambah():
        print(f"{'Tambah Data':^17}")
        print('='*17)
        nim = str(input('NIM\t\t: '))
        nama = str(input('Nama\t\t: '))
        uts = int(input('Nilai UTS\t: '))
        uas = int(input('Nilai UAS\t: '))
        tugas = int(input('Nilai Tugas\t: '))
        akhir = round(float((tugas*0.3)+(uts*0.35)+(uas*0.35)),2)
        data[nama]=nim, uts, uas, tugas, akhir
    def tampilkan():
        print(f"{'Daftar Data Mahasiswa':^82}")
        print('='*84)
        print(f"|{'NO':^4}|{'NIM':^20}|{'NAMA':^20}|{'TUGAS':^10}|{'UTS':^6}|{'UAS':^6}|{'AKHIR':^10}|")
        print('='*84)
        n = 0
        for a in data.items():
            n += 1
            print("|{no:^4}|{0:^20}|{1:^20}|{2:^10}|{3:^6}|{4:^6}|{5:^10}|"
            .format(a[1][0], a[0][:13], a[1][1], a[1][2], a[1][3], a[1][4], no = n))
        print('='*84)

    def hapus(nama):
        print(f"{'Data Berhasil di Hapus':^17}")
        print('='*17)
        del data[nama]

    def ubah(nama):
        print(f"{'Ubah Data':^17}")
        print('='*17)
        nim = str(input('NIM\t\t: ')) 
        uts = int(input('Nilai UTS\t: '))
        uas = int(input('Nilai UAS\t: '))
        tugas = int(input('Nilai Tugas\t: '))
        akhir = round(float((tugas*0.3)+(uts*0.35)+(uas*0.35)),2)
        data[nama] = nim, uts, uas, tugas, akhir

    def salah():
        print(f"{'Daftar Data Mahasiswa':^82}")
        print('='*84)
        print(f"|{'NO':^4}|{'NIM':^20}|{'NAMA':^20}|{'TUGAS':^10}|{'UTS':^6}|{'UAS':^6}|{'AKHIR':^10}|")
        print('='*84)
        print(F"|{'Tidak ada data':^82}|")
        print('='*84)
while True:
    print()
    lanjut = str(input('MENU\n=======\n(L)ihat\n(T)ambah\n(U)bah\n(H)apus\n(K)eluar\n=======\nPilihan : '))
    os.system("cls")
    if lanjut.lower() == 'l':
        if data.items():
            data_mahasiswa.tampilkan()
        else:
            data_mahasiswa.salah()
    elif lanjut.lower() == 't':
            data_mahasiswa.tambah()
    elif lanjut.lower() == 'h':
        print('Data yang ingin di hapus')
        nama = str(input('Nama\t\t: '))
        if nama in data.keys():
            data_mahasiswa.hapus(nama)
        else:
            data_mahasiswa.salah()
    elif lanjut.lower() == 'u':
        print('Data yang ingin di ubah')
        nama = str(input('Nama\t\t: '))
        if nama in data.keys():
            data_mahasiswa.ubah(nama)
        else:
            data_mahasiswa.salah()
    elif lanjut.lower() == 'k':
        break
    else :
        print('Pilih menu yang tersedia')
print('Program Selesai') 

* *Hasil Program*
    * Inputan 'T' untuk Menambahkan Data   
  <img src="Gambar/SS 1.png">
   
    * Inputan 'U' untuk Mengubah Data  
      <img src="Gambar/SS 2.png">

    * Inputan 'H' untuk Menghapus Data  
      <img src="Gambar/SS 3.png">

    * Inputan 'L' untuk Melihat Data  
      <img src="Gambar/SS 4.png">

    * Tampilan Data Sesudah Di Hapus

     <img src="Gambar/SS 5.png">

    * Inputan 'K' untuk Keluar dari program  
  <img src="Gambar/SS 6.png">

    * Inputan selain 'T', 'L', 'U', 'H', dan 'K'    
      <img src="Gambar/SS 7.png">
