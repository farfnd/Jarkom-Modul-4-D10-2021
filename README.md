# Jarkom-Modul-4-D10-2021

## Anggota Kelompok D10
- Mohammad Faderik I H (05111940000023)
- Farhan Arifandi (05111940000061)
- Yusril Zubaydi (05111940000160)

## Topologi
![Topologi](https://media.discordapp.net/attachments/798177440425181256/914057022822051840/topologi.PNG?width=1207&height=701)

Kelompok kami menggunakan VLSM pada CPT dan CIDR pada GNS3

## VLSM - CPT
### Subnetting
Pembagian subnet dari topologi ini dapat dilihat sebagai berikut
![Topologi VLSM](https://media.discordapp.net/attachments/848199470025801749/914057920143060992/unknown.png?width=1167&height=701)

Untuk jumlah IP yang dibutuhkan setiap subnet diuraikan pada tabel dibawah ini.

| Subnet | Jumlah IP | Netmask |
|--------|-----------|---------|
| A1     | 101       | /25     |
| A2     | 2021      | /21     |
| A3     | 2         | /30     |
| A4     | 701       | /22     |
| A5     | 2         | /30     |
| A6     | 1001      | /22     |
| A7     | 2         | /30     |
| A8     | 2         | /30     |
| A9     | 521       | /22     |
| A10    | 502       | /23     |
| A11    | 13        | /28     |
| A12    | 2         | /30     |
| A13    | 252       | /24     |
| A14    | 2         | /30     |
| A15    | 721       | /22     |
| **Total**  | **5845**      | **/19**     |

Subnet besar yang akan digunakan memiliki NID dan netmask `10.26.0.0/19`. Perhitungan IP dari setiap subnet bisa dilihat pada gambar di bawah ini

![Pohon IP](https://media.discordapp.net/attachments/848199470025801749/914058155862929468/unknown.png)

Dari pohon tersebut dapat diuraikan pembagian IP tiap subnet dan dapat dilihat di tabel di bawah ini
|     |                   |                 |
|-----|-------------------|-----------------|
| A1  | Network ID        | 10.26.27.0      |
|     | Netmask           | 255.255.255.128 |
|     | Broadcast Address | 10.26.27.127    |
|     |                   |                 |
| A2  | Network ID        | 10.26.0.0       |
|     | Netmask           | 255.255.248.0   |
|     | Broadcast Address | 10.26.7.255     |
|     |                   |                 |
| A3  | Network ID        | 10.26.27.144    |
|     | Netmask           | 255.255.255.252 |
|     | Broadcast Address | 10.26.27.147    |
|     |                   |                 |
| A4  | Network ID        | 10.26.8.0       |
|     | Netmask           | 255.255.252.0   |
|     | Broadcast Address | 10.26.11.255    |
|     |                   |                 |
| A5  | Network ID        | 10.26.27.148    |
|     | Netmask           | 255.255.255.252 |
|     | Broadcast Address | 10.26.27.151    |
|     |                   |                 |
| A6  | Network ID        | 10.26.12.0      |
|     | Netmask           | 255.255.252.0   |
|     | Broadcast Address | 10.26.15.255    |
|     |                   |                 |
| A7  | Network ID        | 10.26.27.152    |
|     | Netmask           | 255.255.255.252 |
|     | Broadcast Address | 10.26.27.155    |
|     |                   |                 |
| A8  | Network ID        | 10.26.27.156    |
|     | Netmask           | 255.255.255.252 |
|     | Broadcast Address | 10.26.27.159    |
|     |                   |                 |
| A9  | Network ID        | 10.26.16.0      |
|     | Netmask           | 255.255.252.0   |
|     | Broadcast Address | 10.26.21.255    |
|     |                   |                 |
| A10 | Network ID        | 10.26.24.0      |
|     | Netmask           | 255.255.254.0   |
|     | Broadcast Address | 10.26.25.255    |
|     |                   |                 |
| A11 | Network ID        | 10.26.27.128    |
|     | Netmask           | 255.255.255.240 |
|     | Broadcast Address | 10.26.27.143    |
|     |                   |                 |
| A12 | Network ID        | 10.26.27.160    |
|     | Netmask           | 255.255.255.252 |
|     | Broadcast Address | 10.26.27.163    |
|     |                   |                 |
| A13 | Network ID        | 10.26.26.0      |
|     | Netmask           | 255.255.255.0   |
|     | Broadcast Address | 10.26.26.255    |
|     |                   |                 |
| A14 | Network ID        | 10.26.27.164    |
|     | Netmask           | 255.255.255.252 |
|     | Broadcast Address | 10.26.27.167    |
|     |                   |                 |
| A15 | Network ID        | 10.26.20.0      |
|     | Netmask           | 255.255.252.0   |
|     | Broadcast Address | 10.26.23.255    |

### Routing
Untuk routing pada CPT , akan diberikan static route pada semua router yang ada pada topologi tersebut yang diuraikan sebagai berikut

**Foosha**

```
10.26.27.0/25 via 10.26.27.150
10.26.0.0/21 via 10.26.27.150
10.26.8.0/22 via 10.26.27.150
10.26.20.0/22 via 10.26.27.158
10.26.26.0/24 via 10.26.27.158
10.26.27.160/30 via 10.26.27.158
10.26.27.128/28 via 10.26.27.158
10.26.24.0/23 via 10.26.27.158
10.26.16.0/22 via 10.26.27.158
10.26.27.164/30 via 10.26.27.158
10.26.27.144/30 via 10.26.27.150
```

**Water7**

```
0.0.0.0/0 via 10.26.27.149
10.26.27.0/25 via 10.26.27.146
10.26.0.0/21 via 10.26.27.146
```

**Pucci**

```
0.0.0.0/0 via 10.26.27.145
```

**Guanhao**

```
0.0.0.0/0 via 10.26.27.157
10.26.20.0/22 via 10.26.27.162
10.26.26.0/24 via 10.26.27.162
10.26.27.164/30 via 10.26.27.162
10.26.27.128/28 via 10.26.24.3
```

**Alabasta**

```
0.0.0.0/0 via 10.26.24.1
```

**Oimo**

```
0.0.0.0/0 via 10.26.27.161
10.26.20.0/22 via 10.26.26.3
```

**Seastone**

```
0.0.0.0/0 via 10.26.26.1
```

## CIDR - GNS3
### Topologi pada GNS3
![Topologi GNS3](https://user-images.githubusercontent.com/70105993/143677912-9986c511-ab52-4dd8-ab3b-d43461533da8.png)

### Subnetting
![image](https://user-images.githubusercontent.com/70105993/143676621-b285952a-4cfd-45e0-81e5-dcf9593cceff.png)

- B1: A1 + A3
- B2: A12 + A13
- B3: A10 + A11

![image](https://user-images.githubusercontent.com/70105993/143676637-139db206-73c4-44a7-9ec0-4401cbfafa40.png)

- C1: B1 + A4
- C2: B2 + A9
- C3: B3 + A8

![image](https://user-images.githubusercontent.com/70105993/143676666-4b46fe2e-89a2-445d-ba51-e942b707c4a6.png)

- D1: C1 + A2
- D2: C2 + C3

![image](https://user-images.githubusercontent.com/70105993/143676688-89912f27-939c-47d8-b54f-c35bd5279887.png)

- E1: D1 + A5
- E2: D2 + A7

![image](https://user-images.githubusercontent.com/70105993/143676708-c3ba3fa5-3bf1-43c3-a545-e0e1fd19a51f.png)

- F1: E2 + A6

![image](https://user-images.githubusercontent.com/70105993/143676734-7670a87b-9fbc-48ff-b676-820f5fbce010.png)

- G1: E1 + F1

![image](https://user-images.githubusercontent.com/70105993/143676749-2de6e05e-49af-4f4b-b32c-f0c70ed0bf7d.png)

Subnet besar yang digunakan memiliki NID dan netmask `10.26.0.0/16`. Perhitungan IP dari setiap subnet bisa dilihat pada gambar berikut.

![Pohon IP CIDR](https://user-images.githubusercontent.com/70105993/143676771-6ab5a1c9-aea9-4721-9643-7bfe19ab7a44.png)


Dari pohon tersebut dapat diuraikan pembagian IP tiap subnet dan dapat dilihat pada tabel berikut.

|                     |                   |                 |
|---------------------|-------------------|-----------------|
| A1 (/25)            | Network ID        | 10.26.8.0       |
| Jipangu - Pucci     | Netmask           | 255.255.255.128 |
|                     | Broadcast Address | 10.26.8.127     |
|                     |                   |                 |
| A2 (/22)            | Network ID        | 10.26.32.0      |
| Cipher - Water7     | Netmask           | 255.255.252.0   |
|                     | Broadcast Address | 10.26.35.255    |
|                     |                   |                 |
| A3 (/21)            | Network ID        | 10.26.0.0       |
| Pucci - Courtyard   | Netmask           | 255.255.248.0   |
| - Calmbelt          | Broadcast Address | 10.26.7.255     |
|                     |                   |                 |
| A4 (/30)            | Network ID        | 10.26.16.0      |
| Pucci - Water7      | Netmask           | 255.255.255.252 |
|                     | Broadcast Address | 10.26.16.3      |
|                     |                   |                 |
| A5 (/30)            | Network ID        | 10.26.64.0      |
| Foosha - Water7     | Netmask           | 255.255.255.252 |
|                     | Broadcast Address | 10.26.64.3      |
|                     |                   |                 |
| A6 (/22)            | Network ID        | 10.26.192.0     |
| Blueno - Foosha     | Netmask           | 255.255.252.0   |
|                     | Broadcast Address | 10.26.195.255   |
|                     |                   |                 |
| A7 (/30)            | Network ID        | 10.26.160.0     |
| Foosha - Guanhao    | Netmask           | 255.255.255.252 |
|                     | Broadcast Address | 10.26.160.3     |
|                     |                   |                 |
| A8 (/22)            | Network ID        | 10.26.152.0     |
| Guanhao - Jabra     | Netmask           | 255.255.252.0   |
|                     | Broadcast Address | 10.26.155.255   |
|                     |                   |                 |
| A9 (/30)            | Network ID        | 10.26.136.0     |
| Guanhao - Oimo      | Netmask           | 255.255.255.252 |
|                     | Broadcast Address | 10.26.136.3     |
|                     |                   |                 |
| A10 (/23)           | Network ID        | 10.26.144.0     |
| Guanhao - Maingate  | Netmask           | 255.255.254.0   |
| - Alabasta          | Broadcast Address | 10.26.145.255   |
|                     |                   |                 |
| A11 (/28)           | Network ID        | 10.26.148.0     |
| Alabasta - Jorge    | Netmask           | 255.255.255.240 |
|                     | Broadcast Address | 10.26.148.15    |
|                     |                   |                 |
| A12 (/24)           | Network ID        | 10.26.132.0     |
| Oimo - EniesLobby   | Netmask           | 255.255.255.0   |
| - Seastone          | Broadcast Address | 10.26.132.255   |
|                     |                   |                 |
| A13 (/22)           | Network ID        | 10.26.128.0     |
| Seastone - Elena    | Netmask           | 255.255.252.0   |
|                     | Broadcast Address | 10.26.131.255   |
|                     |                   |                 |
| (/30)               | Network ID        | 151.63.10.0     |
| Foosha - Doriki     | Netmask           | 255.255.255.252 |
|                     | Broadcast Address | 151.63.10.3     |
|                     |                   |                 |
| (/30)               | Network ID        | 151.100.10.0    |
| Oimo - Fukurou      | Netmask           | 255.255.255.252 |
|                     | Broadcast Address | 151.100.10.3    |

## Kendala selama pengerjaan
- Sempat gagal melakukan ping ke server pada CPT (VLSM)
- Sempat ragu apakah server dijadikan subnet sendiri atau tidak ketika melakukan pembagian subnet untuk metode CIDR
- its.ac.id tidak dapat di-ping baik menggunakan console di dalam GNS3 maupun command prompt dari sistem operasi (di luar GNS3)
