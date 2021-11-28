# Jarkom-Modul-4-E15-2021
M. Iqbal Abdi (05111940000151)

## VLSM
### Topologi
![image](https://user-images.githubusercontent.com/75016595/143725050-77978f72-bb3b-42ec-b3cb-61cb0ee4a9f9.png)

Pada CPT akan digunakan metode VLSM dalam penerapan pembagian IP

### Pembagian IP
![vlsm-tree](images/vlsm-vlsm.drawio.png)

Pembagian IP dilakukan dengan tree diatas, sehingga menghasilkan IP sebagai berikut.
```txt
A1
Network ID : 10.29.27.0
Netmask    : 255.255.255.128
Broadcast  : 10.29.27.127
A2
Network ID : 10.29.0.0
Netmask    : 255.255.248.0
Broadcast  : 10.29.7.255
A3
Network ID : 10.29.27.144
Netmask    : 255.255.255.252
Broadcast  : 10.29.27.147
A4
Network ID : 10.29.16.0
Netmask    : 255.255.252.0
Broadcast  : 10.29.19.255
A5
Network ID : 10.29.27.148
Netmask    : 255.255.255.252
Broadcast  : 10.29.27.151
A6
Network ID : 10.29.8.0
Netmask    : 255.255.252.0
Broadcast  : 10.29.11.255
A7
Network ID : 10.29.27.152
Netmask    : 255.255.255.252
Broadcast  : 10.29.27.155
A8
Network ID : 10.29.27.156
Netmask    : 255.255.255.252
Broadcast  : 10.29.27.159
A9
Network ID : 10.29.20.0
Netmask    : 255.255.252.0
Broadcast  : 10.29.23.255
A10
Network ID : 10.29.27.160
Netmask    : 255.255.255.252
Broadcast  : 10.29.27.163
A11
Network ID : 10.29.26.0
Netmask    : 255.255.255.0
Broadcast  : 10.29.26.255
A12
Network ID : 10.29.12.0
Netmask    : 255.255.252.0
Broadcast  : 10.29.15.255
A13
Network ID : 10.29.27.164
Netmask    : 255.255.255.252
Broadcast  : 10.29.27.167
A14
Network ID : 10.29.24.0
Netmask    : 255.255.254.0
Broadcast  : 10.29.25.255
A15
Network ID : 10.29.27.128
Netmask    : 255.255.255.240
Broadcast  : 10.29.27.143
```

### Routing
* **Foosha**
```txt
Network 10.29.16.0 Netmask 255.255.252.0 Next Hop 10.29.27.150
Network 10.29.27.0 Netmask 255.255.255.128 Next Hop 10.29.27.150
Network 10.29.27.144 Netmask 255.255.255.252 Next Hop 10.29.27.150
Network 10.29.0.0 Netmask 255.255.248.0 Next Hop 10.29.27.150
Network 10.29.20.0 Netmask 255.255.252.0 Next Hop 10.29.27.158
Network 10.29.24.0 Netmask 255.255.254.0 Next Hop 10.29.27.158
Network 10.29.27.128 Netmask 255.255.255.240 Next Hop 10.29.27.158
Network 10.29.27.160 Netmask 255.255.255.252 Next Hop 10.29.27.158
Network 10.29.27.164 Netmask 255.255.255.252 Next Hop 10.29.27.158
Network 10.29.26.0 Netmask 255.255.255.0 Next Hop 10.29.27.158
Network 10.29.12.0 Netmask 255.255.252.0 Next Hop 10.29.27.158
```

* **Water7**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 10.29.27.149
Network 10.29.27.0 Netmask 255.255.255.128 Next Hop 10.29.27.146
Network 10.29.0.0 Netmask 255.255.248.0 Next Hop 10.29.27.146
```

* **Pucci**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 10.29.27.145
```

* **Guanhao**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 10.29.27.157
Network 10.29.27.128 Netmask 255.255.255.240 Next Hop 10.29.24.2
Network 10.29.27.164 Netmask 255.255.255.252 Next Hop 10.29.27.162
Network 10.29.26.0 Netmask 255.255.255.0 Next Hop 10.29.27.162
Network 10.29.12.0 Netmask 255.255.252.0 Next Hop 10.29.27.162
```

* **Alabasta**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 10.29.24.1
```

* **Oimo**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 10.29.27.161
Network 10.29.12.0 Netmask 255.255.252.0 Next Hop 10.29.26.2
```

* **Seastone**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 10.29.26.1
```

## CIDR
### Topologi
![cidr](images/Jarkom4-GNS3.png)

Untuk CIDR, saya menggunakan GNS3 untuk penerapannya. Untuk subnet terkecilnya, sama dengan VLSM

### Pembagian IP
Pembagian IP dilakukan dengan cara mengelompokkan subnet-subnet kecil menjadi subnet besar. Untuk pengelompokkannya seperti berikut.
* Subnet B
![subnet-b](images/cidr-2-step-1.png)
* Subnet C
![subnet-c](images/cidr-2-step-2.png)
* Subnet D
![subnet-d](images/cidr-2-step-3.png)
* Subnet E
![subnet-e](images/cidr-2-step-4.png)
* Subnet F
![subnet-f](images/cidr-2-step-5.png)

Pada pengelompokkan subnet di atas, didapatkan subnet root /19. Pengelompokkan di atas tidak termasuk server, sehingga perlu ditambahkan pada pembagian IP, sehingga tree-nya akan seperti ini.
![cidr-tree](images/cidr-2-cidr-revisi.png)

Pembagian IP tersebut menghasilkan IP berikut.
```txt
A1
Network ID : 10.29.8.0 
Netmask    : 255.255.255.128
Broadcast  : 10.29.8.127
A2
Network ID : 10.29.0.0 
Netmask    : 255.255.248.0
Broadcast  : 10.29.7.255
A3
Network ID : 10.29.16.0 
Netmask    : 255.255.255.252
Broadcast  : 10.29.16.3
A4
Network ID : 10.29.32.0 
Netmask    : 255.255.252.0
Broadcast  : 10.29.35.255
A5
Network ID : 10.29.64.0 
Netmask    : 255.255.255.252
Broadcast  : 10.29.64.3
A6
Network ID : 10.29.192.0 
Netmask    : 255.255.252.0
Broadcast  : 10.29.195.255
A7
Network ID : 10.92.196.0 
Netmask    : 255.255.255.252
Broadcast  : 10.29.196.3
A8
Network ID : 10.29.160.0 
Netmask    : 255.255.255.252
Broadcast  : 10.29.160.3
A9
Network ID : 10.29.144.0 
Netmask    : 255.255.252.0
Broadcast  : 10.29.147.255
A10
Network ID : 10.29.136.0 
Netmask    : 255.255.255.252
Broadcast  : 10.29.136.3
A11
Network ID : 10.29.132.0 
Netmask    : 255.255.255.0
Broadcast  : 10.29.132.255
A12
Network ID : 10.29.128.0 
Netmask    : 255.255.252.0
Broadcast  : 10.29.131.255
A13
Network ID : 10.29.133.0 
Netmask    : 255.255.255.252
Broadcast  : 10.29.133.3
A14
Network ID : 10.29.128.0 
Netmask    : 255.255.254.0
Broadcast  : 10.29.129.255
A15
Network ID : 10.29.150.0 
Netmask    : 255.255.255.240
Broadcast  : 10.29.150.15
```

### Routing
* **Foosha**
```txt
-net 10.29.0.0 netmask 255.255.128.0 gw 10.29.64.2
-net 10.29.128.0 netmask 255.255.128.0 gw 10.29.160.2
```

* **Water7**
```txt
-net 0.0.0.0 netmask 0.0.0.0 gw 10.29.64.1
-net 10.29.8.0 netmask 255.255.255.128 gw 10.29.160.2
-net 10.29.0.0 netmask 255.255.248.0 gw 10.29.160.2
```

* **Pucci**
```txt
-net 0.0.0.0 netmask 0.0.0.0 gw 10.29.160.1
```

* **Guanhao**
```txt
-net 0.0.0.0 netmask 0.0.0.0 gw 10.29.160.1
-net 10.29.150.0 netmask 255.255.255.240 gw 10.29.148.2
-net 10.29.128.0 netmask 255.255.240.0 gw 10.29.136.2
```

* **Alabasta**
```txt
-net 0.0.0.0 netmask 0.0.0.0 gw 10.29.148.1
```

* **Oimo**
```txt
-net 0.0.0.0 netmask 0.0.0.0 gw 10.29.136.1
-net 10.29.128.0 netmask 255.255.252.0 gw 10.29.132.2
```

* **Seastone**
```txt
-net 0.0.0.0 netmask 0.0.0.0 gw 10.29.132.1
```
