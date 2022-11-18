# ChainFLIP

​[​<img src="https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg) [Twitter BeritaCryptoo](https://twitter.com/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png) [Telegram BeritaCryptoo](https://t.me/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png) [Discord BeritaCryptoo](https://discord.gg/beritacryptoonode)​

<figure><img src=".gitbook/assets/kdt_AgmT_400x400 (2).png" alt=""><figcaption></figcaption></figure>

### Official Link

* [Discord](https://discord.gg/C3AfDPVBKP)
* [Twitter](https://twitter.com/chainflip)
* [Telegram](https://t.me/chainflip\_io\_chat)
* [Docs](https://docs.chainflip.io/perseverance-validator-documentation/)

### Minimum Requirements

> OS: **Ubuntu 20.04** - <mark style="color:red;">**HANYA BISA DI UBUNTU 20.04**</mark>&#x20;
>
> * CPU: 4 GHz | 4+ Cores, Dedicated is better
> * RAM: 8 GB SSD: 50 GB (this may increase over time)&#x20;
> * Bandwidth: Recommended 1GBps connection, 100 GB bandwidth combined up/down per month

### 1. Port

```
sudo ufw allow 22 & sudo ufw allow 30333/tcp && sudo ufw allow 8078/tcp && sudo ufw enable
```

### 2. Create User

**Add user `flip`**

```
sudo useradd -s /bin/bash -d /home/flip/ -m -G sudo flip 
```

**Add password**

```
sudo passwd flip
```

> Masukan password baru yang mudah diingat, samakan dengan password VPS mu atau tanggal lahir terserah. **YANG PENTING JANGAN LUPA**
