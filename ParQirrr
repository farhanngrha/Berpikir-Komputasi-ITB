#KAMUS
#database = Data Kendaraan, list
#riwayat_kendaraan = Riwayat Kendaraan, list
#kapasitas_parkir = Kapasitas Parkir, int
#jumlah_kendaraan = Jumlah Kendaraan Yang Sedang Parkir, int
#kode_akses = Kode Akses, int
#kode_pengguna = Kode Akses yang terdapat dalam database
#pilihan = Menu yang dipilih, int
#plat_nomor = Plat Nomor Motor
#jenis_kendaraan = Jenis Kendaraan
#P = Array Kapasitas Parkir, array
#lama_parkir= Waktu Kendaraan Parkir di ITB Jatinangor (Jam), int


#ALGORITMA 
#KAMUS
#database = Data Kendaraan, list
#riwayat_kendaraan = Riwayat Kendaraan, list
#kapasitas_parkir = Kapasitas Parkir, int
#jumlah_kendaraan = Jumlah Kendaraan Yang Sedang Parkir, int
#kode_akses = Kode Akses, int
#kode_pengguna = Kode Akses yang terdapat dalam database
#pilihan = Menu yang dipilih, int
#plat_nomor = Plat Nomor Motor
#jenis_kendaraan = Jenis Kendaraan
#P = Array Kapasitas Parkir, array
#lama_parkir= Waktu Kendaraan Parkir di ITB Jatinangor (Jam), int


#ALGORITMA
database = [
    237109, 723098, 893555, 998608, 700378, 577256, 820787, 810767, 340599, 245652,
    976434, 232458, 164978, 405771, 324416, 419617, 289781, 622865, 167535, 536119,
    503738, 913748, 731043, 634530, 441996, 737791, 479502, 642574, 581569, 218624,
    398266, 239481, 947037, 994126, 578398, 860462, 268458, 744478, 866957, 197949,
    845670, 156149, 417124, 683520, 218525, 956603, 524837, 713349, 698274, 118508
]

# Kapasitas parkir dan variabel parkir
kapasitas_parkir = 25
jumlah_kendaraan = 0
P = [0] * kapasitas_parkir

# Kapasitas maksimum untuk Riwayat Kendaraan
riwayat_kendaraan = [0] * 50
i = 0

while True:
    # Tampilkan menu utama
    print("=== ParQirr: Sistem Parkir ITB Multikampus Jatinangor ===")
    print("1. Masuk Parkir")
    print("2. Keluar Parkir")
    print("3. Cek Kendaraan Saat Ini")
    print("4. Riwayat Kendaraan Hari Ini")
    
    pilihan = input("Pilih menunya boss: ")

    # Menu Masuk Parkir
    if pilihan == '1':
        if jumlah_kendaraan >= kapasitas_parkir:
            print("Maaf, parkiran penuh.")
        else:
            kode_akses = int(input("Masukkan kode akses: "))
            
            # Cek kode_pengguna akses
            for kode_pengguna in database:
                if kode_akses == kode_pengguna:
                    plat_nomor = input("Masukkan nomor plat kendaraan: ")
                    jenis_kendaraan = input("Masukkan jenis kendaraan (mobil/motor): ")
                
                    # Menambahkan kendaraan ke data parkir dan riwayat
                    kendaraan = [kode_akses, plat_nomor, jenis_kendaraan]
                    for i in range(kapasitas_parkir):
                        if P[i] is 0:
                            P[i] = kendaraan
                            jumlah_kendaraan += 1
                            riwayat_kendaraan[i] = kendaraan
                            i += 1

                        print("Silakan masuk. Kendaraan Anda telah terdaftar.")
            else:
                print("Maaf, kode_pengguna akses salah. Tolong periksa lagi.")

    # Menu Keluar Parkir
    elif pilihan == '2':
        kode_akses = int(input("Masukkan kode_pengguna akses: "))
        plat_nomor = input("Masukkan nomor plat kendaraan: ")
        lama_parkir = int(input("Masukkan lama parkir (dalam jam): "))

        for i in range(kapasitas_parkir):
            if P[i] != 0 and P[i][0] == kode_akses and P[i][1] == plat_nomor:
                kendaraan_ditemukan = True
                P[i] = 0
                jumlah_kendaraan -= 1

                # Hitung biaya parkir
                if jenis_kendaraan == str("motor") or str("Motor"):
                    if lama_parkir <= 1:
                        biaya = 2000
                    else:
                        biaya = 2000 + (lama_parkir - 1) * 1000
                elif jenis_kendaraan == str("mobil") or str("Mobil"):
                    if lama_parkir <= 1:
                        biaya = 5000
                    else:
                        biaya = 5000 + (lama_parkir - 1) * 2000
                print("Biaya parkir anda adalah: " + str(biaya))
                print("Silakan bayar di petugas yaaa temann ^^")
                print("Terima kasih, sampai jumpa lagi!")

        else:
            print("Maaf, kendaraan Anda tidak ada dalam database.")

    # Menu Cek Kendaraan Saat Ini
    elif pilihan == '3':
        if jumlah_kendaraan == 0:
            print("Tidak ada kendaraan yang diparkir saat ini.")
        else:
            print("=== Daftar Kendaraan yang Diparkir ===")
            nomor_urut = 1
            for i in range(kapasitas_parkir):
                if P[i] != 0:
                    print(str(nomor_urut) + "Nomor Plat:" + str(P[i][1]) + "Jenis Kendaraan:" + str(P[i][2]))
                    nomor_urut += 1

    # Menu Riwayat Kendaraan Hari Ini
    elif pilihan == '4':
        if i == 0:
            print("Belum ada kendaraan yang masuk hari ini.")
        else:
            print("=== Riwayat Kendaraan Masuk Hari Ini ===")
            nomor_urut = 1
            for i in range(i):
                print(str(nomor_urut) + "Nomor Plat:" + str(riwayat_kendaraan[i][1]) + "Jenis Kendaraan:" + str(riwayat_kendaraan[i][2]))
                nomor_urut += 1

    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
