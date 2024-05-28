import os
from termcolor import colored,cprint
os.system('cls')
baris_atas  = 3
baris_bawah = 3
lebar       = 32
for _ in range(baris_atas):
    cprint(" " * lebar, 'white', 'on_blue')
cprint(" " * lebar, 'blue', 'on_white')
def cetak_teks(teks, panjang):
    kiri = (lebar - panjang) // 2
    cprint(" " * kiri, 'blue', 'on_white', end="")
    for char in teks:
        if char != ' ':
            cprint(" ", 'blue', 'on_blue', end="")
        else:
            cprint(" ", 'blue', 'on_white', end="")
    kanan = lebar - kiri - panjang
    cprint(" " * kanan, 'blue', 'on_white')
    print(end="")

cetak_teks("  ██    ██ ██ ███████  █████    ",50)
cetak_teks("  ██    ██ ██ ██      ██   ██   ",50)
cetak_teks("  ██    ██ ██ ███████ ███████   ",50)
cetak_teks("  ██    ██ ██      ██ ██   ██   ",50)
cetak_teks("    ████   ██ ███████ ██   ██   ",50)


cprint(" " * lebar, 'blue', 'on_white')
for _ in range(baris_bawah - 7):  
    cprint(" " * lebar, 'blue', 'on_white')
for _ in range(baris_atas):
    cprint(" " * lebar, 'white', 'on_yellow')
