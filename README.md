# Jarkom-Modul-1-C15-2021

## Soal 11

```
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
```

**Filter capture: src port 80**

Screenshot:
![](./img/11.png)

## Soal 12

```
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

```

**Filter capture: port 21**

Screenshot:
![](./img/12.png)

## Soal 13

```
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
```

Filter display: **tcp**.dstport == 443 || udp.dstport == 443

Screenshot:
![](./img/13.png)

## Soal 14

```
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
```

Filter capture: dst host kemenag.go.id

Screenshot:
![](./img/14.png)

## Soal 15

```
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
```

IP komputer pribadi saat itu adalah **192.168.100.5**
Filter capture: src host 192.168.100.5

Screenshot:
![](./img/15.png)
