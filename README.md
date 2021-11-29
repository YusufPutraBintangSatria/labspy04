# Labspy04
Ini adalah latihan list

## Latihan 1

Latihan yang pertama adalah membuat list dengan menulis:
```python
list=[] 
```
(keterangan: list dapat diubah dengan nilai lainnya misal list1, atau nama lainnya)

berikut penulisan dalam python:

![1](https://user-images.githubusercontent.com/92704969/143794561-c91c8cd2-1d95-4cb0-90ae-ff36e7d4fe47.png)

dengan keterangan:
```python
list=["a", "b", "c", "d", "e"]
```
- diatas ini adalah isi list nya

```python
print("Tampilkan Element ke 3:", list[2])
```
- diatas adalah perintah untuk menampilkan elemen ke 3 dalam list, karena elemen ke 3 ada di index 2, maka didalam list pakai kurung siku[2]

```python
print("ambil Element ke 2 sampai 4:", list[1:4]) 
```
- diatas untuk perintah untuk mengambil elemn ke 2 sampai ke 4 dengan index elemen ada di index 1 sampai 4

```python
print("ambil elemen terakhir:", list[5-1])
```
- sedangkan diatas ini adalah perintah untuk mengambil elemen terakhir, karena di dalam list ada 5 elemen, maka digunakan -1 untuk mengambil elemen terakhir


### merubah elemen ke 4 dengan nilai lain
```python
list[3] = "f" 
```
- sedangkan ini untuk merubah elemen ke 4 dengan nilai F, karena elemen ke 4 ada di index 3, maka ditulis list[3]

```python
print("merubah elemen ke 4 dengan nilai lain:", list)
```
- merubah elemen ke 4 sampai terakhir

```python
list[3:] = "f", "g" 
```
- ini untuk merubah elemen ke 4 sampai terakhir dengan string "f" dan "g". maka ditulis list[3:]

```python
print("merubah elemen ke 4 sampai elemen terakhir:", list)
```
berikut hasil pemogramannya:

![2](https://user-images.githubusercontent.com/92704969/143794562-e171fdb4-99d8-48d6-9f3d-65effc0d0c93.png)


### Latihan untuk menambahkan elemen dalam list:

berikut gambar program nya:

![3](https://user-images.githubusercontent.com/92704969/143794563-390e3bee-ed8d-4a62-89c6-c9cbca28124c.png)

### tambah elemen list
```python
a=[1,2,3,4,5]
b=[6,7,8,9,10]
```
- diatas adalah untuk membuat 2 list


### Ambil 2 bagian list A ke list B

```python
b.append(a[1:3])
print("2 bagian List A dijadikan List B:", b)
```
- diatas adalah code untuk menambahkan list A kedalam list B dengan menggunakan perintah append

### tambah list b dengan string
```python
b.append("saya")
print("Tambah B dengan Sring:", b)
```
- diatas adalah untuk menambahkan list B dengan string menggunakan append

### tambah list b dengan 3 nilai
```python
print("Tambah list b dengan 3 nilai:", b+[11,12,13])
```
- diatas adalah untuk menambahkan list b dengan 3 nilai dengan menggunakan arithmatic +

### Gabungan List B dan A
```python
c=b+a
print("Gabungan list B dan A:", c)
```
- dan yang di atas ini adalah untuk menggabungkan list B dan list A, menjadi list C

Berikut hasil programnya:

![4](https://user-images.githubusercontent.com/92704969/143794565-4a4780bb-424d-456a-8b46-b9f7241dc824.png)


#Praktikum Labs 4

## Membuat list nilai Mahasiswa

- flowchart programnya adalah sebagai berikut:

![5](https://user-images.githubusercontent.com/92704969/143794566-7d2eb0a2-9391-44e7-b7e0-feee8d303114.png)

- Berikut gambar programnya:

![6](https://user-images.githubusercontent.com/92704969/143794568-90f3acb0-4896-48b8-9df4-c241fd5619a0.png)

- Keterangan:
```python
i=0
```
- diatas adalah untuk  menginisiasikan variable i sama dengan 0, karena diprogram ini akan menggunakan perulangan while dan for, jadi perlu di inisiasikan agar tidak terjadi error 

```python
nama=[]
nim=[]
tugas=[]
uts=[]
uas=[]
nilai_akhir=[]
```
- diatas adalah untuk mendefinisikan list nya, terdapat list untuk menampung nama, nim, tugas, uts, uas, dan nilai akhir

```python
while True:
    s_nama=input("Nama  : ")
    nama.append(s_nama)
    s_nim=input("NIM    : ")
    nim.append(s_nim)
    i_tugas=input("Nilai Tugas  : ")
    tugas.append(i_tugas)
    i_uts=input("Nilai UTS  : ")
    uts.append(i_uts)
    i_uas=input("Nilai UAS    : ")
    uas.append(i_uas)
```
- diatas adalah code untuk menginput isi dalam list tersebut, juga untuk menambahkan list jika sudah menginput 1 nama atau nilai dalam list, dengan menggunakan append dan menggunakan pengulangan while

```python
i_nilai_akhir=(int(i_tugas)*0.30)+(int(i_uts)*0.35)+(int(i_uas)*0.35)
nilai_akhir.append(i_nilai_akhir)
```
- diatas adalah code untuk menghitung nilai akhir dengan kondisi nilai akhir 30% dari nilai tugas, ditambah 35% dari nilai UTS dan juga 35% dari nilai UAS, dengan kemudian diubah persentase menjadi bentuk desimal, maka terdapat 0.30, 0.35. sedangkan untuk nilai_akhir.append adalah untuk menambahkan list dari yang telah di inputkan sebelum akhirnya di tampilkan

```python
more=""
   while more!="y" and more!="t":
    more=input("Tambah Data (y/t) ?")
i+=1
if more=="t":
    break
```
- sedangkan code diatas adalah untuk perintah menambahkan data dengan pertanyaan ya atau tidak, dengan definisi jika ya, maka ketikkan y pada keyboard, maka akan mengulang inputan list. dan jika tidak, ketikkan t paada keyboard, maka akan menampilkan hasil list yang telah di inputkan

```python
print("                                       Daftar Mahasiswa                               ")
print("======================================================================================")
print("|    No.    |    Nama    |   NIM    |    Tugas   |   UTS    |    UAS    |    Akhir   |")
print("======================================================================================")
```
- diatas untuk membuat border agar terlihat rapi

```python
for n in range(i):
    print("|    ",n+1,"    |    ",nama[n],"    |   ",nim[n],"    |    ",tugas[n],"   |   ",uts[n],"    |    ",uas[n],"    |    ",nilai_akhir[n],"   |")
```
- sedangkan yang diatas adalah untuk menampilkan hasil dari list yang telah di inputkan, dengan menggunakan perulangan for n in range. dan berikut hasil dari code programnya:

![7](https://user-images.githubusercontent.com/92704969/143794569-44a415f6-aa05-44b8-b347-efcadd949235.png)

## SEKIAN PRAKTIKUM LABS 4 