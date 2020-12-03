# Lab 6

## Latihan 1

 ![1.1.png](/gambar/1.1.png)


	Source Code

	print("________________________________________")
	# mengubah function menggunakan lambda


	def a(x):
	   	return x ** 2


	lambda x: x ** 2


	print("1. Mengubah function menggunakan Lambda \n   def a(x): \n \t   return x ** 2")
	print("   Hasil : lambda x: x ** 2")


	def b(x, y):
        	return math.sqrt(x ** 2 + y ** 2)


	lambda x, y: math.sqrt(x ** 2 + y ** 2)


	print("________________________________________")
	print("2. Mengubah function menggunakan Lambda \n   def b(x, y): \n \t   return math.sqrt(x ** 2 + y ** 2)")
	print("   Hasil : lambda x, y: math.sqrt(x ** 2 + y ** 2))")


	def c(*args):
        	return sum(args) / len(args)


	lambda *args: sum(args) / len(args)


	print("________________________________________")
	print("3. Mengubah function menggunakan Lambda \n   def c(*args): \n \t   return sum(args) / len(args)")
	print("   Hasil : lambda *args: sum(args) / len(args))")


	def d(s):
        	return "".join(set(s))


	lambda s: "".join(set(s))


	print("________________________________________")
	print("4. Mengubah function menggunakan Lambda \n   def d(s): \n \t   return "".join(set(s))")
	print("   Hasil : lambda s: "".join(set(s)))")

## Hasil Output

 ![1.2.png](/gambar/1.2.png)





# praktikum6

	
  **Tugas Praktikum**
  
  Buat program sederhana dengan mengaplikasikan penggunaan fungsi
  yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:
  
  • Fungsi tambah() untuk menambah data
  
  • Fungsi tapilkan() untuk menampilkan data
  
  • Fungsi hapus(nama) untuk menghapus data berdasarkan nama
  
  • Fungsi ubah(nama) untuk mengubah data berdasarkan nama
  
  • Buat flowchart dan penjelasan programnya pada README.md. 
  
  • Commit dan push repository ke github.




	@author: febri aditiya
	"""

	print("||===========================================================================================||")
	print("||=========================>>>>>>>>>>>|| Selamat Datang ||<<<<<<<<<<<========================||")
	print("||===========================================================================================||")

	data = {}


	def tambah():
     	     print("Tambah Data")
     	     nama  = input("Nama                  : ")
     	     nim   = input("Nim                   : ")
     	     tugas = float(input("Masukkan Nilai Tugas  : "))
     	     uts   = float(input("Masukkan Nilai UTS    : "))
     	     uas   = float(input("Masukkan Nilai UAS    : "))
     	     akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
     	     data[nama] = nim, tugas, uts, uas, akhir
     
	def tampilkan():
    	    if data.items():
        	print("======================>>>>>>>>>>>>>>>>|| DAFTAR NILAI ||<<<<<<<<<<<<<<<=======================")
        	print("||==========================================================================================||")
        	print("|| NO |     NAMA       |      NIM     |    TUGAS    |    UTS     |    UAS     |    AKHIR    ||")
        	print("||==========================================================================================||")
        	i = 0
        	for x in data.items():
            	i += 1
            	print("  1  |  {0:9}  |  {1:9}  |  {2:9}  |  {3:9}  |  {4:9}  |  {5:9}  |" .format(
                      x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4]))
        
           else:
            	print("========================>>>>>>>>>>>>>|| Tidak Ada Data ||<<<<<<<<<<<<<=========================")
         
         
	def hapus():
     	     print("Hapus Data Mahasiswa")
     	     nama = input("nama : ")
     	     if nama in data.keys():
         	 del data[nama]
         	 print()
     	     else:     
         	 print("Data {0} tidak ada".format(nama))
         
         
	def ubah():       
    	    print("Ubah Data Mahasisiswa")
    	    nama      = input("Nama                  : ")
    	    if nama in data.keys():
        	nim   = input("Nim                   : ")
        	tugas = float(input("masukkan nilai tugas  : "))
        	uts   = float(input("masukkan nilai uts    : "))
        	uas   = float(input("masukkan nilai uas    : "))
        	akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
        	data[nama] = nim, tugas, uts, uas, akhir 
        	print()
    	    else:
        	print("Data Nilai {0} tidak ada ".format(nama))
        
	while True:
    	    print("====================>>>>>>>>>|| Biodata Mahasiswa Teknik Informatika ||<<<<<<<<<=====================")
    	    print("||=================================================================================================||")
    	    print("||  No  ||       Nama       ||        Nim      ||   Tugas    ||   Uts   ||   Uas   ||     Akhir    ||")
     	    print("||=================================================================================================||")
    	    print("=====================>>>>>>>>>>>>>>>>>>> TIDAK ADA DATA <<<<<<<<<<<<<<<<<<<<<<<<=====================")
    	    x = input("1.| Lihat Data \n2.| Tambah Data \n3.| Ubah Data \n4.| Hapus data \n0.| Keluar Aplikasi \nPilih menu : ")
    	    if x.lower() == "1":
        	tampilkan()
    	    elif x.lower() == "2":
        	tambah()
   	    elif x.lower() == "3":
        	ubah()
    	    elif x.lower() == "4":
        	hapus()
    	    elif x.lower() == "0":
        	print()
        	print("||===========================================||")
        	print("||      >>>   Keluar Dari Program   <<<      ||")
        	print("||===========================================||")
        	break
    
    	    else:
        	print()
        	print("||======================================||")
        	print("||       >>>   Program Eror   <<<       ||")
        	print("||======================================||")

 ## Hasil Output

 ![1.png](/gambar/1.png)

 ## Tambah Data

 ![2.png](/gambar/2.png)
  
  ``Lihat Data``

 ![3.png](/gambar/3.png)

 ## Ubah Data

 ![4.png](/gambar/4.png)

  ``Lihat Data``

 ![5.png](/gambar/5.png)

 ## Hapus Data

 ![6.png](/gambar/6.png)

 # Selesai