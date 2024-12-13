# 📘 Bab 1: Introduction to Python

## Apa itu Python?
Python adalah bahasa pemrograman yang sederhana, mudah dipelajari, dan populer. Python dirancang untuk berbagai kebutuhan, mulai dari pengembangan web, analisis data, hingga kecerdasan buatan.

**Fitur utama Python:**
- Mudah dipahami dengan sintaks sederhana.
- Komunitas yang besar dan banyak dokumentasi.
- Mendukung berbagai library untuk mempercepat pengembangan.

## Kenapa Python untuk Data Science?
Python menjadi pilihan utama untuk data science karena:
- **Ekosistem library yang lengkap**, seperti pandas, numpy, dan matplotlib.
- **Kemudahan integrasi** dengan teknologi lainnya.
- **Kinerja optimal** untuk komputasi skala besar dengan dukungan komunitas yang terus berkembang.

## Library Python untuk Data Science
Berikut adalah beberapa library populer yang sering digunakan:

- **pandas**: Untuk manipulasi dan analisis data.
- **numpy**: Untuk operasi matematis dan array multidimensi.
- **matplotlib**: Untuk visualisasi data.
- **seaborn**: Untuk visualisasi data yang lebih estetik.
- **scikit-learn**: Untuk machine learning.
- **tensorflow**: Untuk deep learning dan AI.

## Tipe Data di Python

1. **Integers**: Angka bulat, contohnya `1`, `42`, `-10`.
2. **Floating-point numbers**: Angka desimal, contohnya `3.14`, `0.5`.
3. **String**: Teks, contohnya `'Hello World'`, `"Python"`.
4. **Boolean**: Nilai logika, yaitu `True` atau `False`.

### Contoh:
```python
x = 10            # Integer
pi = 3.14         # Float
name = "Python"   # String
is_active = True  # Boolean
```

## Variable Assignment
Variabel adalah tempat untuk menyimpan data. Anda dapat memberikan nilai ke variabel menggunakan tanda `=`.

### Contoh:
```python
age = 25
height = 5.9
language = "Python"
```

## Operator Aritmatika dan Perbandingan

### Operator Aritmatika
| Operator | Fungsi        | Contoh      |
|----------|---------------|-------------|
| `+`      | Penjumlahan   | `5 + 3 = 8` |
| `-`      | Pengurangan   | `7 - 2 = 5` |
| `*`      | Perkalian     | `4 * 2 = 8` |
| `/`      | Pembagian     | `9 / 3 = 3` |
| `%`      | Modulus       | `10 % 3 = 1` |

### Operator Perbandingan
| Operator | Fungsi               | Contoh       |
|----------|----------------------|--------------|
| `==`     | Sama dengan          | `5 == 5`     |
| `!=`     | Tidak sama dengan    | `5 != 3`     |
| `>`      | Lebih besar dari     | `7 > 5`      |
| `<`      | Lebih kecil dari     | `3 < 8`      |
| `>=`     | Lebih besar atau sama| `6 >= 6`     |
| `<=`     | Lebih kecil atau sama| `4 <= 5`     |

## Python List
List adalah kumpulan elemen yang terurut dan dapat diubah (mutable).

### Contoh:
```python
fruits = ["apple", "banana", "cherry"]
print(fruits[0])  # Output: apple
fruits.append("durian")
print(fruits)     # Output: ['apple', 'banana', 'cherry', 'durian']
```

## Python Tuples
Tuples adalah kumpulan elemen yang terurut dan tidak dapat diubah (immutable).

### Contoh:
```python
coordinates = (10, 20)
print(coordinates[1])  # Output: 20
```

## Python Dictionary
Dictionary adalah kumpulan pasangan key-value yang tidak terurut.

### Contoh:
```python
person = {"name": "Alice", "age": 30}
print(person["name"])  # Output: Alice
```

