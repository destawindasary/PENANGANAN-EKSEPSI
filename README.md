@triexcept1.py

#menginpor modul sys untuk exit()
import sys
def main () :
        #membuat judul program
        print("PROGRAM PEMBAGIAN BILANGAN")

        #meminta user memasukkan bilangan
        a=float(input("Masukkan a : "))
        b=float(input("Masukkan b :"))

        #mendefenisikan blok try..except
        try:
            hasil = a/b
        except ZeroDivisionError:
            print("\nERROR: Nilai b tidak boleh nol")
            sys.exit(1) #menghentikan program

        #menampilkan hasil
        print("\na : ", a)
        print("b : ", b)
        print("a / b = ", hasil)

if __name__ == "__main__":
    main()
@triacept2.py
def main():
    print("PROGRAM PEMBAGIAN BILANGAN")

        #meminta user memasukkan bilangan
    a = float(input("Masukkan a: "))
    
    b = float(input("Masukkan b :"))

        #mendefenisikan blok try..except
try: 
            hasil = a / b
except ZeroDivisionError:
            print("\nERROR: Nilai b tidak boleh nol")

        #menampilkan hasil
            print("\na : ", a)
            print("b : ", b)

        #kode di bawah ini akan menimbulkan kesalahan
        #dengan tipe NameError
            print("a / b = ", hasil)

if __name__ == "__main__":
    main()

@triaceptElse.py
def main():
    print("PROGRAM PEMBAGIAN BILANGAN")

        #meminta user memasukkan bilangan
    a = float(input("Masukkan a: "))
    
    b = float(input("Masukkan b :"))

        #mendefenisikan blok try..except
try: 
            hasil = a / b
except ZeroDivisionError:
            print("\nERROR: Nilai b tidak boleh nol")
else:
            print("\na : ", a)
            print("b : ", b)
            print("a / b = ", hasil)

if __name__ == "__main__":
    main()
@multy.py

def main():
    print("PROGRAM PEMBAGIAN BILANGAN")

     #mendefenisikan blok try..except
try:
             #meminta user memasukkan bilangan
        a=float(input("Masukkan a : "))
        b=float(input("Masukkan b :"))
        #melakukan pembagian
        hasil = a/ b

except ZeroDivisionError:
            print("\nERROR: Nilai b tidak boleh nol")

            #mengantisipasi variabel a atau b belum diisi
except ValueError:
                print("\nERROR: a dan b harus berupa angka")

            #mengantisipasi variabel a atau b belum diisi
except KeyboardInterrupt:
                print("\nERROR: Jangan tekan CTRL+C!")

else:
            print("\na : ", a)
            print("b : ", b)
            print("a / b = ", hasil)

if __name__ == "__main__":
    main()
@ekspeksi.py

def main():
    print("PROGRAM PEMBAGIAN BILANGAN")

     #mendefenisikan blok try..except
try:
             #meminta user memasukkan bilangan
        a=float(input("Masukkan a : "))
        b=float(input("Masukkan b :"))
        #melakukan pembagian
        hasil = a/ b

except (ZeroDivisionError, ValueError, KeyboardInterrupt) :
            print("\nERROR: Anda telah melakukan " + "kesalahan")

else:
            print("\na : ", a)
            print("b : ", b)
            print("a / b = ", hasil)

if __name__ == "__main__":
    main()
@userdefined.py

import math

#membuat ekspsi AbstractError
class AbstractError(RuntimeError) :
    def __init__(self,s):
        self.s = s

#mendefenisikan kelas abstrak
class DuaDimensi(object):
    def __init__(self):
        raise AbstractError("ERROR: ' " + "DuaDimensi" + " ' adalah kelas abstrak")
    def luas(self):
        raise NotImplementedError
    def keliling(self):
        raise NotImplementedError

    #membuat kelas lingkaran,
    #turunan dari kelas Duadimensi
    class Lingkaran(DuaDimensi):
        def __init__(self, r):
            self.r=r
        def luas(self):
            return 2 * math.pi * self.r

def main():
    obj1 = Lingkaran(3)

    print("LINGKARAN")
    print("luas\t\t:", obj1.luas())
    print("Keliling\t:", obj1.keliling())

    try:
        print("\nMembuat objek " + "dari kelas DuaDimensi..")
        obj2=DuaDimensi()
    except AbstractError as error:
        print(error.s)
    else:
        print("DuaDimensi")
        print("luas\t\t:", obj2.luas())
        print("Keliling\t:", obj2.keliling())

    
if __name__ == "__main__":
    main()













    

