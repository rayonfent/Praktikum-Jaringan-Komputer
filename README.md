# Praktikum-Jaringan-Komputer

## Ping Gagal
Percobaan ping dari PC-A dengan alamat IP 192.168.1.3 ke PC-B dengan alamat IP 192.168.0.3 awalnya tidak berhasil.
Kegagalan ini terjadi karena router belum dikonfigurasi, sehingga kedua jaringan (192.168.0.1 dan 192.168.1.1) belum terhubung satu sama lain.
Tanpa konfigurasi pada router, perangkat belum memiliki alamat IP pada setiap interface dan belum dapat melakukan proses routing antar subnet.
Akibatnya, paket ICMP yang dikirim oleh PC-A tidak dapat mencapai PC-B.

## Ping Berhasil
Setelah router dikonfigurasi dengan alamat IP pada masing-masing interface dan diaktifkan, router mulai berfungsi sebagai penghubung antara kedua jaringan.
Router R1 memiliki interface GigabitEthernet0/0/1 dengan alamat 192.168.1.1 sebagai gateway untuk PC-A, dan interface GigabitEthernet0/0/0 dengan alamat 192.168.0.1 sebagai gateway untuk PC-B.
Dengan konfigurasi tersebut, router dapat melakukan routing antar subnet, sehingga ketika dilakukan ping kembali dari PC-A ke PC-B, paket ICMP berhasil dikirim dan menerima balasan.
Hal ini menunjukkan bahwa konektivitas antar jaringan sudah berfungsi dengan baik.
