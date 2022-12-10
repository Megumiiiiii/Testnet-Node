# Starknet

<figure><img src=".gitbook/assets/STRAKNNNN.jpg" alt=""><figcaption></figcaption></figure>

### Minimum Requirements

| CPU | RAM |  Storage  |
| :-: | :-: | :-------: |
|  4  | 8GB | SSD 100GB |

### Official Link

* [Discord](http://starknet.io/discord)
* [Twitter](https://twitter.com/StarkWareLtd)
* [Explorer](https://voyager.online/)

### 1. Register Alchemy

* [DISINI](https://alchemy.com/?r=8d1e5ee5ec1f9c0c)

### 2. Buat App&#x20;

**a. Pilih Ethereum Mainnet**

<figure><img src=".gitbook/assets/alchemy mainnrt.png" alt=""><figcaption></figcaption></figure>

**b. Masuk ke App**

**c. Pilih View Key**

**d. Salin HTTPS , simpan di Notepad**

<figure><img src=".gitbook/assets/Salin ini.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
<mark style="color:green;">**Ethereum Mainnet**</mark> jangan sampai salah
{% endhint %}

Lanjut ke VPS

### 3. Install Docker

```
sudo apt update -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt install docker-ce
```

### 4. Install Alat

```
sudo apt-get install -y pkg-config curl git build-essential libssl-dev screen
```

### 5. Download Bahan

```
git clone --branch v0.4.0 https://github.com/eqlabs/pathfinder.git
```

### 6. Mulai

```
mkdir -p $HOME/pathfinder
docker run -d \
  --rm \
  -p 9545:9545 \
  --user "$(id -u):$(id -g)" \
  -e RUST_LOG=info \
  --name starknet \
  -e PATHFINDER_ETHEREUM_API_URL="XXXXXXXXXXXXX" \
  -v $HOME/pathfinder:/usr/share/pathfinder/data \
  eqlabs/pathfinder
```

{% hint style="danger" %}
<mark style="color:red;">**XXXXXXXXXXXX**</mark>  diganti dengan link `HTTPS` mu dari alchemy
{% endhint %}

Contoh:

> mkdir -p $HOME/pathfinder docker run -d\
> \--rm\
> \-p 9545:9545\
> \--user "$(id -u):$(id -g)"\
> \-e RUST\_LOG=info\
> \--name starknet\
> \-e PATHFINDER\_ETHEREUM\_API\_URL="https://eth-mainnet.g.alchemy.com/v2/HE50Y4MAEZ4KM1-ud4465hs6"\
> \-v $HOME/pathfinder:/usr/share/pathfinder/data\
> eqlabs/pathfinder

<figure><img src=".gitbook/assets/WOKE.png" alt=""><figcaption></figcaption></figure>

### 7. Cek logs

```
docker logs -f starknet
```

**OKAY!**

<figure><img src=".gitbook/assets/Screenshot from 2022-11-22 13-53-29.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Nunggu sync lama, cek blocks terkini

* [DISINI](https://voyager.online/)
{% endhint %}

### 8. Screenshot

**a. Screenshot Dashboard Alchemy**

harusnya udah ada angka2 disana

<figure><img src=".gitbook/assets/Screenshot from 2022-11-22 13-43-04.png" alt=""><figcaption></figcaption></figure>

**b. Post ke Twitter**

**c. Salin link tweet nya**

**d. Kirim ke Discord** `#✅｜full-node-success`

* Kata- kata mutiara
* IP VPS
* Link tweet
* Screenshot

<figure><img src=".gitbook/assets/2022-11-22_13-45.png" alt=""><figcaption></figcaption></figure>
