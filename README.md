

  
### Raspberry Pi kurulumu

Raspberry pi OS other kısmından Raspberry Pi OS Lite (64-bit) olan versiyonu Raspberry pi imaj yöneticisi ile kurun.
Raspberrydeki kullanıcı adı mutlaka pi olmalı değiştirilirse çalışmayacaktır.


![Alt text](/Images/Resim1.png?raw=true "Optional Title")
![Alt text](/Images/Resim2.png?raw=true "Optional Title")
![Alt text](/Images/Resim3.png?raw=true "Optional Title")
![Alt text](/Images/Resim4.png?raw=true "Optional Title")

pi kullanıcısının şifresini girin daha sonra lazım olacak not alın.
Bu ayarlar wifiye otomatik bağlanması için yapılmıştır. ssh ile bağlantı almak için yapılmaktadır. Monitörlü kurulumda wifiye monitör ile bağlanılabilir.  
### Gsm Modülün Kurulması
Gsm modülün ilk kurulumunda internete ihtiyaç vardır bu yüzden wifi ile veya ethernet kablosu ile internete bağlayın.
<br>Önemli not : Çıkartılan gsmsetup isimli klasör mutlaka /home/pi dizininde olmalı ve kurulumdan sonra silinmemeli !


gsmsetup.zip dosyasını raspberry pi'nin /home/pi dizinine aktarın 
```bash
wget https://github.com/bartinbu/gsmsetup/raw/main/gsmsetup.zip
```

/home/pi dizininde terminal açın
Zip dosyasını çıkartın
```bash
unzip gsmsetup.zip
```
/home/pi/gsmsetup dizinine gidin
```bash
cd gsmsetup
```
Tüm .sh uzantılı dosyalara +x yetkisi verin
```sh
sudo chmod +x *.sh
```
sudo haklarıyla install.sh dosyasını çalıştırın.
```sh
sudo ./install.sh
```
GSM shiled üzerindeki ışıklar yanmaya başlayacaktır. İnternet bağlantısı için hat takılı olmalıdır. Hat takılı değilken de kurulum yapılabilir.

GSM bağlantısını kontrol etmek için pingtest.sh scriptini çalıştırabilirsiniz.(zorunlu değil) Eğer ppp0 arayüzü gelmiyorsa hat çekmiyordur çeken bir yerlerde kendisi otoatik olarak gelecektir. 
<br> Eğer yine de gelmediyse yeniden başlatmayı deneyebilirsiniz.
```sh
./pingtest.sh
``` 
