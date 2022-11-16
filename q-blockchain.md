---
description: Guide Testnet Q-Blockchain
---

# Q-Blockchain

​[​<img src="https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/184274157-08210464-fa03-493d-b01c-2420c67a524f.jpg) [Twitter BeritaCryptoo](https://twitter.com/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png) [Telegram BeritaCryptoo](https://t.me/BeritaCryptoo) [​<img src="https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png" alt="" data-size="line">​](https://user-images.githubusercontent.com/108946833/201040868-61a5cfb9-f39e-4fd1-a3a6-2c15c1b47424.png) [Discord BeritaCryptoo](https://discord.gg/beritacryptoonode)​

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FrZRFGN2QiovDTgE9l85j%2Flogo.898c322b.png?alt=media&#x26;token=3a47114a-7e70-4728-b6a1-cd87d775feb9" alt=""><figcaption></figcaption></figure>

#### Official Link <a href="#official-link" id="official-link"></a>

* ​[Discord](https://discord.gg/FWV7SAG5nM)​
* ​[Guide](https://docs.qtestnet.org/how-to-setup-validator/)​
* ​[Gitlab](https://gitlab.com/q-dev)​
* ​[Reddit](https://www.reddit.com/r/QBlockchain/)​
* ​[Explorer](https://explorer.qtestnet.org/)​
* ​[Medium](https://medium.com/q-blockchain)​
* ​[Faucet](https://faucet.qtestnet.org/)​
* ​[Cek Validator](https://stats.qtestnet.org/)​

#### Setup Awal <a href="#setup-awal" id="setup-awal"></a>

```
wget -O qb.sh https://raw.githubusercontent.com/Megumiiiiii/q-blochchain/main/qb.sh && chmod +x qb.sh && ./qb.sh
```

#### Membuat Password Wallet <a href="#membuat-password-wallet" id="membuat-password-wallet"></a>

```
cd ~/testnet-public-tools/testnet-validator
nano keystore/pwd.txt
```

> * Buatlah password yang mudah diingat, 8 digit
> * Simpan, CTRL+X Y Enter

#### Create Wallet <a href="#create-wallet" id="create-wallet"></a>

```
docker run --entrypoint="" --rm -v $PWD:/data -it qblockchain/q-client:testnet geth account new --datadir=/data --password=/data/keystore/pwd.txt
```

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FxtMzhzWyqteU5sr4utgl%2FScreenshot_1.png?alt=media&#x26;token=214e86ec-3c8c-4219-9f1a-5d569d9f3c9a" alt=""><figcaption></figcaption></figure>

#### Claim Faucet <a href="#claim-faucet" id="claim-faucet"></a>

Klaim faucet menngunakan addressmu: [DISINI](https://faucet.qtestnet.org/)​

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FvQKStaT0SRuLqpZTXxCg%2FScreenshot_3.png?alt=media&#x26;token=10fa6577-5745-4358-a16f-d8051191ba0f" alt=""><figcaption></figcaption></figure>

Error ? Spam bang

#### Edit .env <a href="#edit-.env" id="edit-.env"></a>

nano .env

> Edit pada bagianADDRESS=Addressmu tanpa 0x&#x20;
>
> IP=IP VPS mu
>
> Contoh:

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FkVPTziNWXkIbSME9kOuK%2FScreenshot_4.png?alt=media&#x26;token=25fd2f6b-a0dd-47e2-9075-7e27326bb5fa" alt=""><figcaption></figcaption></figure>

Simpan

#### Edit config.json <a href="#edit-config.json" id="edit-config.json"></a>

nano config.json

> Edit pada bagian"address": "addressmu tanpa ox", "password": "passwordmu yang dibuat di step awal",Contoh:

Simpan

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FRY5MOGgYwVS2POnor2sI%2FScreenshot_5.png?alt=media&#x26;token=6690d9df-b354-41ed-b91e-ad4fd7a888f9" alt=""><figcaption></figcaption></figure>

#### Stake ke Contract <a href="#stake-ke-contract" id="stake-ke-contract"></a>

```
docker run --rm -v $PWD:/data -v $PWD/config.json:/build/config.json qblockchain/js-interface:testnet validators.js
```

**Okay !**

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2Fm1m9bQOIH0G3TCr77hOp%2FScreenshot_6.png?alt=media&#x26;token=8b26db7a-d16c-4300-bd39-a296152a8c35" alt=""><figcaption></figcaption></figure>

#### Mendaftar <a href="#mendaftar" id="mendaftar"></a>

**Edit file dulu**

```
nano docker-compose.yaml
```

> Pada bagian setelah `"geth"` tambahkan

&#x20;"--ethstats=NAMA\_VALIDATOR:qstats-testnet@stats.qtestnet.org",​

> Contoh

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2Fjy0ohmTYoDmNmwSwiE5o%2FScreenshot_9.png?alt=media&#x26;token=de977f52-300c-41ef-a4a1-d0860c79c239" alt=""><figcaption></figcaption></figure>

#### Jalankan NODE <a href="#jalankan-node" id="jalankan-node"></a>

```
docker compose up -d
```

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2FvW2zc0gkbpbKts26ddRx%2FScreenshot_12.png?alt=media&#x26;token=6f87d9d7-758a-4b6d-98db-439f8c65af96" alt=""><figcaption></figcaption></figure>

#### Cek LOGS <a href="#cek-logs" id="cek-logs"></a>

```
cd ~/testnet-public-tools/testnet-validator
docker compose logs -f
```

<figure><img src="https://580801350-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FyjqqGlG6vZEVZjseIV1U%2Fuploads%2F8cbem56BfMlHTa3qmTIx%2FScreenshot_13.png?alt=media&#x26;token=28d40140-e1bc-494b-85d1-a2369a67d1d6" alt=""><figcaption></figcaption></figure>

* Untuk keluar dari sesi logs gunakan `CTRL+C` atau `CTRL+Z`

#### Cek Nama Validator Kalian <a href="#cek-nama-validator-kalian" id="cek-nama-validator-kalian"></a>

[Q Network Status](https://stats.qtestnet.org/)

#### ​ <a href="#undefined" id="undefined"></a>
