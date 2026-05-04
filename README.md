# Tugas_Program_Tranformasi_Linier
# Program Pencerminan Matriks Transformasi Linier Geometri

## Ini untuk Linknya Colabnya:
```
https://colab.research.google.com/drive/1tgSiLGWjkeHoRxmt72VDI32XcXf6hzGq?usp=sharing
```
## Penjelasan Program

Program ini merupakan simulasi sederhana tentang **Transformasi Linier Geometri** menggunakan Python dan Matplotlib.

Program menampilkan:

- Dua matriks berbentuk 2x2
- Matriks bergerak pada bidang koordinat
- Matriks bergerak dari kiri dan kanan
- Kedua matriks berhenti di titik tertentu
- Grafik menggunakan sumbu X dan Y dari -10 sampai 10

---

# Import Library

```python
import matplotlib.pyplot as plt
import numpy as np
from matplotlib.patches import Rectangle
```

### Fungsi Library

| Library | Fungsi |
|---|---|
| matplotlib.pyplot | Membuat grafik dan animasi |
| numpy | Perhitungan numerik |
| Rectangle | Membuat kotak matriks |

---

# Posisi Awal Matriks

```python
x1_awal = -9
y1_awal = 0

x2_awal = 7
y2_awal = 0
```

### Penjelasan

- Matriks pertama berada di sebelah kiri
- Matriks kedua berada di sebelah kanan
- Posisi menggunakan koordinat Cartesian

---

# Titik Tujuan Matriks

```python
tujuan1_x = -1
tujuan1_y = 0

tujuan2_x = 1
tujuan2_y = 0
```

### Penjelasan

- Kedua matriks bergerak menuju tengah
- Matriks kiri berhenti di `(-1,0)`
- Matriks kanan berhenti di `(1,0)`

---

# Fungsi Menggambar Matriks

```python
def gambar_matriks(x, y):
```

Fungsi ini digunakan untuk:

- Membuat matriks 2x2
- Membuat kotak garis
- Mengosongkan isi matriks

---

# Membuat Kotak Matriks

```python
kotak = Rectangle(
    (x + j, y - i),
    ukuran,
    ukuran,
    fill=False,
    linewidth=2
)
```

### Penjelasan

- `Rectangle()` digunakan untuk membuat kotak
- `fill=False` membuat isi kotak kosong
- `linewidth=2` mengatur ketebalan garis

---

# Animasi Pergerakan

```python
for t in np.linspace(0, 1, 60):
```

### Penjelasan

Animasi dibagi menjadi:

- 60 langkah pergerakan
- Nilai `t` bergerak dari 0 sampai 1

---

# Rumus Pergerakan Matriks

```python
x1 = x1_awal + (tujuan1_x - x1_awal) * t
```

### Penjelasan

Rumus ini digunakan agar matriks bergerak perlahan menuju titik tujuan.

### Cara Kerja

| Nilai t | Hasil |
|---|---|
| t = 0 | Posisi awal |
| t = 1 | Posisi tujuan |

---

# Grafik Koordinat

```python
plt.xlim(-10, 10)
plt.ylim(-10, 10)
```

### Penjelasan

Digunakan untuk:

- Membuat sumbu X dari -10 sampai 10
- Membuat sumbu Y dari -10 sampai 10

---

# Hubungan Dengan Transformasi Linier Geometri

Program ini berhubungan dengan **Transformasi Linier Geometri** karena objek matriks mengalami perubahan posisi pada bidang koordinat.

Transformasi geometri adalah perubahan:

- posisi
- arah
- ukuran
- bentuk

objek matematika pada bidang koordinat.

---

# Transformasi Yang Digunakan

## 1. Translasi (Perpindahan)

```python
x1 = x1_awal + (tujuan1_x - x1_awal) * t
```

### Penjelasan

Matriks berpindah dari:

- titik awal
- menuju titik tujuan

tanpa mengubah bentuk matriks.

### Kesimpulan

Ini disebut:

# Transformasi Translasi

karena objek hanya bergeser posisi.

---

## 2. Refleksi / Pencerminan

### Penjelasan

Konsep pencerminan terlihat dari:

- satu matriks berada di kiri
- satu matriks berada di kanan
- bergerak saling mendekati secara simetris

Contoh posisi:

| Matriks | Posisi |
|---|---|
| Kiri | (-9,0) |
| Kanan | (7,0) |

### Kesimpulan

Hal ini menyerupai:

# Refleksi terhadap sumbu Y

---

## 3. Bidang Kartesius

Program menggunakan:

- sumbu X
- sumbu Y
- titik koordinat

yang merupakan dasar geometri transformasi.

---

# Kesimpulan Akhir

Program ini menunjukkan:

- dua matriks 2x2 sebagai objek geometri
- bergerak pada bidang koordinat
- menggunakan translasi
- menggunakan konsep refleksi/pencerminan

Sehingga program termasuk penerapan:

# Transformasi Linier Geometri

karena terjadi perubahan posisi objek matematis pada bidang koordinat menggunakan operasi matematika.
