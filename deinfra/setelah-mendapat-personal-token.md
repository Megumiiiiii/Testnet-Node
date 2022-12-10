# Setelah Mendapat Personal Token

### Install Keperluan

```
sudo apt update; sudo apt upgrade
sudo apt install curl wget gnupg apt-transport-https -y
```

```
curl -fsSL https://packages.erlang-solutions.com/ubuntu/erlang_solutions.asc | sudo gpg --dearmor -o /usr/share/keyrings/erlang.gpg
```

```
echo "deb [signed-by=/usr/share/keyrings/erlang.gpg] https://packages.erlang-solutions.com/ubuntu $(lsb_release -cs) contrib" | sudo tee /etc/apt/sources.list.d/erlang.list
```

```
sudo apt update

sudo apt install erlang-base erlang-public-key erlang-ssl
```

### Download Tea Client

```
wget https://tea.thepower.io/teaclient

chmod +x teaclient
```

### Membuat Folder Baru

```
mkdir {db,log}
mkdir /root/log/deinfra; mkdir /root/db/deinfra
```

### Download Docker Images

```
docker pull thepowerio/tpnode
```

{% hint style="info" %}
<mark style="color:blue;">**Note**</mark>: Baru bisa mulai setelah mendapat Chain Token dari mereka
{% endhint %}
