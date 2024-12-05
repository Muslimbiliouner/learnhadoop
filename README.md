### README.md

# Word Count UUD 1945 dengan MapReduce

Proyek ini bertujuan untuk menghitung jumlah kemunculan setiap kata dalam dokumen teks file yang disimpan dengan nama pembukaan_uud1945.txt menggunakan konsep **MapReduce with Python**. Proyek ini mencakup dua skrip Python utama:

1. `mapper.py` - Bertugas membaca input dan memetakan setiap kata dengan nilai awal `1`.
2. `reducer.py` - Menggabungkan hasil dari mapper untuk menghitung total kemunculan setiap kata.

## File Proyek
- `mapper.py`: Mapper script untuk memproses input baris demi baris dan menghasilkan pasangan `kata\t1`.
- `reducer.py`: Reducer script untuk menggabungkan hasil dari mapper dan menghitung jumlah total kata.
- `pembukaan_uud1945.txt`: File input teks yang digunakan dalam contoh ini.
- `README.md`: Dokumentasi proyek (file ini).

## Prasyarat
- Python 3.x terinstal di sistem Anda.
- Perintah `cat`, `sort`, dan sistem Hadoop untuk menjalankan pipeline.

Notes : Jika menggunakan google collab bisa langsung running script berurutan

## Cara Kerja
### Alur Proses
1. **Mapper**: Memetakan setiap kata dengan nilai `1`.
2. **Sort**: Mengurutkan output mapper berdasarkan kata (key).
3. **Reducer**: Menggabungkan jumlah kata berdasarkan key.

### Ilustrasi
Input:
```plaintext
ini adalah contoh teks ini adalah contoh
```

Output Mapper:
```plaintext
ini    1
adalah 1
contoh 1
teks   1
ini    1
adalah 1
contoh 1
```

Output Reducer:
```plaintext
adalah 2
contoh 2
ini    2
teks   1
```

## Cara Menggunakan

1. **Jika menggunakan google collab pertama upload file pembukaan_uud1945.txt** 

2. **Running seluruh script berurutan**  
  
## Struktur File
```.

├── mapper.py          # Skrip mapper
├── reducer.py         # Skrip reducer
├── pembukaan_uud1945.txt # Contoh file input
├── README.md          # Dokumentasi proyek
```

## Catatan
- Pastikan file `mapper.py` dan `reducer.py` bersifat executable:
  ```bash
  chmod +x mapper.py reducer.py
    ```
    
## Referensi
- **Apache Hadoop Streaming Documentation**: [Hadoop Streaming](https://hadoop.apache.org/docs/current/hadoop-streaming/HadoopStreaming.html)
- **Python Official Documentation**: [Python Docs](https://docs.python.org/3/)
```