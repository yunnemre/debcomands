// kulanılanlar tekrarlıyor olabilir temize cekilmedi kullandıkca untumiyim diye notlar alıyoru tekrar tekrar

############################################################################################
cat /etc/passwd // ya da
 getent passwd // Kullancıları listeler
adduser <username> sudo //sudo grubuna ekler sonra /etc/sudoers dosyasına da eklemen lazım
yunn    ALL=(ALL:ALL) ALL //

sudo ufw status // guvenlik duvarı durumu gosteirr
sudo ufw allow <port_number>
ss or netstat
dpkg -l | grep // grep sonra yazdıgın paket ismi ayrıntıalrını getioyr
sudo service ssh status//ssh status 
sudo service ssh restart //yeniden baslattmqa
hostnamectl -l // cihaz ıp adresi
 netstat -tuln //-t	Sadece TCP bağlantılarını göster
 ss -tuln //     -u	Sadece UDP bağlantılarını göster
                 -l	Sadece dinleyen (LISTEN) portları göster
                 -n	IP ve portları isim yerine numara olarak göster (hızlı ve net görüntü verir)
hostnamectl // bilgisayar bilgilerini gosterir yanınba isim yzarsak makine adı degisiyor
 vim /etc/hosts // makine adını degistirdikten sorna dosyadan da degistiiroyurz
 sudo vim /etc/sudoers // sudo yapılandırma dosyaysı

 i sudo vim /etc/login.defs // parola ayarları icin bu klasorde kodları yazıyoruz
 sudo chage –l <user> ile dosya sifre politikaları goryoruz
 sudo apt install libpam-pwquality -y // parola gucuyle ilgili kuram yazmak icin bu paketi indiriyoruz
 sudo vim /etc/pam.d/common-password // sifrenin ozelliklerini değistirmek icin conf dosyası
 // password requisite pam_pwquality.so retry=3 dcredit=-1 difok=7 enforce_for_root lcredit=-1
maxrepeat=3 ucredit=-1 usercheck=1 minlen=10 gibi
sudo adduser <username> //user ekleme
id <kullanıcı adı> // yuzur detayların ıgetirme yada
// sudo getent passwd kullanici42
groups <kullanıcı adı> // kulnaıcın hangi grouplarda oldugnu yazaıyor