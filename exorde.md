# Exorde

## Cara Install menggunakan Docker

#### Install Docker

```
sudo apt update -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt install docker-ce
```

#### Download Bahan

```
git clone https://github.com/exorde-labs/ExordeModuleCLI.git
```

#### Install

```
cd ExordeModuleCLI
docker build -t exorde-cli . 
```

Tunggu sampai selesai

#### Jalankan Screen dan mulai Node

```
docker run -d --restart unless-stopped --pull always --name exorde-cli rg.fr-par.scw.cloud/exorde-labs/exorde-cli -m Address0x -l 2
```

```
docker logs -f exorde-cli
```

Ganti `Address0x` dengan address metamask mu(WalletBaru)

Contoh:

> docker run -d --restart unless-stopped --pull always --name exorde-cli rg.fr-par.scw.cloud/exorde-labs/exorde-cli -m 0x0000000000000000000000000000000000DEAD -l 2

#### Tonton

Di tunggu bisa, close juga bisa…. Gunakan `CTRL+C` untuk close, untuk cek kembali gunakan

```
docker logs -f exorde-cli
```
