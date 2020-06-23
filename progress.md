## Revisi 12 Juni 2020
Beberapa fitur yg tidak bisa di klik :
1. Tombol "lihat detail" pada masing2 informasi dari status berkas ✅
2. Banner informasi tentang GR pada menu Beranda ✅
3. Tombol informasi produk pada menu Asuransi. ✅
   
Ada dua tombol yg sama :
1. Tombol "Keanggotaan saya" pada menu Beranda ✅
2. Tombol "Lihat semua polis" pada menu Beranda ✅


## Revisi 13 Juni 2020

### Beranda
1. Keanggotaan : 
    - detail dihilangkan, diubah jadi menu shortucut ✅
    - pada detail keanggotaan, apabila user blm memiliki keanggotaan, maka akan ditampilkan user memiliki keanggotaan "candidate" untuk setiap marketer yang ada ✅
2. Banner : ditambahkan banner 7 definisi asuransi
3. Iuran:
   - yang akan datang: dihilangkan ✅
   - digabung dengan stats polis ✅
4. Permohonan: label menjadi "status permohonan" ✅
5. Polis:
    - menampilkan polis saya: Polis Aktif, Polis akan diperpanjang, polis akan diperbarui ✅
    - menampilkan polis teman: Polis Aktif, Polis akan diperpanjang, polis akan diperbarui ✅
    - detail polis, apabila di klik, ke halaman polis dengan filter yang dipilih ✅
6. Klaim
    - label menjadi "Status klaim" ✅
    - yang ditampilkan: Total Laporan, Closed, On going (Perhitungan On going yakni total - closed) ✅
7. Referral
    - label member menjadi "tergabung" ✅
    - ditambahkan statistik jumlah orang yang sudah diajak bergabung, namun belum tergabung (blm daftar atau blm membeli produk) ✅

### General
1. label pengelola menjadi "pengelola administrasi" ✅
2. menu asuransi diganti produk ✅

### Note
1. Level/policy untuk marketer disamakan
2. Referral: apabila org yg di ajak terdapat nama yang sama, untuk membedakan identitas orang tersebut, maka ditampilkan informasi email dan no. telpon
3. Polis Teman: untuk pembelian polis utk teman, akan dikirimkan email ke teman (org yg dibelikan polisnya). adapun doc dikirimkan pada saat: renewal, pengajuan, disetujui (untuk detail, menunggu dokumen dari Pak Irwan)

### Lainnya (web)
1. redirect dari web pemasar, diarahkan ke halaman login gantirugi dengan logo pemasar(asal) ✅
2. dengan 2 step landing page (sesuai dokumen yg diberikan Pak Irwan) 
contoh: buka web "pemasar A" lalu diredirect ke login gantirugi, di halaman gantirugi ada logo "pemasar A" dan mengikuti desain 2 step landing page ✅

## Revisi 16 Juni 2020 (web)
1. kalau dari web pengelola tampil 2 step/page, kalau dari web pemasar langsung saja
2. 2 page: 
   1. halaman welcome (disclaimer, hanya pengelola administrasi), pilih pemasar.
   2. baru signup


## Revisi 17 Juni 2020

### mobile apps
1. mengajukan permohonan 
    - error message -> "permohonan tidak dapat diterima" karena data belum lengkap, expired, dan error lainnya perlu dibedakan 🚧
    - permohonan asuransi, tidak dapat di ajukan dengan error "permohonan tidak dapat diterima" 🚧

2. informasi penampilan penawaran yg expired (seperti aplikasi lama) apabila penawaran telah expired dapat diperbaharui juga dengan tgl inception mengikuti ketentuan ✅

3. cashback di perhitungan premi salah, tidak 25% untuk candidate ✅

4. judul pilih pemasar&penanggung, caption button menjadi "Pilih Pemasar" ✅

5. semua label iuran menjadi premi ✅

6. banner : materi 8 definisi asuransi (lampiran 3) 🚧API

    -> materi no 8, dipindah ke nomor satu

7. urutan menu : beranda, produk, polis, klaim, saya ✅

8. bug di button beli perhitungan premi ✅

9. informasi produk hanya ada PA ✅

10. menu "saya" jadi "akun" ✅

11. untuk informasi produk menggunakan info produk yg lama ✅


### Dokumen2

1. update semua dokumen pdf sesuai 🚧API

    -> dokumen PDF : update terbaru, dokumen (bulan maret seperti (Lampiran 1) 

2. label pengelola -> pengelola adminstrasi 🚧API

3. penanggung ditampilkan, pemasar ditampilkan,  (optional, ditampilkan semua, tdk pakai logo hanya nama, seperti yg berjalan skrg) 🚧API


### Testing
1. skenario testing  ✅

2. menyiapkan data2 yg diperlukan untuk testing
    - account, sesuai level (Principal, Partner, Executive dan Associate)  ✅
    - data pemasar & penanggung dengan detail :  ✅
    
        a. Pemasar A dengan Penanggung ABC b. Pemasar B dengan Penanggung ABC dan c Pemasar C dengan Penanggung XYZ ... ini untuk produk mobil ... untuk produk PA kombinasi dapat berbeda ... misalkan: Pemasar A dengan Penanggung UVW atau Pemasar B dengan Penangung DEF. 

        * note: untuk setiap produk, bisa dibedakan untuk kombinasi penanggung, misal mobil: pemasar A penanggung XY, PA: pemasar B  penanggung YZ, motor: pemasar A penanggung XY dan pemasar B penanggung XZ


### Notes
1. Label CashBack tetap CashBack ✅

2. Komisi (biaya yg displit dari CashBack) seharusnya menjadi Biaya Survey 

3. Referral Fee seharusnya menjadi Reward Komunitas 

4. Jadi besaran CashBack yg bisa displit oleh Principal atau Partner, namanya menjadi Biaya Survey


### Lampiran 
Lampiran 1
https://github.com/budi7/gantiRugi/blob/master/documents/Surat%20Penawaran%20Asuransi%20Mobil%20AFTER.pdf

Lampiran2 
https://github.com/budi7/gantiRugi/blob/master/documents/8%20Asuransi%20versi%20Growth%20Mindset.pdf


1. Expired, bisa lihat di field status -> expired_at > (now)
2. https://trello.com/c/PBdpCzEU/31-3-user-bisa-melihat-riwayat-quotes-menghapus-atau-refresh

    polis teman, aktif: dashboard->stat->insurance->actived->activator
    polis teman, akan diperpanjang: dashboard->stat->insurance->extending->activator
    polis teman, akan diperbarui: dashboard->stat->insurance->renewing->activator
    - detail polis, apabila di klik, ke halaman polis dengan filter yang dipilih
    polis saya/teman : filter holder, policy_owner/activator, digandeng dengan status:actived
    polis akan diperbaharui/diperpanjang : filter setting, extending/renewing, digandeng dengan status:actived
