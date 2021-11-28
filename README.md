# Jarkom-Modul-4-E15-2021
M. Iqbal Abdi (05111940000151)

## VLSM
### Topologi
![image](https://user-images.githubusercontent.com/75016595/143725109-337e9be0-6bf4-4075-a5de-2fdc588f85fb.png)


Pada CPT akan digunakan metode VLSM dalam penerapan pembagian IP

### Pembagian IP
![image](https://user-images.githubusercontent.com/75016595/143725110-fa18ffc7-2c30-4516-8ec5-eec9a70621c0.png)

### Konfigurasi Routing
* **Foosha**
```txt
Network 192.207.12.0 Netmask 255.255.252.0 Next Hop 192.207.27.149
Network 192.207.27.0 Netmask 255.255.255.128 Next Hop 192.207.27.149
Network 192.207.0.0 Netmask 255.255.248.0 Next Hop 192.207.27.149
Network 192.207.12.144 Netmask 255.255.255.252 Next Hop 192.207.27.149
Network 192.207.16.0 Netmask 255.255.252.0 Next Hop 192.207.27.154
Network 192.207.27.156 Netmask 255.255.255.252 Next Hop 192.207.27.154
Network 192.207.20.0 Netmask 255.255.252.0 Next Hop 192.207.27.154
Network 192.207.26.0 Netmask 255.255.255.0 Next Hop 192.207.27.154
Network 192.207.27.128 Netmask 255.255.255.240 Next Hop 192.207.27.154
Network 192.207.24.0 Netmask 255.255.254.0 Next Hop 192.207.27.154
Network 192.207.27.164 Netmask 255.255.255.252 Next Hop 192.207.27.154
```

* **Water7**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.207.27.150
Network 192.207.27.0 Netmask 255.255.255.128 Next Hop 192.207.27.146
Network 192.207.0.0 Netmask 255.255.248.0 Next Hop 192.207.27.146
```

* **Pucci**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.207.27.145
```

* **Guanhao**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.207.27.153
Network 192.207.27.128 Netmask 255.255.255.240 Next Hop 192.207.24.2
Network 192.207.26.0 Netmask 255.255.255.0 Next Hop 192.207.27.158
Network 192.207.20.0 Netmask 255.255.252.0 Next Hop 192.207.27.158
Network 192.207.27.164 Netmask 255.255.255.252 Next Hop 192.207.27.158
```

* **Alabasta**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.207.24.1
```

* **Oimo**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.207.27.157
Network 192.207.20.0 Netmask 255.255.252.0 Next Hop 192.207.26.2
```

* **Seastone**
```txt
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.207.26.1
```

## CIDR
### Topologi
![image](https://user-images.githubusercontent.com/75016595/143725467-becbc207-bf7b-42c2-8715-e59bb6e0ddc6.png)

Pada CPT akan digunakan metode CIDR dalam penerapan pembagian IP

### Pembagian IP
Pembagian IP dilakukan dengan cara mengelompokkan subnet-subnet kecil menjadi subnet besar. Untuk pengelompokkannya seperti berikut.
* Subnet B
![image](https://user-images.githubusercontent.com/75016595/143725694-734627cf-3528-4329-897e-985f308ac59c.png)  
* Subnet C
![image](https://user-images.githubusercontent.com/75016595/143725701-8c2c01fb-f3de-41ff-8476-7734455b5e32.png)  
* Subnet D
![image](https://user-images.githubusercontent.com/75016595/143725703-b9f12fb2-38cb-4967-9729-c0179665df43.png)  
* Subnet E
![image](https://user-images.githubusercontent.com/75016595/143725709-cfe1eb89-a395-4944-ab53-5683a0d4d967.png)  
* Subnet F dan G
![image](https://user-images.githubusercontent.com/75016595/143725714-27a14207-363d-4bae-91dd-80b3c7479bbc.png)  

Pada pengelompokkan subnet di atas, didapatkan subnet root /19. Pengelompokkan di atas tidak termasuk server, sehingga perlu ditambahkan pada pembagian IP, sehingga tree-nya akan seperti ini.
![image](https://user-images.githubusercontent.com/75016595/143725734-f25ad8a7-11b5-473f-9f12-6faabff0c5b3.png)


### Routing
* **Foosha**
```txt
route add -net 10.7.128.0 netmask 255.255.128.0 gw  10.7.192.2
route add -net 10.7.0.0 netmask 255.255.128.0 gw 10.7.32.2
```

* **Water7**
```txt
route add -net 10.7.128.0 netmask 255.255.192.0 gw 10.7.144.2
```

* **Guanhao**
```txt
route add -net 10.7.0.0 netmask 255.255.240.0 gw 10.7.8.2
route add -net 10.7.16.0 netmask 255.255.248.0 gw 10.7.16.3
```

* **Oimo**
```txt
route add -net 10.7.0.0 netmask 255.255.252.0 gw 10.7.4.3
```
