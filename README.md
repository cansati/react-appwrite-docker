# React Appwrite Docker
Terminal açın ve dosya yolunu indirdiğiniz klasöre getirin.
```bash
cd react-appwrite-docker-main
```

## Kurulum

Konteyner'lar çalıştırmadan önce, konteynerların bağımlı olduğu imajlar build ederek hazır hale getirelim.

```bash
docker-compose build
```

Hata yoksa, konteynerları çalıştıralım.

```bash
docker-compose up -d
```

###### -d: Terminali yapılan işlem loglarına kitlemez, başka komutlar girmemize imkan tanır.

appwrite-semsis konteyner'ının terminaline bağlanıp appwrite uygulamasının bizden istediği parametreleri gireceğiz.


```bash
docker attach appwrite-semsis
```

Http istekleri için uygulamanın hangi porta bağlanacağını seçmemiz gerektiği ve varsayılanın 80 olduğu bize terminalde gösterildi fakat konteyner ayağa kalktıktan sonra bağlandığımız için göremedik, bu yüzden aşağıdaki gibi giriş yapmamızı bekleyen bir terminale bağlandık

```bash
|
```
İsterseniz enter'a basıp varsayılan port üzerinden, isterseniz de değiştirerek devam edebilirsiniz.

Sonraki istenen parametre https istekleri için uygulama kendisini hangi porta bağlasın:(varsayılan 443)

Sonraki istenen parametre host ip'si:(varsayılan 'localhost'). Localde çalışacaksanız boş bırakıp Enter.

Sonraki istenen parametre domain ismi: (varsayılan 'localhost'). Localdeyseniz boş bırakıp enter.

Kurulum tamamlandı. Varsayılan ayarlarla tamamladıysanız:

Appwrite: localhost:80 

React: localhost:3000

Sonraki çalıştırmalar için kullanabilirsiniz:

docker-compose up -d && docker attach appwrite-semsis
