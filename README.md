# Tugas-1-Jarkom_Naufal-Ardhana_118

# IP PREFIX = 10.158.0.0

# TOPOLOGI
<img width="1625" height="477" alt="image" src="https://github.com/user-attachments/assets/be10d4f0-6049-418a-a87d-7121d589637f" />

# RINGKASAN ALOKASI IP
| No | Subnet (Nama)                                 | Jumlah Host Aktif (soal) | Prefix (dipilih) | Kapasitas Usable (host) |
|----|-----------------------------------------------|-------------------------:|------------------:|------------------------:|
| 1  | Sekretariat (Kantor Pusat)                    |                      380 | /23              | 510                     |
| 2  | Bidang Kurikulum (Kantor Pusat)               |                      220 | /24              | 254                     |
| 3  | Bidang Guru & Tendik (Kantor Pusat)           |                       95 | /25              | 126                     |
| 4  | Bidang Sarana Prasarana (Kantor Pusat)        |                       45 | /26              | 62                      |
| 5  | Bidang Pengawas Sekolah (Pusat)               |                       18 | /27              | 30                      |
| 6  | Bidang Pengawas Sekolah (Cabang)              |                       18 | /27              | 30                      |
| 7  | Server & Admin (Kantor Pusat)                 |                        6 | /29              | 6                       |
| 8  | Link Router Pusat–Cabang (P2P)                |                        2 | /30              | 2                       |

# VLSM
<img width="885" height="695" alt="image" src="https://github.com/user-attachments/assets/728c6896-4f38-4a16-b7d4-0dcf9592b6c3" />
<img width="1670" height="608" alt="image" src="https://github.com/user-attachments/assets/152a79cd-b23a-495a-be7d-160d691009a6" />

|  No | Nama Subnet (Lokasi)              | Jumlah Host Aktif | Prefix |     Netmask     |    Network   |     Range Host (usable)     |   Broadcast  |          Gateway         |
| :-: | :-------------------------------- | :---------------: | :----: | :-------------: | :----------: | :-------------------------: | :----------: | :----------------------: |
|  1  | Sekretariat (Kantor Pusat)        |        380        |   /23  |  255.255.254.0  |  10.158.0.0  |  10.158.0.1 – 10.158.1.254  | 10.158.1.255 |        10.158.0.1        |
|  2  | Bidang Kurikulum (Pusat)          |        220        |   /24  |  255.255.255.0  |  10.158.2.0  |  10.158.2.1 – 10.158.2.254  | 10.158.2.255 |        10.158.2.1        |
|  3  | Bidang Guru & Tendik (Pusat)      |         95        |   /25  | 255.255.255.128 |  10.158.3.0  |  10.158.3.1 – 10.158.3.126  | 10.158.3.127 |        10.158.3.1        |
|  4  | Bidang Sarana & Prasarana (Pusat) |         45        |   /26  | 255.255.255.192 | 10.158.3.128 | 10.158.3.129 – 10.158.3.190 | 10.158.3.191 |       10.158.3.129       |
|  5  | Bidang Pengawas Sekolah (Pusat)   |         18        |   /27  | 255.255.255.224 | 10.158.3.192 | 10.158.3.193 – 10.158.3.222 | 10.158.3.223 |       10.158.3.193       |
|  6  | Bidang Pengawas Sekolah (Cabang)  |         18        |   /27  | 255.255.255.224 | 10.158.3.224 | 10.158.3.225 – 10.158.3.254 | 10.158.3.255 |       10.158.3.225       |
|  7  | Server & Admin (Pusat)            |         6         |   /29  | 255.255.255.248 |  10.158.4.0  |   10.158.4.1 – 10.158.4.6   |  10.158.4.7  |        10.158.4.1        |
|  8  | Link Router Pusat ↔ Cabang (P2P)  |         2         |   /30  | 255.255.255.252 |  10.158.4.8  |   10.158.4.9 – 10.158.4.10  |  10.158.4.11 | 10.158.4.9 / 10.158.4.10 |

# CIDR
<img width="1228" height="819" alt="image" src="https://github.com/user-attachments/assets/e8c93847-29d1-4490-9de5-57169ff59a4c" />
<img width="1664" height="572" alt="image" src="https://github.com/user-attachments/assets/bcdfbf7d-45ef-4260-bc1d-65d26da6b137" />

| No | Network        | Mask               | Prefix | Range Host (usable)           | Broadcast       | Gateway         | Keterangan                                 |
|----|----------------|--------------------|:------:|-------------------------------|-----------------|-----------------|--------------------------------------------|
| 1  | 10.158.0.0     | 255.255.254.0      | /23    | 10.158.0.1 - 10.158.1.254     | 10.158.1.255    | 10.158.0.1      | Sekretariat (380 host)                     |
| 2  | 10.158.2.0     | 255.255.255.0      | /24    | 10.158.2.1 - 10.158.2.254     | 10.158.2.255    | 10.158.2.1      | Bidang Kurikulum (220 host)                |
| 3  | 10.158.3.0     | 255.255.255.128    | /25    | 10.158.3.1 - 10.158.3.126     | 10.158.3.127    | 10.158.3.1      | Bidang Guru & Tendik (95 host)             |
| 4  | 10.158.3.128   | 255.255.255.192    | /26    | 10.158.3.129 - 10.158.3.190   | 10.158.3.191    | 10.158.3.129    | Bidang Sarana Prasarana (45 host)          |
| 5  | 10.158.3.192   | 255.255.255.224    | /27    | 10.158.3.193 - 10.158.3.222   | 10.158.3.223    | 10.158.3.193    | Bidang Pengawas Sekolah - Pusat (18 host)  |
| 6  | 10.158.3.224   | 255.255.255.224    | /27    | 10.158.3.225 - 10.158.3.254   | 10.158.3.255    | 10.158.3.225    | Bidang Pengawas Sekolah - Cabang (18 host) |
| 7  | 10.158.4.0     | 255.255.255.248    | /29    | 10.158.4.1 - 10.158.4.6       | 10.158.4.7      | 10.158.4.1      | Server & Admin (6 host)                    |
| 8  | 10.158.4.8     | 255.255.255.252    | /30    | 10.158.4.9 - 10.158.4.10      | 10.158.4.11     | 10.158.4.9 /10  | Link Router Pusat-Cabang (P2P)             |
