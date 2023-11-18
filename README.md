# UTS-METODE-NUMERIK
1. Persamaan non Linear
3 + x^3 - x = 4

2. Persamaan Linear
2x - 4 = 8

Jawaban

1. Persamaan non linear
3 + x³ - x = 4 
3 + x³ - x - 4 = 0 
x³ - x + 3 - 4 = 0 
x³ - x - 1 = 0 atau 
x³ - x = 1

dengan cara sebagai berikut: 

def fungsi_non_linear(x):
    return x**3 - x + 3 - 4
	
def turunan_fungsi_non_linear(x):
    return 3*x**2 - 1

def metode_newton_raphson(x0, toleransi, maks_iter):
    iterasi = 1
    while iterasi <= maks_iter:
          x1 = x0 - fungsi_non_linier(x0) / turunan_fungsi_non_linier(x0)
          print(f'Iterasi {iterasi}: x = {x1}')

	  if abs(x1 - x0) < toleransi:
	     print(f'Solusi ditemukan setelah {iterasi} iterasi: x = {x1}')
	     return x1

	     x0 = x1
	     iterasi += 1

	  print('Iterasi maksimum tercapai. Metode Newton-Raphson tidak konvergen.')
	  return None

# Tentukan nilai awal, toleransi, dan maksimum iterasi
x0 = 1.0
toleransi = 1e-6
maks_iter = 100

# Panggil fungsi untuk metode Newton-Raphson
solusi = metode_newton_raphson(x0, toleransi, maks_iter)

2. Persamaan linear
2x - 4 = 8 
2x = 8 + 4 
2x = 12 
x = 6
solusi persamaan linear ini adalah x = 6.

def solve_linear_equation(coef, constant):
# Persamaan linear: coef * x = constant
x = constant / coef
return x

# Koefisien persamaan
coef = 2

# Konstanta persamaan
constant = 8 + 4  # Sisi kanan persamaan dipindahkan ke sisi kiri dengan menggabungkan konstanta

# Panggil fungsi untuk menyelesaikan persamaan linear
solusi = solve_linear_equation(coef, constant)

# Cetak solusi
print(f"Solusi persamaan 2x - 4 = 8 adalah x = {solusi}")
Output :

Solusi persamaan 2x - 4 = 8 adalah x = 6.0

Jadi, nilai \(x\) untuk persamaan linier adalah 6.
