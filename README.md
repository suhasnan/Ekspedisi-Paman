# Ekspedisi-Paman
Menghitung total pengeluaran selama satu bulan berdasarkan angka genap dan ganjil

Kali ini kita akan menghitung total pengeluaran dari angka genap dan ganjil yang sudah disediakan, kemudian dikalikan dengan jumlah hari genap dan ganjil dalam satu bulan
Langkah-langkah


 
 
 
 
 
 
 
 
 
 
 
 1. Pertama-tama kita memerlukan variabel yang berisi angka pengeluaran
                  
        uang_jalan = 1500000
	
     Dalam kasus ini kita menggunakan variabel uang_jalan sebagai angka pengkali dengan variabel lain
  
  2. Membuat variabel jumlah hari dan variabel yang berisi list menampung angka genap dan ganjil
          
          jumlah_hari = 31
	    
          list_plat_nomor = [8993, 2198, 2501, 2735, 3772, 4837, 9152]
	
	    Variabel jumlah_hari adalah total hari dalam satu bulan, hal ini bisa disesuaikan jika terdapat bulan yang hanya 30 hari atau 29 hari pada bulan februari
	    Pada variabel list_plat_nomor bisa di isi bebas dengan angka genap dan ganjil
      
   3. Lalu membuat 2 variabel yang berisi angka 0, variabel ini berfungsi untuk menampung berapa banyak angka genap dan ganjil dari variabel list_plat_nomor
   
          kendaraan_genap = 0
	        
          kendaraan_ganjil = 0
	
	    Di set dengan angka nol karena nanti akan ditambahkan melalui proses looping
      
  4. Kemudian kita membuat sebuah looping atau perulangan yang akan menghitung jumlah angka genap dan ganjil pada variabel list_plat_nomor
    
            for plat_nomor in list_plat_nomor:
	              if plat_nomor % 2 == 0:
	                  kendaraan_genap += 1
	              else:
	                  kendaraan_ganjil += 1
	
      Penjelasan looping
	    
            for plat_nomor in list_plat_nomor             # untuk setiap plat_nomor yang ada pada variabel list_plat_nomor
		  
            If plat_nomor % 2 == 0:                       # jika plat_nomor habis dibagi 2 atau menghasilkan angka nol jika di bagi 2
			
            Kendaraan_genap += 1                          # maka tambah 1 ke variabel kendaraan_genap tadi yang telah kita buat
		  
            else:                                         # jika plat_nomor tidak habis dibagi 2 atau tidak menghasilkan angka 0 jika di bagi 2
			
            Kendaraan_ganjil += 1                         # maka tambah 1 ke variabel kendaraan_ganjil yang telah kita buat tadi
            
   5. Lalu tetapkan variabel i yang berisi angka 1
	
	         i = 1
	
	     Di isi dengan angka 1 karena ini menentukan hari atau tanggal terkecil dalam satu bulan yakni tanggal 1, tidak bisa di set dengan angka 0 karena tidak ada tanggal 0
	     Nama variabel bisa diganti dengan hari atau tanggal untuk lebih memudahkan pemahaman
       
   6. Membuat variabel total pengeluaran yang berisi angka 0
    
          Total_pengeluaran = 0
          
       Nantinya variabel inilah yang berisi total keseluruhan pengeluaran angka genap dan ganjil selama satu bulan
       
   7. Kemudian membuat perulangan yang akan mengisi variabel total_pengeluaran tadi dengan mengkalikan variabel kendaraan_genap dan variabel uang jalan, jika variabel i habis dibagi 2 dan begitu juga begitu juga sebaliknya
	 
	        while i <= jumlah_hari:                                              # ketika variabel i kecil dari atau sama dengan jumlah_variabel jumlah hari pada langkah 2 tadi
	             if i % 2 == 0:                                                  # jika variabel i habis dibagi dua atau menghasilkan angka 0 jika dibagi dua
	                 total_pengeluaran += (kendaraan_genap * uang_jalan)         # maka, tambahkan nilai pada variabel total_pengeluaran sesuai dengan hasil pengkalian total variabel kendaraan_genap dan variabel uang_jalan
	             else:                                                           # selain itu, jika variabel i tidak habis dibagi dua atau tidak menghasilkan angka 0 jika dibagi dua
	                 total_pengeluaran += (kendaraan_ganjil * uang_jalan)        # maka, tambahkan nilai pada variabel total_pengeluaran sesuai dengan hasil pengkalian total variabel kendaraan_ganjil dan variabel uang_jalan
	        i += 1                                                                                                    
	 
	    i += 1, Artinya setiap kali perulangan while di atas selesai dilakukan maka variabel i akan bertambah satu, maksudnya disini ialah berfungsi untuk menambah hari atau tanggal pada kalender. 
      Nantinya variabel i akan di update menjadi 2, 3, 4, 5, … dan seterusnya sampai nanti pada angka 31 atau tanggal 31 akan berhenti karena sudah sama dengan angka pada variabel jumlah_hari
    
   8. Kemudian tinggal cetak atau panggil variabel total_pengeluaran
    
          print (total_pengeluaran)




