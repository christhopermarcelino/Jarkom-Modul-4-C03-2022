# Laporan Resmi Praktikum Modul 4 Jaringan Komputer

Penyelesaian Soal Shift Modul 4 Jaringan Komputer 2022 <br>
Kelompok C03
- Aqil Ramadhan Hadiono - NRP 5025201261
- Christhoper Marcelino Mamahit - NRP 5025201249
- Zahra Fayyadiyati - NRP 5025201133

## Table of Contents
* [VLSM](#vlsm)
* [CIDR](#cidr)
* [Kendala](#kendala)

## VLSM
### Pembagian Subnet  
![image](https://user-images.githubusercontent.com/78243059/203458942-d5454a32-cf54-48a4-9a02-90cfc897e7f4.png)


|Subnet     |Jumlah IP |Netmask   |
|-          |-         |-         |
|A1         |1001      |/22       |
|A2         |2         |/30       |
|A3         |251       |/24       |
|A4         |2         |/30       |
|A5         |51        |/26       |
|A6         |2         |/30       |
|A7         |2         |/30       |
|A8         |2         |/30       |
|A9         |271       |/23       |
|A10        |2         |/30       |
|A11        |121       |/25       |
|A12        |2         |/30       |
|A13        |121       |/25       |
|A14        |71        |/25       |
|A15        |2         |/30       |
|A16        |211       |/24       |
|A17        |2         |/30       |
|A18        |501       |/23       |
|Total      |2617      |/20       |

### Pohon Pembagian IP

### Topologi CPT

## CIDR
### Topologi pada GNS3

![image](https://user-images.githubusercontent.com/34309557/203185983-fee42a6f-93a9-4460-9a29-25d9522f84b3.png)

Metode CIDR adalah metode pembagian IP dengan cara menggabung-gabungkan subnet-subnet terkecil yang terjauh dari internet (awan) hingga menjadi satu subnet besar. Kemudian, dari satu subnet besar tersebut, pembagian pohon IP dapat dilakukan. Hal ini mirip dengan konsep bottom up approach.

### Pembagian Subnet

**Subnet Awal (Subnet A)**

Terdapat  18 subnet A pada topologi.

![image](https://user-images.githubusercontent.com/34309557/203200840-c2415e28-d268-491f-9ae6-e8dd565dc8ca.png)

**Gabungan Subnet Pertama (Subnet B)**

- Penggabungan subnet A8 dan A9 menjadi B1
- Penggabungan subnet A14 dan A15 menjadi B2
- Penggabungan subnet A17 dan A18 menjadi B3
- Penggabungan subnet A6 dan A7 menjadi B4

![image](https://user-images.githubusercontent.com/34309557/203201915-25e91ca9-ea3d-4d6b-8313-162b9cd09c09.png)

**Gabungan Subnet Kedua (Subnet C)**

- Penggabungan subnet B1 dan A1 menjadi C1
- Penggabungan subnet B2 dan A13 menjadi C2
- Penggabungan subnet B3 dan A16 menjadi C3
- Penggabungan subnet B4 dan A5 menjadi C4

![image](https://user-images.githubusercontent.com/34309557/203203185-cdb58712-7291-4b57-8f65-01fe1664d1d3.png)

**Gabungan Subnet Ketiga (Subnet D)**

- Penggabungan subnet C1 dan A2 menjadi D1
- Penggabungan subnet C2 dan A12 menjadi D2

![image](https://user-images.githubusercontent.com/34309557/203211722-0edfd18e-99d3-48c3-8576-216696be3c45.png)

**Gabungan Subnet Keempat (Subnet E)**

- Penggabungan subnet D1 dan A3 menjadi E1
- Penggabungan subnet D2, C3 dan A11 menjadi E2

![image](https://user-images.githubusercontent.com/34309557/203212828-7e0f2416-0420-44ef-b121-29cf0057df48.png)

**Gabungan Subnet Kelima (Subnet F)**

- Penggabungan subnet E1 dan A4 menjadi F1 
- Penggabungan subnet E2 dan A10 menjadi F2

![image](https://user-images.githubusercontent.com/34309557/203212619-b1114c1f-6de2-492f-9c03-5acda24d872f.png)

**Gabungan Subnet Keenam (Subnet G)**

- Penggabungan subnet F2 dan C4 menjadi G1

![image](https://user-images.githubusercontent.com/34309557/203212948-0de71d1f-9213-46c1-948b-2efd7edb6cdb.png)

**Gabungan Subnet Ketujuh (Subnet H)**

- Penggabungan subnet G1 dan F1 menjadi H1

![image](https://user-images.githubusercontent.com/34309557/203213091-3276f630-4ca3-44f5-8622-bdcbea3bfbb9.png)

### Pohon Pembagian IP

Setelah melakukan pembagian dan penggabungan subnet, pohon IP dapat dibuat dengan mula-mula memecah kembali satu subnet besar yang merupakan gabungan dari semua subnet yang ada.

![image](https://user-images.githubusercontent.com/34309557/203493507-c9ac7360-fbee-48c8-a29e-dee435cd3ac6.png)

Berikut ini adalah tabel pembagian IP berdasarkan pohon IP untuk setiap subnet.

|Subnet     |IP  Address    |Subnet Mask      |Netmask   |
|-          |-              |-                |-         |
|A1         |10.11.68.0     |255.255.252.0    |/22       |
|A2         |10.11.72.0     |255.255.255.252  |/30       |
|A3         |10.11.80.0     |255.255.255.192  |/26       |
|A4         |10.11.96.0     |255.255.255.252  |/30       |
|A5         |10.11.36.0     |255.255.255.252  |/30       |
|A6         |10.11.34.0     |255.255.255.252  |/30       |
|A7         |10.11.32.0     |255.255.254.0    |/23       |
|A8         |10.11.65.0     |255.255.255.252  |/30       |
|A9         |10.11.64.0     |255.255.255.0    |/24       |
|A10        |10.11.16.0     |255.255.255.252  |/30       |
|A11        |10.11.12.0     |255.255.255.128  |/25       |      
|A12        |10.11.4.0      |255.255.255.252  |/30       |
|A13        |10.11.2.0      |255.255.254.0    |/23       |
|A14        |10.11.0.0      |255.255.255.0    |/24       |
|A15        |10.11.1.0      |255.255.255.252  |/30       |
|A16        |10.11.9.0      |255.255.255.252  |/30       |
|A17        |10.11.8.128    |255.255.255.128  |/25       |
|A18        |10.11.8.0      |255.255.255.128  |/25       |

### Konfigurasi ETH pada Network Configuration

**TheResonance**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
address 10.11.96.1
netmask 255.255.255.252

auto eth2
iface eth2 inet static
address 10.11.36.1
netmask 255.255.255.252

auto eth3
iface eth3 inet static
address 10.11.34.1
netmask 255.255.255.252

auto eth4
iface eth4 inet static
address  10.11.16.1
netmask 255.255.255.252
```

**TheBeast**
```
auto eth0
iface eth0 inet static
address 10.11.36.2
netmask 255.255.255.252
gateway 10.11.36.1
```

**TheMagical**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.11.34.2
netmask 255.255.255.252
gateway 10.11.34.1

auto eth1
iface eth1 inet static
address 10.11.32.1
netmask 255.255.254.0
```

**Haines**
```
auto eth0
iface eth0 inet static
address 10.11.32.2
netmask 255.255.254.0
gateway 10.11.32.1
```

**Corvekt**
```
auto eth0
iface eth0 inet static
address 10.11.32.3
netmask 255.255.254.0
gateway 10.11.32.1
```

**TheOrder**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.11.96.2
netmask 255.255.252.252
address 10.11.96.1

auto eth1
iface eth1 inet static
address 10.11.80.1
netmask 255.255.252.192

auto eth2
iface eth2 inet static
address 10.11.72.1
netmask 255.255.255.252
```

**TheMinister**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.11.72.2
netmask 255.255.255.252
gateway 10.11.72.1

auto eth1
iface eth1 inet static
address 10.11.68.1
netmask 255.255.252.0

auto eth2
iface eth2 inet static
address 10.11.65.1
netmask 255.255.255.252
```

**Guideau***
```
auto eth0
iface eth0 inet static
address 10.11.68.2
netmask 255.255.252.0
gateway 10.11.68.1
```

**TheDauntless**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.11.65.2
netmask 255.255.255.252
gateway 10.11.65.1

auto eth1
iface eth1 inet static
address 10.11.64.1
netmask 255.255.255.0
```

**Phanora**
```
auto eth0
iface eth0 inet static
address 10.11.64.2
netmask 255.255.255.0
gateway 10.11.64.1
```

**Johan**
```
auto eth0
iface eth0 inet static
address 10.11.64.3
netmask 255.255.255.0
gateway 10.11.64.1
```

**TheInstrument**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.11.16.2
netmask 255.255.255.252
gateway 10.11.16.1

auto eth1
iface eth1 inet static
address 10.11.9.1
netmask 255.255.255.252

auto eth2
iface eth2 inet static
address 10.11.12.1
netmask 255.255.255.128

auto eth3
iface eth3 inet static
address 10.11.4.1
netmask 255.255.255.252
```

**MattCugas**
```
auto eth0
iface eth0 inet static
address 10.11.12.2
netmask 255.255.255.128
gateway 10.11.12.1
```

**TheProfound**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.11.9.2
netmask 255.255.255.252
gateway 10.11.9.1

auto eth1
iface eth1 inet static
address 10.11.8.128
netmask 255.255.255.129

auto eth2
iface eth2 inet static
address 10.11.8.1
netmask 255.255.255.128
```

**Spendrow**
```
auto eth0
iface eth0 inet static
address 10.11.8.130
netmask 255.255.255.128
gateway 10.11.8.129
```

**Helga**
```
auto eth0
iface eth0 inet static
address 10.11.8.2
netmask 255.255.255.128
gateway 10.11.8.1
```

**Firefist**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.11.4.2
netmask 255.255.255.252
gateway 10.11.4.1

auto eth1
iface eth1 inet static
address 10.11.2.1
netmask 255.255.254.0

auto eth2
iface eth2 inet static
address 10.11.0.1
netmask 255.255.255.0
```

## Kendala
