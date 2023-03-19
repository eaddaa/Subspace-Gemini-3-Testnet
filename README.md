<h1 align="center">Subspace Gemini 3 Testneti Kurulum Rehberi

## Helo, ödülsüz olduğu belirtilen Subspace Gemini 3 Testneti için kurulum yapacağız. Sağ üstten yıldızlayıp forklamayı unutmayalım. Sorularınız olursa: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/226185548-0a877428-60b7-4bf6-96c3-bab3b6d8f758.png)
  
## Minimum sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Testnet | 4          | 4         | 150GB yeterli  |


## Subspace için önemli linkler:
- [Website](https://subspace.network/)
- [Telemetry](https://telemetry.subspace.network/#list/0xab946a15b37f59c5f4f27c5de93acde9fe67a28e0b724a43a30e4fe0e87246b7)
- [Subscan](https://subspace.subscan.io/)
- [Twitter](https://twitter.com/NetworkSubspace)
- [Discord](https://discord.gg/APGKbgn5nT)
  
# Kuruluma başlayalım. Öncelikle polkadot.js cüzdanına ihtiyacımız olacak. Daha öncesinde node kurduysanız o wallet ile devam edebilirsiniz, bu adımı atlayın.

[Polkadot.js](https://polkadot.js.org/extension/) sayfasına gidiyoruz. Polkadotjs cüzdanı eklenti olarak indiriyoruz. Hesap açıp verdiği kelimeleri bir yere kaydediyoruz.
  
  <img width="1440" alt="Ekran Resmi 2023-03-19 18 13 24" src="https://user-images.githubusercontent.com/101462877/226185668-f3cac5d2-9a9f-427d-bf23-52adacb480b6.png">


# Terminalimize geliyoruz ve aşağıdaki komutları sırayla yapıştırıyoruz.


```
sudo su
cd $HOME
```

```
screen -S gemini
```
  
```
sudo apt update && sudo apt upgrade -y
```
  
```
sudo apt install wget ocl-icd-libopencl1 screen libopencl-clang-dev libgomp1 ocl-icd-opencl-dev -y
```
  
```
wget https://github.com/subspace/subspace-cli/releases/download/v0.1.9-alpha/subspace-cli-ubuntu-x86_64-v0.1.9-alpha
```
  
```
chmod +x subspace-cli-ubuntu-x86_64-v0.1.9-alpha
```
  
```
./subspace-cli-ubuntu-x86_64-v0.1.9-alpha init
``` 
   
## Bu noktada sırasıyla `Subspace adresiniz`, `node adınız`, `Enter`,  `Enter`, `Enter` giriyoruz veya tıklıyoruz.

<img width="1032" alt="Ekran Resmi 2023-03-19 18 37 20" src="https://user-images.githubusercontent.com/101462877/226187029-1c22c119-7f08-4565-99ec-72f9c9e760e9.png">

```
./subspace-cli-ubuntu-x86_64-v0.1.9-alpha farm
``` 
  
## Node'u başlattık, sync olması bir süre alır.
  
  <img width="1027" alt="Ekran Resmi 2023-03-19 18 45 05" src="https://user-images.githubusercontent.com/101462877/226187496-fb614a0e-7d59-4659-99d0-e64b069240aa.png">

# Ardından Ctrl + A + D tıklayarak screen'den çıkabilirsiniz. Screen'i silmeyin, node durur.
  
# Daha sonrasında node'un durumunu kontrol etmek için terminale `screen -r gemini` yazabilirsiniz.

# `No journal files were found` hatası verirse alttaki komutu girip log komutunu tekrar deneyin:
```
systemctl restart systemd-journald.service
```

# Node'unuz çalışmaya başladıktan bir süre sonra [Telemetry](https://telemetry.subspace.network/#list/0xab946a15b37f59c5f4f27c5de93acde9fe67a28e0b724a43a30e4fe0e87246b7)'de node adınız ile aratabilirsiniz.
  
  
# Sorularınız ve merak ettikleriniz için: 
  
- Telegram: [LossNode Chat](https://t.me/LossNode)
- Discord: [Cryptoloss](https://discord.gg/bJZA4NyPjz)

