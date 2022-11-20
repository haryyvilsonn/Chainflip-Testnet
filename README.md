<h1 align="center">Chainflip Testneti Kurulum Rehberi

## Chainflip Testneti için Kurulum Rehberi. Sağ üstten yıldızlayıp forklamayı unutmayalım. Sorularınız olursa: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/202866596-c418882c-cd8a-4344-9a67-11e645d9fb37.png)


## Sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Testnet | 4         | 8         | 200*  |

`*` -> Resmi dokümanda 50 GB olarak belirtilmiş fakat zaman geçtikçe yetersiz kalmaya başlayacaktır.

## Chainflip için önemli linkler:
- [Website](https://chainflip.io/)
- [Explorer](https://blocks-perseverance.chainflip.io/)
- [Twitter](https://twitter.com/Chainflip)
- [Discord](https://discord.gg/2B5w7FXK8h)

# 1) Birçok şeyi manuel girmeniz gerektiği için script yazmak anlamsız olacaktı, direkt manuel kuruyoruz.

## Kuruluma başlayalım. Sunucuyu güncelleyelim.

```
sudo apt update && sudo apt upgrade -y
```

## Chainflip GPG key'lerini indirelim.

```
sudo mkdir -p /etc/apt/keyrings
curl -fsSL repo.chainflip.io/keys/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/chainflip.gpg
```

## Aşağıdaki komutu girdiğinizde görseldeki gibi bir çıktı vermesi gerekir.

```
gpg --show-keys /etc/apt/keyrings/chainflip.gpg
```

![image](https://user-images.githubusercontent.com/101462877/202867259-10cff82e-59ab-4afe-9fcf-833b853a8040.png)


## Chainflip için gerekli kurulumları `apt` ile indirilebilir hale getirelim.

```
echo "deb [signed-by=/etc/apt/keyrings/chainflip.gpg] https://repo.chainflip.io/perseverance/ focal main" | sudo tee /etc/apt/sources.list.d/chainflip.list
```


## Chainflip paketlerini yükleyelim.

```
sudo apt-get update
sudo apt-get install -y chainflip-cli chainflip-node chainflip-engine
```

## Chainflip anahtarları oluşturalım.

```
sudo mkdir /etc/chainflip/keys
```

## [Discord](https://discord.gg/2B5w7FXK8h)'a giderek test token alalım, hazırda bulunsun.


- BOŞ CÜZDANINIZ İÇİN FAUCET KULLANIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZ İLE HERHANGİ BİR TESTNET'TE ETKİLEŞİME GİRMEYİN.

- BOŞ CÜZDANINIZ İÇİN FAUCET KULLANIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZ İLE HERHANGİ BİR TESTNET'TE ETKİLEŞİME GİRMEYİN.

- BOŞ CÜZDANINIZ İÇİN FAUCET KULLANIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZ İLE HERHANGİ BİR TESTNET'TE ETKİLEŞİME GİRMEYİN.

- BOŞ CÜZDANINIZ İÇİN FAUCET KULLANIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZ İLE HERHANGİ BİR TESTNET'TE ETKİLEŞİME GİRMEYİN.

- BOŞ CÜZDANINIZ İÇİN FAUCET KULLANIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZ İLE HERHANGİ BİR TESTNET'TE ETKİLEŞİME GİRMEYİN.

```
!drip <TESTNETLER İÇİN KULLANDIĞINIZ METAMASK ADRESİ>
```

![image](https://user-images.githubusercontent.com/101462877/202867811-4dc1d3d0-2b53-44f8-8575-f90102976510.png)

![image](https://user-images.githubusercontent.com/101462877/202867827-fa85100d-b63a-4ef3-920a-6142123fb7ff.png)


## Ayrıca Chainflip testnetinde stake işlemleri sırasında gas fee için minimum 0.1 GoerliETH bulundurduğunuza emin olun, [Goerli Faucet](https://goerlifaucet.com)'e giderek alabilirsiniz.



# BURADAN İTİBAREN DİKKATLİ İLERLEMENİZİ ÖNERİYORUM. METAMASK PRIVATE KEY EKLEYECEĞİZ FALAN ÇÜNKÜ

## Aşağıdaki komut için tırnak içerisine metamask cüzdanımızın private key'ini yazıyoruz. 

- BOŞ CÜZDANINIZIN PRIVATE KEY'İNİ YAZIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZIN PRIVATE KEY'İNİ ASLA YAZMAYIN.
- BOŞ CÜZDANINIZIN PRIVATE KEY'İNİ YAZIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZIN PRIVATE KEY'İNİ ASLA YAZMAYIN.
- BOŞ CÜZDANINIZIN PRIVATE KEY'İNİ YAZIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZIN PRIVATE KEY'İNİ ASLA YAZMAYIN.
- BOŞ CÜZDANINIZIN PRIVATE KEY'İNİ YAZIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZIN PRIVATE KEY'İNİ ASLA YAZMAYIN.
- BOŞ CÜZDANINIZIN PRIVATE KEY'İNİ YAZIN, İÇİNDE VARLIK BULUNAN CÜZDANINIZIN PRIVATE KEY'İNİ ASLA YAZMAYIN.


## Hocam tırnak siliyo muyuz hocam nası yapıştırıyosunuz sorularını şimdiden cevaplıyorum, görsele bakabilirsiniz.
```
echo -n "YOUR_VALIDATOR_WALLET_PRIVATE_KEY" |  sudo tee /etc/chainflip/keys/ethereum_key_file
```

![image](https://user-images.githubusercontent.com/101462877/202867745-49177b81-20bf-444d-b72c-e2bbf6a79bb1.png)


## Chainflip için signing anahtarları oluşturalım. Bu komutun ardından aldığınız çıktı aşağıdaki görseldeki gibi olmalıdır. Bu çıktının tamamını bir yere KAYDETTİĞİNİZDEN emin olun.

```
chainflip-node key generate
```
![image](https://user-images.githubusercontent.com/101462877/202868256-36063de3-e008-4024-8700-2e7480a37c3c.png)

## Ardından signing anahtarımızı yüklüyoruz. Değiştirmeniz gereken kısmı görsellerle belirtiyorum.

```
SECRET_SEED=<YUKARIDA KAYDETTİĞİNİZ BİLGİLER İÇERİSİNDEN SECRET SEED'İNİZ>
```

![image](https://user-images.githubusercontent.com/101462877/202868521-d1109d58-b9c2-421c-a97d-2487da6fcfaf.png)

![image](https://user-images.githubusercontent.com/101462877/202868538-b678c3a2-e640-4acb-8471-f39a7c1982d6.png)

## Ardından aşağıdaki komutları sırayla olduğu gibi yapıştırıyoruz.

```
echo -n "${SECRET_SEED:2}" | sudo tee /etc/chainflip/keys/signing_key_file
```
```
sudo chainflip-node key generate-node-key --file /etc/chainflip/keys/node_key_file
```
```
sudo chmod 600 /etc/chainflip/keys/ethereum_key_file
sudo chmod 600 /etc/chainflip/keys/signing_key_file
sudo chmod 600 /etc/chainflip/keys/node_key_file
history -c
```

# Ardından Alchemy üzerinde birkaç işlem yapıp oradan bazı bilgiler alacağız.

## [Alchemy](https://dashboard.alchemy.com/) üzerinde hesabınız yoksa hesap açıyoruz. 

## Bir isim girip `Create App` diyelim. Ağ olarak Goerli'yi seçtiğinize emin olun.

![image](https://user-images.githubusercontent.com/101462877/202868778-92196590-fd55-4f5e-a0f6-0a09f97264ae.png)

## Oluşturduğumuz App için `View key`'e tıklayalım. Kutucukla gösterdiğim `https` ve `wss` ile başlayanları bir yere kopyalayalım. 

![image](https://user-images.githubusercontent.com/101462877/202868859-6a43fb06-65ea-467d-8c4b-bb8cd44cb219.png)

## Terminale geri dönelim. Aşağıdaki komutları girelim.

```
sudo mkdir -p /etc/chainflip/config
sudo nano /etc/chainflip/config/Default.toml
```

## Aşağıdaki komutta değiştirmemiz gereken yerleri değiştirelim, ardından açılan sayfaya yapıştıralım.

```
# Default configurations for the CFE
[node_p2p]
node_key_file = "/etc/chainflip/keys/node_key_file"
ip_address="<CHAINFLIP KURDUĞUMUZ SUNUCUNUN IP ADRESİNİZ>"
port = "8078"

[state_chain]
ws_endpoint = "ws://127.0.0.1:9944"
signing_key_file = "/etc/chainflip/keys/signing_key_file"

[eth]
# Ethereum RPC endpoints (websocket and http for redundancy).
ws_node_endpoint = "<ALCHEMY'DEN ALDIĞINIZ WSS İLE BAŞLAYAN KISIM>"
http_node_endpoint = "<ALCHEMY'DEN ALDIĞINIZ HTTPS İLE BAŞLAYAN KISIM>"

# Ethereum private key file path. This file should contain a hex-encoded private key.
private_key_file = "/etc/chainflip/keys/ethereum_key_file"

[signing]
db_file = "/etc/chainflip/data.db"
```

- `<CHAINFLIP KURDUĞUMUZ SUNUCUNUN IP ADRESİNİZ>:` Sunucunuzun IP adresi
- `<ALCHEMY'DEN ALDIĞINIZ WSS İLE BAŞLAYAN KISIM>:` Alchemy'den aldığınız wss ile başlayan kısım
- `<ALCHEMY'DEN ALDIĞINIZ HTTPS İLE BAŞLAYAN KISIM>:` Alchemy'den aldığınız https ile başlayan kısım

# Son görünüm aşağıdaki görselde gibi olduktan sonra; Ctrl+X , Y ve Enter'a basıp sayfayı kapatın.

![image](https://user-images.githubusercontent.com/101462877/202869083-9c060b45-1f23-411c-b50b-18d4d0bacfba.png)


## Node'umuzu başlatalım. Güncel bloğa ulaştıktan sonra devam edelim. GÜNCEL BLOĞA ULAŞMADAN DEVAM ETMEYELİM.
            
```
sudo systemctl start chainflip-node
tail -f /var/log/chainflip-node.log
```
            
Güncel Blok: [Explorer](https://blocks-perseverance.chainflip.io/)
            
![image](https://user-images.githubusercontent.com/101462877/202870551-4e4d5198-b6e7-44a7-b706-8c735cc72b10.png)
            
            
## Node'umuz GÜNCEL BLOĞA ULAŞTIKTAN SONRA  Chainflip Engine'i başlatacağız. Sırasıyla komutları girelim.
            
```
sudo systemctl start chainflip-engine
```
            
```
sudo systemctl enable chainflip-node
```
```
sudo systemctl enable chainflip-engine
```
Log'lara bakalım.
```
tail -f /var/log/chainflip-engine.log
```
            
# Node'umuzu kurduk. Şimdi test tokenlarımızı stake edelim. [Chainflip Stake](https://stake-perseverance.chainflip.io/) sayfasına giderek private key'ini kullandığımız metamask cüzdanını bağlıyoruz.
            
![image](https://user-images.githubusercontent.com/101462877/202871128-72384ce7-e484-4371-8f6f-65fe080335e7.png)
            
## `Add node`'a tıklayalım ve daha öncesinde kenara not ettiğimiz `Validator Public Key`'i yazalım, stake miktarını max yapalım.
            
Hocam nerede bu Validator Public Key derseniz, bir alttaki görsele bakın.
    
![image](https://user-images.githubusercontent.com/101462877/202871237-4716ceb7-0dd3-43c2-9fde-86a9b33aaf66.png)
 
![image](https://user-images.githubusercontent.com/101462877/202871202-df11d000-9a3a-4cde-b399-1d2a61467b2d.png)

## Bir süre geçtikten sonra staking sayfasında node'unuz görünecektir, NODE GÖRÜNDÜKTEN SONRA devam ediyoruz.
            
![image](https://user-images.githubusercontent.com/101462877/202896547-ecb17a97-920b-4351-ad13-072cadc85d6e.png)

## Ardından validator anahtarını register ediyoruz. Öncelikle aşağıdaki komutu girelim. Yes/no sorusuna `y` diyip enter'lıyoruz.
            
```
sudo chainflip-cli \
      --config-path /etc/chainflip/config/Default.toml \
      register-account-role Validator
```            
![image](https://user-images.githubusercontent.com/101462877/202896510-e0e983b8-e071-4317-910e-73a44a76a122.png)

## Sonrasında bize bir tx veriyor, [Explorer]()'a giderek tx'in durumuna bakabiliriz.
            
![image](https://user-images.githubusercontent.com/101462877/202896591-22a71e87-4b80-4979-83eb-2ab7f236ff0b.png)
            
            
## Son olarak sırasıyla aşağıdaki komutlar ile devam edelim.
           
```
sudo chainflip-cli \
    --config-path /etc/chainflip/config/Default.toml \
    activate
``` 
            
```
sudo chainflip-cli \
    --config-path /etc/chainflip/config/Default.toml rotate
``` 
            
## Validatorunuze isim vermek isterseniz:
           
```
sudo chainflip-cli \
    --config-path /etc/chainflip/config/Default.toml \
    vanity-name <VALIDATOR ADI>
``` 
