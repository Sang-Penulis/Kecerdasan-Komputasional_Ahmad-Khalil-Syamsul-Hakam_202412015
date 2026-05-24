# SISTEM STATUS KEHADIRAN MAHASISWA
# DATA MAHASISWA (ARRAY)
nama = [
    "Andi",
    "Budi",
    "Citra",
    "Deni",
    "Khalil" # Data mahasiswa baru
]

kehadiran = [
    "Tinggi",
    "Rendah",
    "Tinggi",
    "Rendah",
    "Tinggi"
]

tugas = [
    "Lengkap",
    "Tidak Lengkap",
    "Tidak Lengkap",
    "Lengkap",
    "Lengkap"
]

# HEADER PROGRAM
print("SISTEM ANALISIS PRESENSI MAHASISWA")
print("DECISION TREE SEDERHANA (IF-ELSE)")

# VARIABEL TAMBAHAN
aktif = 0
tidak_aktif = 0
disiplin = 0

# PROSES DATA
for i in range(len(nama)):

    # LOGIKA DECISION TREE
    if kehadiran[i] == "Tinggi":
        status = "Aktif"
        aktif += 1
    else:
        status = "Tidak Aktif"
        tidak_aktif += 1

    # KETERANGAN TAMBAHAN
    if kehadiran[i] == "Tinggi" and tugas[i] == "Lengkap":
        keterangan = "Mahasiswa Disiplin"
        disiplin += 1
    elif kehadiran[i] == "Tinggi" and tugas[i] == "Tidak Lengkap":
        keterangan = "Aktif Tetapi Tugas Kurang"
    else:
        keterangan = "Perlu Pembinaan"

    # OUTPUT DATA MAHASISWA
    print("\n" + "-" * 65)
    print("Nama :", nama[i])
    print("Kehadiran :", kehadiran[i])
    print("Tugas :", tugas[i])
    print("Status :", status)
    print("Keterangan :", keterangan)

# FITUR TAMBAHAN
# Statistik Mahasiswa
print("STATISTIK MAHASISWA")
print("Jumlah Mahasiswa Aktif :", aktif)
print("Jumlah Mahasiswa Tidak Aktif :", tidak_aktif)
print("Jumlah Mahasiswa Disiplin :", disiplin)
print("Total Mahasiswa :", len(nama))

# PENUTUP PROGRAM
print("\nProgram berhasil dijalankan tanpa error.")
