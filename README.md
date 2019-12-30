
## Dockerizing Laravel Application With Nginx,Mysql on Ubuntu

![Docker_Compose](images/laravel-docker.png)

Bir laravel projesini sanallaştırma teknolojilerini kullanarak nasıl ayağa kaldırırız?

Bu projede bir tane docker composer oluşturup bir container'da web sunucusu olarak ngnix, bir başka container'da db olarak mysql, bir başka container'da da uygulamamız'ın koşmasını hedefliyoruz.Sonuç olarak projemizde docker composer kullanarak toplam 3 tane ayrı container kullanmış olacağız ve bunlar bir birleri ile etkilşim halinde olmuş olacaklar.

## 1-Laravel Kütüphanesini Projeye İmport Edelim


![Docker_Compose](images/laravel-logo.jpg)

Aşağıdaki komut satırı ile laravel kütüphanesini Projemize clone edelim.

    - $ git clone https://github.com/laravel/laravel.git Dockerizing-laravel-App

## 2-Docker Composer'ı Projemize Kuralım

Composer'ı kullanabilmek için projemizin ana dizininde kurulumu yapalım.
    
    - $ cd ~/laravel-app
    
    - $ docker run --rm -v $(pwd):/app composer install
    
## 3-Docker Compose File Oluşturalım.

Projemizde kullacağımız image 'leri tanımlamak için Docker-Compose dosyası oluşturalım.

    - $ nano ~/laravel-app/docker-compose.yml

## 4-Docker Compose Dosyasını Projemizin Niteliklerine Göre Düzenleyelim.

Projemizde kullanmamız gereken 3 tane container var.Bu container'ları oluşturucağımız docker-compose.yml dosyasında tanımlayıp sonra build edeceğiz.

## 5- Docker File dosyasını OLuşturalım.

![Docker](images/docker-file.jpeg)
 
