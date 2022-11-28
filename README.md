<h1 align="center">Manta Network Trusted Setup Güncelleme

  ## Güvenilir kurulumların açıklaması ve Manta Network'te oynadıkları rol için [buraya](https://docs.manta.network/docs/concepts/TrustedSetup) bakın . Katılım talimatları için okumaya devam edin.
  
 ![image](https://docs.manta.network/img/guides/trusted-setup-stages.svg)

## Manta Network için minimum kurulum gereksinimleri belirtilmemiştir. Aşağıdaki rehberden digital ocean veya google cloud ile en düşük sunucuları kiralayıp kurabilirsiniz.
  
   # Daha önce Node kurulumu yapmadıysanız buradan sırasıyla adımları takip ederek tüm süreci öğrenebilirsiniz.
  ## Yeni Başladım Rehberi; [Pusula Finans Labs.](https://www.labs.pusulafinans.com/category/rehber/)
  ### 1. [Testnet ve Node test kurulum rehberi Bölüm-1](https://www.labs.pusulafinans.com/2022/08/23/testnet-ve-node-kurulum-rehberi/)
  ### 2. [Yeni Chrome Tarayıcı nasıl açarım?](https://www.labs.pusulafinans.com/2022/08/23/yeni-chrome-tarayici-nasil-acarim/)
  ### 3. [Ücretsiz Sunucu Kiralama](https://www.labs.pusulafinans.com/2022/08/23/nasil-ucretsiz-sunucu-kiralarim/)
  ### 4. [Digital Ocean Nasıl Kayıt olurum?](https://www.labs.pusulafinans.com/2022/08/23/digital-oceana-nasil-kayit-olabilirim/)
  ### 5. [MobaXTerm Terminal Kurulumu](https://www.labs.pusulafinans.com/2022/08/23/mobaxterm-terminal-kurulumu/)

 
  
  # 1. adımda Manta kurulumu otomatik script ile kurulumunu paylaşalım sorun yaşarsanız manuel kurulum kısmına geçebilirsiniz.
  
  
  ## Root yetkisi alalım.
  ```
  sudo su
  cd
  ```
  
 ## Sunucumuzu güncelleyelim
  
  ```
 sudo apt update && sudo apt upgrade -y
  ```
  
 ## Ardından bu komu ile çalıştırıyoruz.
  
 ```
sudo apt install pkg-config build-essential libssl-dev curl jq
 ```
 
  ## Rust Yükleme
 ```
curl https://sh.rustup.rs/ -sSf | sh -s -- -y
 ```
 ## Kaynağını belirtelim;
   ```
source $HOME/.cargo/env
 ```

 ## Gtihubdan dosyasını indirelim
 ```
git clone https://github.com/Manta-Network/manta-rs.git
 ```

 ## Yeni bir screen oluşturalım
 ```
sudo apt install screen
 ```
 ```
screen -S mantatestnet
 ``` 

 ## Manta klasörüne giriş yapıyoruz;
 ```
cd manta-rs
 ```
 
 ## Contribution kodunu girelim

 ```
cargo run --release --all-features --bin groth16_phase2_client contribute
 ``` 
  
 ## Yukarıdaki kodu girdikten sonra aşağıdaki gibi bir ekran sizi karşılayacak. Daha önce [Manta-Network-Trusted-Setup](https://github.com/pusulafinanslabs/Manta-Network-Trusted-Setup) kurulumunu yaptığınızda size verilen anahtar kelimeleri bu bölümde giriyoruz.
  
  
  ![image](https://docs.manta.network/assets/images/ts_guide_secret_prompt-a51b0113ad8b979fb1cf9f23d46cd42e.png)
  
### Tek yapmanız gereken anahtar kelimeleri girdikten sonra, gerisi otomatik olarak çalışacaktır. Muhtemelen şuna benzer bir katkı kuyruğuna yerleştirileceksiniz:
  
   ![image](https://docs.manta.network/assets/images/ts_guide_queue-6b351fe8be3332c1b7cb382f5547ce8d.png)
  
Bu noktada yapmanız gereken hiçbir şey yok; sadece bu süreç devam ederken bekleyin ve sıranız geldiğinde otomatik olarak katkıda bulunacaksınız. Bu görevi kapatırsanız sıradaki yerinizi kaybedeceğinizi unutmayın! Yine de katkıda bulunmak için görevi daha sonra yeniden başlatabilirsiniz, ancak sıranın sonuna yerleştirileceksiniz.

Sıranın önüne ulaştığınızda, otomatik olarak katkınıza başlayacaktır. Katkıda bulunma işlemi birkaç dakika sürebilir. Yine bu noktada yapmanız gereken bir şey yok; sadece bekleyin. Katkınız bittiğinde, doğrulama için sunucumuza gönderilecektir. Aşağıdaki gibi ekranlar göreceksiniz;
  
   ![image](https://docs.manta.network/assets/images/ts_guide_awaiting_confirmation-e6e621889850a8ee8bc5fd3e896859b7.png)
  
Sunucu katkınızı doğruladıktan sonra bir onay mesajı alacaksınız:
  
    ![image](https://docs.manta.network/assets/images/ts_guide_success-1f47034af6b0b5e191cb9b2ec1c03a6e.png)
  
Katkı sağladığımız mesajı tweetleyerek (veya diğer genel forumlara göndererek) katkınızı tamamlayın. Bu adım kesinlikle gerekli olmasa da, katkınızın herkese açık bir kaydını oluşturarak törenin güvenliğini artırır.
  
