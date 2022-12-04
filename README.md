# <p align="center"> Tutorial Exorde Incentivized Tesnet </p>

<p style="font-size:14px" align="left">
<a href="https://t.me/Pepoy_Crypto" " target="_blank" rel="nofollow">Join Telegram kami <img width="20" height="auto" src="https://github.com/mrfastes/datablog/blob/main/photo_2022-09-17_07-05-40.jpg" </a>
</p>
<p style="font-size:14px" align="left">
<a href="https://twitter.com/mrfastes" target="_blank"> Follow My twitter
</p>
<p style="font-size:14px" align="left">
<a href="https://exorde.network/" target="_blank">Exorde Web
</p>

 
  
<p align="center">
  <img width="30%" height="auto" src="https://github.com/mrfastes/datablog/blob/main/tXqjiR3t_400x400.jpg">
</p>

# Exorde Tesnet

|  Komponen |  Persyaratan Minimum |
| ------------ | ------------ |
| CPU  | 2 core  |
| RAM | 4 GB  |
| Penyimpanan  | 50 GB HDD |

## Pemasangan menggunakan Docker
### Ikuti Step by Step
1
```
apt update
```
2
```
apt install git
```
3
```
apt install apt-transport-https ca-certificates software-properties-common curl
```
4
```
curl -f -s -S -L https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
5
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```
6
```
apt update
```
7
```
cd /root
```
8
```
sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y
```
9
```
sudo systemctl status docker
```

### Cek Versi Docker
```
docker --version
```
> Jika muncul pesan seperti ini `Docker version xxx.xxxx` artinya Docker sudah terpasang, jika tidak muncul silahkan install kembali dockernya

### Unduh paket Exorde
```
git clone https://github.com/exorde-labs/ExordeModuleCLI.git
```
### Jalankan Docker

```
docker run \
-d \
--restart unless-stopped \
--pull always \
--name exorde-cli \
exordelabs/exorde-cli \
-m <alamat eth kalian> \
-l 2
```
contoh:
```
docker run \
-d \
--restart unless-stopped \
--pull always \
--name exorde-cli \
exordelabs/exorde-cli \
-m 0xA1E4976c74D012494d7DB515aBb8B3f9B4c3CC93 \
-l 2
```
> Ganti `<alamat eth kalian>` dengan alamat eth kamu, untuk logging bisa 1-4 
> disini saya sarankan menggunakan logging 2
## Logging
| Logging level | Keterangan |
|---------------|------------|
|0|Tidak ada log|
|1|Log biasa|
|2|Log validasi|
|3|Log validasi dan scrapping|
|4|Log validasi (detail) + log scrapping 


## Note : Jika error dan Rep/Poin tidak bertambah Silahkan hapus dan install ulang docker anda
