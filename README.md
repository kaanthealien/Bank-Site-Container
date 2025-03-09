# Banka Uygulaması (Flask + Nginx + Docker)

Bu proje, bir banka uygulamasının temel özelliklerini barındıran bir web sitesinin Docker ve Nginx ile yapılandırılmasını içermektedir. Flask, backend için kullanılırken, Nginx proxy sunucusu olarak görev yapmaktadır. Proje, Docker Compose ile birden fazla hizmetin (Flask uygulaması ve Nginx) aynı anda çalışmasını sağlar.

## Proje Özellikleri
- **Flask**: Python ile yazılmış minimal bir web framework olan Flask, bankacılık uygulamasının backend'ini sağlar. (Bunu önceden yaptığım basit projemden aldım -->https://github.com/kaanthealien/Flask-Basit-Banka)
- **Nginx**: Flask uygulaması ile istemciler arasındaki istekleri yönlendiren ve proxy işlemlerini gerçekleştiren bir web sunucusu olarak kullanılır.
- **Docker**: Tüm uygulama, Docker konteynerleri içinde çalışacak şekilde yapılandırılmıştır. Bu sayede uygulama her ortamda hızlıca çalıştırılabilir.
- **Docker Compose**: Birden fazla servisi (Flask ve Nginx) tek bir komutla başlatmak için Docker Compose kullanılır.

## Kurulum

### Gereksinimler
- Docker
- Docker Compose

### Kurulum Adımları
1. Reposunu bilgisayarınıza klonlayın:
   ```bash
   git clone https://github.com/kaanthealien/Bank-site-container.git
   cd Bank-site-container
2.Docker ve Docker Compose'un bilgisayarınızda kurulu olduğundan emin olun.

3.Uygulamanın başlatılması için aşağıdaki komutu çalıştırın:
   ```bash
   docker-compose up --build
   ```
4.Uygulama başarıyla başlatıldığında, tarayıcınızda http://localhost adresine giderek uygulamayı görüntüleyebilirsiniz. (Benim 8081 portum müsait olduğu için 8081 portunu kullandım fakat siz bunu kendinize göre konfigüre edebilirsiniz.)

### Projenin Yapısı
- docker-compose.yml: Docker Compose yapılandırma dosyası, tüm servislerin nasıl başlatılacağını belirtir.
- Dockerfile: Flask uygulamasını bir Docker konteynerine yerleştirir.
- nginx.conf: Nginx yapılandırma dosyası, isteklerin Flask uygulamasına yönlendirilmesini sağlar.
- app/: Flask uygulamasının bulunduğu dizin.
- requirements.txt: Flask uygulaması için gerekli Python bağımlılıkları.

  
