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

Subnet besar yang akan digunakan memiliki NID dan netmask `10.26.0.0/19`. Perhitungan IP dari setiap subnet bisa dilihat pada gambar dibawah ini

![Pohon IP](https://media.discordapp.net/attachments/848199470025801749/914058155862929468/unknown.png)

Dari pohon tersebut dapat diuraikan pembagian IP tiap subnet dan dapat dilihat di tabel dibawah ini
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

**Water 7**

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

