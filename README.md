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
- Penggabungan subnet D2 dan C3 menjadi E2


**Gabungan Subnet Kelima (Subnet F)**

- Penggabungan subnet E1 dan A4 menjadi F1 
- Penggabungan subnet E2 dan A10 menjadi F2

![image](https://user-images.githubusercontent.com/34309557/203212619-b1114c1f-6de2-492f-9c03-5acda24d872f.png)

**Gabungan Subnet Keenam (Subnet G)**





## Kendala
