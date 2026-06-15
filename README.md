# ISG Sertifika

ISG Sertifika, iş sağlığı ve güvenliği eğitim süreçlerinde sertifika ve katılım formu hazırlamayı hızlandıran Windows masaüstü uygulamasıdır.

Bu repository yalnızca public indirme ve güncelleme dosyaları içindir. Uygulama kaynak kodu private repository'de tutulur.

## İndir

Son kararlı sürüm:

[ISG-Sertifika-Setup-1.0.0.exe](https://github.com/KemaList93/isg-sertifika-releases/releases/download/v1.0.0/ISG-Sertifika-Setup-1.0.0.exe)

Release sayfası:

https://github.com/KemaList93/isg-sertifika-releases/releases/latest

## Ne İşe Yarar?

ISG Sertifika şu operasyonları tek uygulamada toplar:

- Firma ve eğitim oturumu yönetimi
- Çalışan kayıtlarının eklenmesi ve düzenlenmesi
- Meslek ve eğitim konusu seçimi
- Eğitim sürelerinin takip edilmesi
- Sertifika PDF üretimi
- Katılım formu PDF üretimi
- Geçmiş kayıtların yeniden görüntülenmesi ve yeniden PDF'e çevrilmesi
- Uygulama içinden GitHub Releases üzerinden güncelleme kontrolü

## Temel Özellikler

- Modern Windows masaüstü arayüzü
- Offline lisans sistemi
- SQLite tabanlı yerel veri saklama
- Firma logosu ve eğitici imzası kullanabilme
- Toplu sertifika üretimi
- Katılım formu oluşturma
- Public GitHub Releases üzerinden tokensız güncelleme
- SHA256 doğrulamalı installer indirme

## Kurulum

1. Son sürüm installer dosyasını indirin:
   [ISG-Sertifika-Setup-1.0.0.exe](https://github.com/KemaList93/isg-sertifika-releases/releases/download/v1.0.0/ISG-Sertifika-Setup-1.0.0.exe)
2. Dosyayı çalıştırın.
3. Kurulum sihirbazındaki adımları tamamlayın.
4. Uygulamayı başlatın.
5. Lisans dosyanız istenirse lisans dosyasını seçip doğrulayın.

## İlk Kullanım Akışı

1. Uygulamayı açın.
2. Firma veya eğitim bilgilerini girin.
3. Eğitici, uzman veya hekim bilgilerini tanımlayın.
4. Çalışan listesini ekleyin.
5. Eğitim tarihi, süre ve tehlike sınıfı gibi bilgileri doldurun.
6. Eğitim konularını kontrol edin.
7. Sertifika veya katılım formu önizlemesi alın.
8. PDF çıktısını oluşturun.

## Güncelleme

Uygulama içinden güncelleme kontrolü:

1. `Ayarlar` sayfasını açın.
2. `Güncellemeleri Kontrol Et` düğmesine basın.
3. Yeni sürüm varsa sürüm bilgileri ve release notları gösterilir.
4. `Güncelle` seçilirse installer indirilir.
5. SHA256 doğrulaması başarılı olursa kurulum için onay istenir.
6. Onaydan sonra installer başlatılır ve uygulama kapanır.

Güncelleme sistemi GitHub token kullanmaz. Sadece public GitHub Releases endpoint'ini okur:

```text
https://api.github.com/repos/KemaList93/isg-sertifika-releases/releases/latest
```

## SHA256 Doğrulama

Installer SHA256 değeri:

```text
5507355353F3534A2BFA173FA29F4BEC6C02745934E62730C5CC7D5019E3DC30
```

PowerShell ile manuel kontrol:

```powershell
Get-FileHash .\ISG-Sertifika-Setup-1.0.0.exe -Algorithm SHA256
```

Komut çıktısındaki hash değeri yukarıdaki değerle aynı olmalıdır.

## Dosyalar

Release assetleri:

- `ISG-Sertifika-Setup-1.0.0.exe` - Windows kurulum dosyası
- `ISG-Sertifika-Setup-1.0.0.exe.sha256` - SHA256 doğrulama dosyası
- `RELEASE_REHBERI.md` - Kurulum ve güncelleme rehberi
- `KULLANIM_REHBERI.md` - Uygulama kullanım rehberi

## Sorun Giderme

- Uygulama açılmıyorsa lisans dosyanızın geçerli olduğundan emin olun.
- Güncelleme bulunamıyorsa internet bağlantısını kontrol edin.
- Hash doğrulaması başarısızsa installer dosyasını tekrar indirin.
- Windows SmartScreen uyarısı çıkarsa dosyayı bu release sayfasından indirdiğinizi ve SHA256 değerinin doğru olduğunu kontrol edin.

## Güvenlik Notu

Bu public repository uygulamanın kaynak kodunu içermez. Yalnızca installer, doğrulama dosyaları ve kullanıcı rehberleri yayınlanır.

## Teknik Destek

Tüm teknik sorunlar ve destek talepleri için:

kemalsogut@koruyucu.com.tr