## Perbedaan antara List, Tuples, dan Dictionary
| Fitur         | List                  | Tuples                | Dictionary             |
|---------------|-----------------------|-----------------------|------------------------|
| Mutable       | ✅ Ya                 | ❌ Tidak              | ✅ Ya                  |
| Indexed       | ✅ Ya                 | ✅ Ya                 | ❌ Tidak (key-value)   |
| Syntax        | `[1, 2, 3]`          | `(1, 2, 3)`          | `{key: value}`         |

## Materi Tambahan

### 1. Conditional Statements
Python mendukung logika `if`, `elif`, dan `else` untuk pengambilan keputusan.
```python
age = 18
if age >= 18:
    print("Dewasa")
elif age >= 13:
    print("Remaja")
else:
    print("Anak-anak")
```

**Tips:**
- Gunakan indentasi (spasi) untuk menentukan blok kode.
- Indentasi standar Python adalah 4 spasi.

#### Contoh lanjutan:
```python
score = 85
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
else:
    print("D")
```

### 2. Looping
Python memiliki loop seperti `for` dan `while` untuk iterasi.

#### Contoh `for` loop:
```python
for i in range(5):
    print(i)  # Output: 0, 1, 2, 3, 4
```

#### Contoh loop dengan list:
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

#### Contoh `while` loop:
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

**Tips:** Gunakan kondisi di `while` dengan hati-hati untuk menghindari infinite loop.

#### Contoh nested loop:
```python
for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
```

### 3. Break dan Continue
- `break` digunakan untuk menghentikan loop.
- `continue` digunakan untuk melewatkan iterasi saat ini.

#### Contoh:
```python
for i in range(5):
    if i == 3:
        break
    print(i)  # Output: 0, 1, 2
```

```python
for i in range(5):
    if i == 3:
        continue
    print(i)  # Output: 0, 1, 2, 4
```

### 4. Fungsi
Fungsi digunakan untuk menyimpan blok kode yang dapat digunakan kembali.

#### Contoh:
```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))  # Output: Hello, Alice!
```

#### Fungsi dengan beberapa parameter:
```python
def add(a, b):
    return a + b

print(add(3, 5))  # Output: 8
```

#### Fungsi dengan nilai default:
```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

print(greet("Alice"))  # Output: Hello, Alice!
print(greet("Bob", "Hi"))  # Output: Hi, Bob!
```

### Argumen dan Parameter
#### 1. Required Argument
Argumen ini harus diberikan saat memanggil fungsi.
```python
def introduce(name):
    print(f"Hi, my name is {name}")

introduce("Alice")  # Output: Hi, my name is Alice
```

#### 2. Default Argument
Argumen ini memiliki nilai default jika tidak diberikan.
```python
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}")

greet("Alice")  # Output: Hello, Alice
greet("Bob", "Hi")  # Output: Hi, Bob
```

#### 3. Positional Argument
Argumen yang posisinya menentukan nilainya.
```python
def describe_person(name, age):
    print(f"{name} is {age} years old")

describe_person("Alice", 25)  # Output: Alice is 25 years old
```

#### 4. Keyword Argument
Argumen yang diberikan dengan nama parameter.
```python
def describe_person(name, age):
    print(f"{name} is {age} years old")

describe_person(age=25, name="Alice")  # Output: Alice is 25 years old
```

#### Fungsi tanpa return:
Fungsi ini hanya menjalankan aksi tanpa mengembalikan nilai.
```python
def print_message(message):
    print(message)

print_message("Hello World!")  # Output: Hello World!
```

### 5. Module

#### Apa itu Module?
Module adalah file Python yang berisi koleksi fungsi dan variabel yang dapat digunakan di program lain.

#### Mengimpor Module
Anda dapat mengimpor module dengan cara berikut:
```python
import math

print(math.sqrt(16))  # Output: 4.0
```

#### Mengimpor dengan Alias
Anda dapat menggunakan alias untuk module:
```python
import numpy as np

array = np.array([1, 2, 3])
print(array)
```

#### Mengimpor Fungsi Spesifik dari Module
```python
from math import sqrt

print(sqrt(25))  # Output: 5.0
```
