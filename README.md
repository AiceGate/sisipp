# SISTEM NOTIFIKASI SIPP #

NOTIFIKASI WHATSAPP
- Pendaftaran Perkara
- Penetapan Majelis
- Penetapan PP
- Penetapan Jurusita
- Penetapan Hari Sidang
- Penundaan Sidang
- BHT

## Environment Variables

File ini berisi konfigurasi aplikasi, seperti nama aplikasi dan koneksi database SIPP

```
// .env

APP_TITLE="SISIPP"
APP_DESCRIPTION="SISTEM NOTIFIKASI PIHAK - MAHKAMAH SYAR'IAH SIGLI"
PORT=3000
HOST_SIPP= "192.168.1.3"
USER_SIPP= "root"
PASSWORD_SIPP= "sql4dm1n"
DATABASE_SIPP= "sipp_ms_sigli"

```

## Install and Running

Clone the project

```
  git clone https://github.com/AiceGate/sisipp
  cd sisipp
  node index
```

## WAJIB seting LOG DB

Modul ini bekerja dengan memantau file log database, bukan langsung memantau database itu sendiri. Dengan demikian, performa database tidak akan terpengaruh sama sekali.

LINUX : tambahkan baris berikut di file /etc/my.cnf
```
[mysqld]
server-id        = 1
log_bin          = /var/log/mariadb/mysql-bin
log_bin_index    = /var/log/mariadb/mysql-bin.index
binlog-format    = row                              # needed for row events
# Optional
expire_logs_days = 10
```

## License

This application is licensed by Catur Adi Sukrisno
