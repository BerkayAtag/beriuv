# Beriuv

Beriuv için teknoloji bağımsız proje başlangıcı. Bu paket klasör düzeni ve geliştirme yönergeleri sağlar; henüz çalışan bir uygulama içermez.

## Durum ve varsayımlar

- 13 Ekim 2026 kontrolünde `BerkayAtag/beriuv` deposunun boyutu 0, varsayılan dalı `master`; içerik uç noktası `This repository is empty` yanıtı verdi.
- Projenin amacı, uygulama türü, dili, framework'ü ve dağıtım ortamı henüz belirlenmedi.
- Tek depo içinde basit bir yapı başlangıç için yeterli kabul edildi. İhtiyaç oluşursa çoklu uygulama düzenine dönüştürülebilir.
- `master` adı korunur. Yeniden adlandırma ayrı bir karardır.
- Henüz bağımlılık, paket yöneticisi, çalışma zamanı veya CI seçilmedi.
- Lisans kararı verilmedi; bu başlangıç herhangi bir kullanım lisansı tanımlamaz.

## Klasör yapısı

| Yol | Amaç |
| --- | --- |
| `src/` | Uygulama veya kütüphane kaynak kodu |
| `tests/` | Seçilecek test aracının testleri |
| `docs/` | Geliştirme rehberi ve teknik kararlar |
| `scripts/` | Tekrarlanabilir geliştirme ve bakım komutları |
| `.gitignore` | Yerel dosya, sır ve yaygın çıktı istisnaları |
| `.editorconfig` | Tutarlı metin biçimi |
| `.gitattributes` | Metin dosyalarında LF satır sonları |
| `CONTRIBUTING.md` | Katkı ve değişiklik kontrolü |

Boş klasörler `.gitkeep` ile izlenir; gerçek dosyalar eklendiğinde yer tutucuları kaldırabilirsiniz.

## Başlangıç

Git dışında kurulum önkoşulu yoktur. Henüz çalıştırma, derleme veya test komutu yoktur; bunlar teknoloji seçildikten sonra eklenecektir.

Boş depoyu klonlayın:

```sh
git clone https://github.com/BerkayAtag/beriuv.git
cd beriuv
```

Paketin `beriuv/` klasörünün **içeriğini**, gizli ayar dosyaları dahil, klonlanan klasöre kopyalayın. İç içe `beriuv/beriuv/` oluşturmayın.

```sh
git status --short
git add README.md CONTRIBUTING.md .gitignore .editorconfig .gitattributes src tests docs scripts
git diff --cached --check
git diff --cached --stat
git diff --cached
git commit -m "chore: initialize Beriuv project structure"
```

Git kullanıcı kimliği eksikse kendi adınız ve e-posta adresinizle yapılandırın. Uzak depo hâlâ boşsa ilk commit yayımlamak için:

```sh
git push -u origin master
```

Depoya bu arada içerik eklenmişse kopyalamadan önce mevcut dosyaları inceleyin; bu paketle üstüne yazmayın.

## Sonraki teknik adımlar

1. Projenin çözeceği problemi, hedef kullanıcıyı ve ilk teslimatın kabul ölçütünü `docs/DECISIONS.md` içinde tanımlayın.
2. Uygulama türünü, dili, desteklenen çalışma zamanı sürümünü ve paket yöneticisini seçin; karar ve gerekçesini kaydedin.
3. Seçilen teknolojiye ait manifesti ve gerekiyorsa bağımlılık kilit dosyasını ekleyin. `.gitignore` kurallarını uyarlayın.
4. Tek bir temel akışı `src/` içinde uygulayın; kurulumu ve çalıştırma komutlarını README'ye ekleyin.
5. Bu akışın kabul ölçütünü doğrulayan ilk testi `tests/` içine ekleyin; biçimlendirme ve lint komutlarını belirleyin.
6. Kurulum, lint, test ve varsa derlemeyi çalıştıran CI ekleyin. Başarılı kontrolleri dal korumasına bağlayın.
7. Dağıtım, yapılandırma ve lisans kararlarını ihtiyaçlara göre tamamlayın.

Ayrıntılar: [Geliştirme rehberi](docs/DEVELOPMENT.md), [Kararlar](docs/DECISIONS.md), [Katkı rehberi](CONTRIBUTING.md).
