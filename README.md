# Jarkom_Modul4_Lapres_T04

## T4

## Fachrizal Rahmat Hidayat /05311840000005

## Faza Murtadho            /05311840000034


# Cisco Packet Tracer (VLSM)

Membuat Topologi seperti soal

![Soal Shift Modul 4](https://user-images.githubusercontent.com/55182321/101979863-4fb43000-3c93-11eb-9e5d-f58579fab160.png)

## Subneting 

Melabeli masing masing netmask dan menghitung ip yang dibutuhkan

![gambar](https://user-images.githubusercontent.com/55182321/101979953-247e1080-3c94-11eb-854a-ee6026edfec3.png)

Menghitung pembangian IP berdasarkan NID dan netmask

![gambar](https://user-images.githubusercontent.com/55182321/101980312-006ffe80-3c97-11eb-8f1d-36cd38c90ad2.png)

Untuk server menggunakan IP DMZ 

![gambar](https://user-images.githubusercontent.com/55182321/101980797-99ecdf80-3c9a-11eb-92a4-59dd40575dfe.png)

## Pembagian IP

Melabeli pada topologi

![gambar](https://user-images.githubusercontent.com/55182321/101980612-31e9c980-3c99-11eb-97f7-756d794165ef.png)
![gambar](https://user-images.githubusercontent.com/55182321/101980639-69587600-3c99-11eb-9731-360f0e1f54e3.png)

Mengatur IP pada setiap interface di setiap router server dan client berdasarkan subnet yang telah di tentukan tadi seperti contoh pada gambar dibawah

### Router
![gambar](https://user-images.githubusercontent.com/55182321/101980814-c43e9d00-3c9a-11eb-9e66-baec73e1bd5b.png)

### Server
![gambar](https://user-images.githubusercontent.com/55182321/101981118-26000680-3c9d-11eb-9306-e4a95d9de252.png)

### Client
![gambar](https://user-images.githubusercontent.com/55182321/101981142-5d6eb300-3c9d-11eb-8a23-6d6d329c804a.png)

## Routing 

Melakukan routing pada setiap router menuju subnet subnet yang "tidak dikenal"

![gambar](https://user-images.githubusercontent.com/55182321/102004773-3ae4a480-3d46-11eb-9226-886cb9992e9b.png)
![gambar](https://user-images.githubusercontent.com/55182321/102004874-513f3000-3d47-11eb-9fd2-e7b7f4649669.png)
![gambar](https://user-images.githubusercontent.com/55182321/102004792-813a0380-3d46-11eb-8904-5996b5265a18.png)
![gambar](https://user-images.githubusercontent.com/55182321/102004929-cdd20e80-3d47-11eb-88a4-31bc0eb7e006.png)
![gambar](https://user-images.githubusercontent.com/55182321/102004941-daeefd80-3d47-11eb-8f8f-8e67c9fdf0d8.png)
![gambar](https://user-images.githubusercontent.com/55182321/102004959-ea6e4680-3d47-11eb-85a0-34cc5c115150.png)
![gambar](https://user-images.githubusercontent.com/55182321/102004967-f5c17200-3d47-11eb-8566-157df057a91c.png)


# UML (CIDR)
Membuat Topologi seperti pada CPT untuk gambaran, dan menambahkan router di stiap antara router

![gambar](https://user-images.githubusercontent.com/55182321/101984714-c6622500-3cb5-11eb-9534-1ab2b53631f6.png)
![gambar](https://user-images.githubusercontent.com/55182321/101984726-dc6fe580-3cb5-11eb-89f5-c703a1e2acf7.png)



## Subneting 

Gabungkan label subnet menjadi satu subnet yang lebih besar (dimulai dari yang paling jauh)

![gambar](https://user-images.githubusercontent.com/55182321/101981935-f5bb6680-3ca2-11eb-9f67-4826912c3fd9.png)

Dari gambar di atas kita sudah mengetahui subnet terbesar yaitu /16 , dan membagi berdasarkan pembagian subnet yang telah dilakukan di atas

![gambar](https://user-images.githubusercontent.com/55182321/101982017-7a0de980-3ca3-11eb-9b25-d29d79f30b28.png)

## Routing

Masukan IP pada `/etc/network/interfaces` sesuai dengan interface nya 

### router

Pada router setelah memasukan IP sesuai dengan interfacenya, masukan juga 

`post-up route add -net [NETWORK] netmask [SUBNET] gw [GATEWAY]` Untuk menambahkan route saat uml di booting

`post-down route del -net [NETWORK] netmask [NETMASK] gw [GATEWAY]` Untuk menghapus route saat uml di matikan

pada setiap interface yang dilewati oleh routing

![gambar](https://user-images.githubusercontent.com/55182321/102005216-b136d600-3d49-11eb-9197-5197c6d86cdb.png)

### server
![gambar](https://user-images.githubusercontent.com/55182321/102005383-fc9db400-3d4a-11eb-8205-d928bf8a8e17.png)

### client
![gambar](https://user-images.githubusercontent.com/55182321/102005438-66b65900-3d4b-11eb-98b5-7b92ce4ff6cb.png)


Untuk mengecek hasil routing menggunakan route -n pada setiap router

![gambar](https://user-images.githubusercontent.com/55182321/102005527-f825cb00-3d4b-11eb-9070-568110bcb7fd.png)

![gambar](https://user-images.githubusercontent.com/55182321/102005580-73877c80-3d4c-11eb-9a6b-e4735ceff008.png)

![gambar](https://user-images.githubusercontent.com/55182321/102005592-8d28c400-3d4c-11eb-80b4-c0e418aedd13.png)

![gambar](https://user-images.githubusercontent.com/55182321/102005636-f0b2f180-3d4c-11eb-9ab6-097752ca7545.png)

![gambar](https://user-images.githubusercontent.com/55182321/102005645-04f6ee80-3d4d-11eb-9621-62f0f10db2b3.png)

![gambar](https://user-images.githubusercontent.com/55182321/102005712-9a927e00-3d4d-11eb-9fd4-be5240a95230.png)

![gambar](https://user-images.githubusercontent.com/55182321/102005725-b85fe300-3d4d-11eb-928d-d30dc4385aca.png)
