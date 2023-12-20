# Jarkom-Modul-5-IT05-2023

Yohannes Hasahatan Tua Alexandro - 5027211022

Arkan Hendri Abdul Ghani Burhan - 5027211026


## Topologi
Pada modul kali ini, kami diarahkan untuk membuat topologi di gns3 seperti berikut

![topologi](https://github.com/yohanneslex/Jarkom-Modul-5-IT05-2023/assets/50076171/f387bcb4-b035-4147-87a6-489a2dac5743)


## Subnetting GNS3


## Tree VLSM
Dengan menggunakan perhitangan metode VLSM, didapatkan tree sebagai berikut

![treeVSLM](https://github.com/yohanneslex/Jarkom-Modul-5-IT05-2023/assets/50076171/9a3ea832-3db5-4bf3-8831-60be9885270b)


## Tabel Rute VLSM
Berdasarkan tree tersebut, didapatkan rute dalam bentuk tabel terhadap perhitungan VLSM sebagai berikut

![ruteVLSM](https://github.com/yohanneslex/Jarkom-Modul-5-IT05-2023/assets/50076171/85718289-0c89-409c-90f8-b4deab9b545a)


## Perhitungan IP VLSM
Berdasarkan tree dan tabel rute, kami mendapatkan hasil perhitungan IP dengan menggunakan VLSM sebagai berikut

![ipVLSM](https://github.com/yohanneslex/Jarkom-Modul-5-IT05-2023/assets/50076171/632873df-0a54-4d36-a0c7-298f50c023cf)


## Network Configuration
1. Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.66.14.149
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.66.14.145
	netmask 255.255.255.252

#Menerima 

#Mengirim 

#A9
route add -net 10.66.0.0 netmask 255.255.248.0 gw 10.66.14.150
#A10
route add -net 10.66.8.0 netmask 255.255.252.0 gw 10.66.14.150
#A5 
route add -net 10.66.14.136 netmask 255.255.255.252 gw 10.66.14.146
#A6
route add -net 10.66.14.140 netmask 255.255.255.252 gw 10.66.14.146
#A4
route add -net 10.66.12.0 netmask 255.255.255.252 gw 10.66.14.146
#A3
route add -net 10.66.14.0 netmask 255.255.255.252 gw 10.66.14.146
#A2
route add -net 10.66.14.132 netmask 255.255.255.252 gw 10.66.14.146
#A1
route add -net 10.66.14.128 netmask 255.255.255.252 gw 10.66.14.146
```

2. Heiter
```
auto eth0
iface eth0 inet static
	address 10.66.14.150
	netmask 255.255.255.252
  gateway 10.66.14.149

auto eth1
iface eth1 inet static
	address 10.66.0.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 10.66.8.1
	netmask 255.255.252.0


#menerima 
#aura(a8)
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.66.14.149
```

3. Turk Region
```
auto eth0
iface eth0 inet static
	address 10.66.0.2
	netmask 255.255.248.0
  gateway 10.66.0.1
```

4. Sein
```
auto eth0
iface eth0 inet static
	address 10.66.8.2
	netmask 255.255.252.0
  gateway 10.66.8.1
```

5. GroberForest
```
auto eth0
iface eth0 inet static
	address 10.66.8.3
	netmask 255.255.252.0
  gateway 10.66.8.1
```

6. Frieren
```
auto eth0
iface eth0 inet static
	address 10.66.14.146
	netmask 255.255.255.252
  gateway 10.66.14.145

auto eth1
iface eth1 inet static
	address 10.66.14.141
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.66.14.137
	netmask 255.255.255.252

#Menerima 
#aura(A7)
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.66.14.145

#Mengirim 
#A4
route add -net 10.66.12.0 netmask 255.255.254.0 gw 10.66.14.138
#A3
route add -net 10.66.14.0 netmask 255.255.255.128 gw 10.66.14.138
#A2
route add -net 10.66.14.132 netmask 255.255.255.252 gw 10.66.14.138
#A1
route add -net 10.66.14.128 netmask 255.255.255.252 gw 10.66.14.138
```

7. Stark
```
auto eth0
iface eth0 inet static
	address 10.66.14.142
	netmask 255.255.255.252
  gateway 10.66.14.141
```

8. Himmel
```
auto eth0
iface eth0 inet static
	address 10.66.14.138
	netmask 255.255.255.252
  gateway 10.66.14.137

auto eth1
iface eth1 inet static
	address 10.66.12.1
	netmask 255.255.254.0

auto eth2
iface eth2 inet static
	address 10.66.14.1
	netmask 255.255.255.128

#menerima 
#Frieren(A5)
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.66.14.137

#Mengirim 
#A1
route add -net 10.66.14.128 netmask 255.255.255.252 gw 10.66.14.2
#A2
route add -net 10.66.14.132 netmask 255.255.255.252 gw 10.66.14.2
```

9. Laubhills
```
auto eth0
iface eth0 inet static
	address 10.66.12.2
	netmask 255.255.254.0
  gateway 10.66.12.1
```

10. SchewerMountain
```
auto eth0
iface eth0 inet static
	address 10.66.14.3
	netmask 255.255.255.128
  gateway 10.66.14.1
```

11. Fern
```
auto eth0
iface eth0 inet static
	address 10.66.14.2
	netmask 255.255.255.128
  gateway 10.66.14.1

auto eth1
iface eth1 inet static
	address 10.66.14.133
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.66.14.129
	netmask 255.255.255.252

#menerima 
#himmel(A3)
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.66.14.1

```

12. Richter
```
auto eth0
iface eth0 inet static
	address 10.66.14.134
	netmask 255.255.255.252
    gateway 10.66.14.133
```

13. Revolte
```
auto eth0
iface eth0 inet static
	address 10.66.14.130
	netmask 255.255.255.252
  gateway 10.66.14.129
```

## Set Up DHCP
1. dhcpd.conf pada node Revolte
```
subnet 10.66.14.128 netmask 255.255.255.252 {
   option routers 10.66.14.129;
}
#A2
subnet 10.66.14.132 netmask 255.255.255.252 {
  
}
#A5
subnet 10.66.14.136 netmask 255.255.255.252 {
   option routers 10.66.14.137;
}
#A6
subnet 10.66.14.140 netmask 255.255.255.252 {
  
}
#A7
subnet 10.66.14.144 netmask 255.255.255.252 {
   option routers 10.66.14.145;
}
#A8
subnet 10.66.14.148 netmask 255.255.255.252 {
    option routers 10.66.14.150;
}


#laubhils
subnet 10.66.12.0 netmask 255.255.254.0 {
    range 10.66.12.2 10.66.13.1;
    option routers 10.66.12.1;
    option broadcast-address 10.66.13.255;
    option domain-name-servers 10.66.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}
#schwermountain
subnet 10.66.14.0 netmask 255.255.255.128 {
    range 10.66.14.3 10.66.14.66;
    option routers 10.66.14.1;
    option broadcast-address  10.66.14.127;
    option domain-name-servers 10.66.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}
#turkregion
subnet 10.66.0.0 netmask 255.255.248.0 {
    range 10.66.0.2 10.66.4.4;
    option routers 10.66.0.1;
    option broadcast-address  10.66.7.255;
    option domain-name-servers 10.66.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}
#Grobforest
subnet 10.66.8.0 netmask 255.255.252.0 {
    range 10.66.8.3 10.66.10.5;
    option routers 10.66.8.1;
    option broadcast-address  10.66.11.255;
    option domain-name-servers 10.66.14.134;
    default-lease-time 720;
    max-lease-time 5760;
}

```

2. DHCP pada -isc-dhcp-relay
```
SERVERS="10.66.14.130"  
INTERFACES="eth0 eth1 eth2"
OPTIONS=
```

## Pembahasan

### Soal 1
Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.

### Jawaban 1
Buat bash baru dengan nama aura.sh dengan isi berikut

```
ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')

iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP
```

Agar dapat mengakses internet tambahkan juga dns pada setiap node dengan cara
```
echo '
nameserver 192.168.122.1
' > /etc/resolv.conf
```

### Soal 2
Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.

### Jawaban 2
Jalankan syntax dibawah ini untuk menyelesaikan permasalahan di atas

```
# Drop semua koneksi UDP
iptables -A INPUT -p udp -j DROP

# Drop semua koneksi TCP kecuali port 8080
iptables -A INPUT -p tcp ! --dport 8080 -j DROP
iptables -A INPUT -p tcp -j DROP
```

### Soal 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Jawaban 3
Setting dahulu DNS dan DHCP server, setelah itu jalankan syntax berikut
```
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

### Soal 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

### Jawaban 4

jalankan syntax berikut untuk menyelesaikan permsalahan tersebut:
```
# di Node Sein
# Mengizinkan port 22 yang digunakan sebagai SSH pada IP range
iptables -A INPUT -p tcp --dport 22 -m iprange --src-range 10.66.8.3-10.66.10.5 -j ACCEPT

# Drop port 22 agar tidak bisa SSH selain pada IP range
iptables -A INPUT -p tcp --dport 22 -j DROP

```

### Soal 5
Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Jawaban 5

jalankan syntax berikut untuk menyelesaikan permsalahan tersebut:
```
# Batasi akses inteernet menuju Webserver pada waktu tertentu
iptables -A INPUT -p tcp --dport 80 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT

# Jika diluar waktu yang ditentukan drop akses internet
iptables -A INPUT -p tcp --dport 80 -j DROP
```

### Soal 6
Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Jawaban 6


### Soal 7
Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Jawaban 7


### Soal 8
Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Jawaban 8


### Soal 9
Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. (clue: test dengan nmap)


### Jawaban 9


### Soal 10
Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level. 

### Jawaban 10









