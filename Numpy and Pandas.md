# Bab 2: Pendahuluan NumPy dan Pandas

## 📘 NumPy
NumPy (Numerical Python) adalah library Python yang digunakan untuk komputasi numerik dan manipulasi array. Library ini dirancang untuk mempermudah pengolahan data dalam bentuk array multidimensi dengan performa tinggi.

### Kelebihan NumPy
- Performa lebih cepat dibandingkan list Python untuk komputasi matematis.
- Mendukung operasi vektor dan matriks secara efisien.
- Memiliki berbagai fungsi siap pakai untuk analisis numerik.

### 🔗 Fungsi-Fungsi Populer NumPy:
Berikut adalah fungsi-fungsi yang sering digunakan di NumPy:
1. **`numpy.array()`**: Membuat array.
   ```python
   import numpy as np
   
   array = np.array([1, 2, 3])
   print(array)  # Output: [1 2 3]
   ```

2. **`numpy.arange()`**: Membuat array dengan rentang nilai tertentu.
   ```python
   array = np.arange(5)  # Output: [0 1 2 3 4]
   ```

3. **`numpy.zeros()`**: Membuat array dengan nilai nol.
   ```python
   array = np.zeros(3)  # Output: [0. 0. 0.]
   ```

4. **`numpy.ones()`**: Membuat array dengan nilai satu.
   ```python
   array = np.ones(3)  # Output: [1. 1. 1.]
   ```

5. **`numpy.reshape()`**: Mengubah bentuk array.
   ```python
   array = np.array([1, 2, 3, 4])
   reshaped = array.reshape(2, 2)  # Output: [[1 2] [3 4]]
   ```

6. **`numpy.sum()`**: Menjumlahkan elemen array.
   ```python
   array = np.array([1, 2, 3])
   total = np.sum(array)  # Output: 6
   ```

7. **`numpy.mean()`**: Menghitung rata-rata array.
   ```python
   array = np.array([1, 2, 3, 4])
   mean = np.mean(array)  # Output: 2.5
   ```

8. **`numpy.max()`**: Mencari nilai maksimum.
   ```python
   array = np.array([1, 2, 3, 4])
   maximum = np.max(array)  # Output: 4
   ```

9. **`numpy.min()`**: Mencari nilai minimum.
   ```python
   array = np.array([1, 2, 3, 4])
   minimum = np.min(array)  # Output: 1
   ```

10. **`numpy.dot()`**: Melakukan perkalian matriks (dot product).
    ```python
    A = np.array([[1, 2], [3, 4]])
    B = np.array([[5, 6], [7, 8]])
    result = np.dot(A, B)  # Output: [[19 22] [43 50]]
    ```

### Langkah Awal Menggunakan NumPy
#### 1. Import NumPy
```python
import numpy as np
```

#### 2. Membuat Array
- **Array 1D (vektor):**
  ```python
  vector = np.array([1, 2, 3])
  print(vector)  # Output: [1 2 3]
  ```

- **Array 2D (matriks):**
  ```python
  matrix = np.array([[1, 2], [3, 4]])
  print(matrix)
  # Output:
  # [[1 2]
  #  [3 4]]
  ```

#### 3. Operasi Aritmatika dan Logika

NumPy mendukung operasi matematis langsung pada array:

- **Perkalian Skalar**:
  ```python
  array = np.array([1, 2, 3])
  result = array * 2  # Perkalian skalar
  print(result)  # Output: [2 4 6]
  ```

- **Penjumlahan Elemen**:
  ```python
  array1 = np.array([1, 2, 3])
  array2 = np.array([4, 5, 6])
  result = array1 + array2  # Penjumlahan elemen
  print(result)  # Output: [5 7 9]
  ```

- **Operasi Logika**:
  ```python
  array = np.array([1, 2, 3])
  logical = array > 1  # Operasi logika
  print(logical)  # Output: [False  True  True]
  ```

- **Pengurangan Elemen**:
  ```python
  array1 = np.array([10, 20, 30])
  array2 = np.array([1, 5, 10])
  result = array1 - array2  # Pengurangan elemen
  print(result)  # Output: [ 9 15 20]
  ```

- **Perkalian Matriks**:
  ```python
  matrix1 = np.array([[1, 2], [3, 4]])
  matrix2 = np.array([[5, 6], [7, 8]])
  result = np.dot(matrix1, matrix2)  # Perkalian matriks
  print(result)
  # Output:
  # [[19 22]
  #  [43 50]]
  ```

