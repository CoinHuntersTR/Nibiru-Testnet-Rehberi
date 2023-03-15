# Cosmos Projelerinde Validator NODE Yedek Alma. #1

![nibiru-roadmap](https://staticfiles.acronis.com/images/blog-cover/696aba821d856b6e452815b12e98d97b.png)


### MobaxTerm İle Yedek Alma
- İlk önce yedeği alacağınız projeyi açıyoruz. 
- Soldaki menüden dosyalarına ulaşıyoruz. 
- Sonrasında .projeadi şeklinde klasöre giriyoruz. 
- Config klasörüne giriş yapıyoruz.
- Config içerisinde "priv_validator_key.json" olan dosya seçiyoruz.
- Sonra üstte "Download Select files" simgesine basıyoruz. Aşağı doğru mavi ok.
- İndireceğimiz yere seçip dosyayı indirip saklıyoruz.
- Aşağıdaki animasyonlu görselde adımları tek tek gösterdik. COSMOS projelerinde node taşımak için bu "priv_validator_key.json" dosyasını kesinlikle almanız gerekiyor.

![ezgif com-video-to-gif (2)](https://user-images.githubusercontent.com/111747226/225409643-07837d36-2cb8-4a8e-901a-ab73e9de4fd7.gif)

### Google Cloud ile yedek alma.
- Öncelikle cloud google açıyoruz oradan SSH açıyoruz.
- Sonrasdında aşağıdaki kodu yazıyoruz.

```
sudo su
```

- Yedeğini almamız gerek projenin dosya yolunu yazmamız gerekiyor.
- "projeadi-sonuna-d ekliyoruz" kısmını projeye göre değiştirebilirsiniz. Nibiru nibi, andromeda andromedad babylon babylond gibi
- Kurulumu yaptıktan sonra genel dosya dizini /root/."projeadi-sonuna-d ekliyoruz"/config/priv_validator_key.json
```
nano /root/."projeadi-sonuna-d ekliyoruz"/config/priv_validator_key.json
```
- Karşımıza gelen kodları kopyalıyoruz. 
- Sonra bir .txt dosyası açıyoruz. 
- Dosya adını priv_validator_key.json ile .txt uzantısını .json olarak değiştiriyoruz.
- Terminal içerisindeki kodları bunun içerisine kayıt ediyoruz. 
- Yedek alma işlemi tamamdır. 
-  Node yeni projeye taşırken bu aldığımız dosya işimize yarayacak mutlaka saklayın.
![google](https://user-images.githubusercontent.com/111747226/225417218-532d5b07-09c5-46c0-a315-c6d187eb3d99.gif)
