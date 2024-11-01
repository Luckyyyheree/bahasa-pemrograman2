# latihan praktikum 1
 Latihan 1: Buat program python untuk kasus berikut:

Kasus 1: Program Pemesanan Tiket Bioskop

Buat program yang menghitung harga tiket bioskop. Tiket reguler berharga Rp50.000, sedangkan tiket VIP berharga Rp100.000. Jika user memiliki kartu member, mereka mendapatkan diskon 20% dari harga tiket. Program ini harus meminta tipe tiket dan status member dari user, lalu menghitung total harga yang harus dibayar.

Petunjuk:

Gunakan if else dan operator ternary.

## cara kerja program
- Program akan meminta pengguna untuk memilih jenis tiket (reguler atau VIP) dan menyatakan status keanggotaan mereka (ya atau tidak).
- Berdasarkan pilihan jenis tiket, program akan menetapkan harga yang sesuai (Rp40.000 untuk tiket reguler dan Rp100.000 untuk tiket VIP).
- Jika jenis tiket yang dimasukkan tidak sah, program akan menampilkan pesan kesalahan dan menetapkan harga tiket menjadi 0.
- Jika pengguna memiliki kartu anggota dan jenis tiket yang dipilih sah, program akan menghitung diskon 20% dari harga tiket.
- Total yang harus dibayar akan ditampilkan dalam format dua angka desimal, selama harga tiket lebih dari 0.
  
## kode progam 
``` python
# Fungsi untuk menghitung total harga tiket
def hitung_harga_tiket():
    # Meminta input dari pengguna
    tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): ").lower()
    status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").lower()

    # Menentukan harga tiket berdasarkan tipe
    if tipe_tiket == "reguler":
        harga_tiket = 40000
    elif tipe_tiket == "vip":
        harga_tiket = 100000
    else:
        print("Tipe tiket salah / invalid!")
        return  # Pastikan untuk mengembalikan dari fungsi jika tipe tidak valid
    
    # Menghitung diskon jika pengguna adalah member
    diskon = 0.2 if status_member == "ya" else 0
    total_harga = harga_tiket * (1 - diskon)

    # Menampilkan total harga
    print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")

# Memanggil fungsi
hitung_harga_tiket()
```
## output program 
``` python
Masukkan tipe tiket (reguler/VIP): reguler
Apakah Anda memiliki kartu member? (ya/tidak): ya
Total harga yang harus dibayar: Rp32000
PS C:\Users\Kanzaki>
```
## flowchart latihan 1

![tiket vip](https://github.com/user-attachments/assets/e17f1312-cff1-4159-8f85-6a86a797be10)

# latihan 2
Kasus 2: Program Kalkulator Sederhana

Buat program kalkulator yang menerima dua angka dan satu operator aritmatika dari pengguna (penjumlahan, pengurangan, perkalian, atau pembagian). Program akan menghitung hasil sesuai dengan operator yang dipilih.

Petunjuk:

* Gunakan if elif else untuk menentukan operasi aritmatika.

## kode program
``` python
# progam kalkulator simple

# fungsi kalkulator
def calculate(num1, num2, operator):
    if operator == '+':
        return num1 + num2
    elif operator == '-':
        return num1 - num2
    elif operator == '*':
        return num1 * num2
    elif operator == '/':
        if num2 != 0:
            return num1 / num2
        else:
            return "Error! Division by zero."
    else:
        return "Invalid operator!"

# Main program
def main():
    # Taking input from the user
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))
    operator = input("Enter an operator (+, -, *, /): ")

    # Performing the calculation
    result = calculate(num1, num2, operator)

    # Displaying the result
    print("The result is:", result)

# Running the main program
if __name__ == "__main__":
    main()
```
## output program
``` python
Enter the first number: 3
Enter the second number: 6
Enter an operator (+, -, *, /): +
The result is: 9.0
PS C:\Users\Kanzaki>
```
## flowchart
![kalkulator](https://github.com/user-attachments/assets/2f3641af-968f-4fee-87c4-371fd2232fc6)

## cara kerja program
Mirip dengan kalkulator standar, tetapi tanpa tampilan yang menarik karena hanya berupa kalkulator dasar.