#### 4. Indexing dan Slicing
Untuk mengambil atau mengubah elemen array:
```python
array = np.array([10, 20, 30, 40, 50])
print(array[1])     # Output: 20
print(array[1:4])   # Output: [20 30 40]

# Mengubah elemen
array[1:4] = 99
print(array)        # Output: [10 99 99 99 50]
```

#### 4. Indexing dan Slicing
Untuk mengambil atau mengubah elemen array:
```python
array = np.array([10, 20, 30, 40, 50])
print(array[1])     # Output: 20
print(array[1:4])   # Output: [20 30 40]

# Mengubah elemen
array[1:4] = 99
print(array)        # Output: [10 99 99 99 50]
```

---

## 📘 Pandas
Pandas adalah library Python yang digunakan untuk analisis dan manipulasi data, terutama data tabular (berbentuk tabel).

### Apa itu DataFrame dan Series?
- **DataFrame**: Struktur data dua dimensi (baris dan kolom).
- **Series**: Struktur data satu dimensi (mirip dengan array).

```python
import pandas as pd

# Membuat DataFrame
data = {'Nama': ['Alice', 'Bob'], 'Umur': [25, 30]}
df = pd.DataFrame(data)
print(df)
# Output:
#     Nama  Umur
# 0  Alice    25
# 1    Bob    30

# Membuat Series
s = pd.Series([1, 2, 3])
print(s)
# Output:
# 0    1
# 1    2
# 2    3
# dtype: int64
```

### 🔗 Fungsi-Fungsi Populer Pandas:
1. **`pd.read_csv()`**: Membaca file CSV.
   ```python
   import pandas as pd

   data = pd.read_csv('file.csv')
   print(data.head())
   ```

2. **`df.head()`**: Menampilkan beberapa baris awal DataFrame.
   ```python
   print(df.head())
   # Output:
   #     Nama  Umur
   # 0  Alice    25
   # 1    Bob    30
   ```

3. **`df.describe()`**: Memberikan ringkasan statistik DataFrame.
   ```python
   print(df.describe())
   # Output:
   #        Umur
   # count    2.0
   # mean   27.5
   # std     3.5
   # min    25.0
   # 25%    26.25
   # 50%    27.50
   # 75%    28.75
   # max    30.0
   ```

4. **`df.loc[]`**: Mengakses data berdasarkan label.
   ```python
   print(df.loc[0])  # Mengambil baris pertama
   # Output:
   # Nama    Alice
   # Umur       25
   # Name: 0, dtype: object
   ```

5. **`df.iloc[]`**: Mengakses data berdasarkan indeks.
   ```python
   print(df.iloc[1])  # Mengambil baris kedua
   # Output:
   # Nama    Bob
   # Umur      30
   # Name: 1, dtype: object
   ```

6. **`df.drop()`**: Menghapus kolom atau baris.
   ```python
   df = df.drop('Kota', axis=1)  # Menghapus kolom
   print(df)

   df = df.drop(0, axis=0)  # Menghapus baris pertama
   print(df)
   ```

7. **`df.append()`**: Menambahkan data baru.
   ```python
   new_data = {'Nama': ['Charlie'], 'Umur': [28]}
   df = df.append(new_data, ignore_index=True)
   print(df)
   # Output:
   #     Nama  Umur
   # 0  Alice    25
   # 1    Bob    30
   # 2  Charlie  28
   ```

8. **`df.merge()`**: Menggabungkan dua DataFrame.
   ```python
   df1 = pd.DataFrame({'Key': ['A', 'B', 'C'], 'Value': [1, 2, 3]})
   df2 = pd.DataFrame({'Key': ['A', 'B', 'D'], 'Value': [4, 5, 6]})
   merged = pd.merge(df1, df2, on='Key')
   print(merged)
   # Output:
   #   Key  Value_x  Value_y
   # 0    A        1        4
   # 1    B        2        5
   ```

9. **`df.groupby()`**: Mengelompokkan data berdasarkan kolom tertentu.
   ```python
   grouped = df.groupby('Nama').mean()
   print(grouped)
   # Output:
   #        Umur
   # Nama        
   # Alice    25.0
   # Bob      30.0
   ```

10. **`df.isnull()`**: Mengecek nilai kosong.
    ```python
    print(df.isnull())
    # Output:
    #       Nama   Umur
    # 0  False  False
    # 1  False  False
    # 2  False  False
    ```

---

Gunakan Pandas dan NumPy untuk membuat analisis data lebih cepat dan efisien! 🚀
