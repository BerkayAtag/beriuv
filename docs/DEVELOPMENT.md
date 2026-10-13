# Geliştirme rehberi

## Mevcut durum

Bu başlangıçta uygulama kodu, bağımlılık, test koşucusu, derleme veya CI bulunmaz. Başarılı uygulama testi yapıldığı iddia edilmez.

## Dosya yerleşimi

- `src/`: Kaynak kodu; framework farklı bir düzen gerektirirse uyarlayın.
- `tests/`: Kabul ölçütünü doğrulayan testler; aracın yerleşik düzeni tercih edilebilir.
- `scripts/`: Tekrarlanabilir komutlar. Her komutun gereksinimini, girdisini, çıktısını ve yan etkisini belgeleyin.
- `docs/`: Kurulum dışındaki teknik açıklamalar ve karar kayıtları.

## Teknoloji seçildikten sonra

README'ye kesin çalışma zamanı sürümünü, kurulum, geliştirme, lint, test ve derleme komutlarını ekleyin. Gerekmeyen aşamalar için nedenini belirtin. Sürüm ve komutlar seçilmeden tahmini komut kullanmayın.

Ortam değişkeni gerekmiyorsa `.env.example` oluşturmayın. Gerekiyorsa yalnızca sahte değerleri ve değişken açıklamalarını içeren örnek ekleyin. Gerçek değerleri yerelde veya dağıtım ortamının sır yönetiminde tutun. Ön yüz paketine yerleştirilen değerlerin kullanıcıya görünür olabileceğini dikkate alın.

`.gitignore` genel başlangıçtır: kaynak olarak kullanılan `build/` gibi yollar varsa ilgili kuralı kaldırın; yeni teknolojiye ait çıktı ve önbellek kurallarını ekleyin. Ekipçe paylaşılacak editör ayarları gerekiyorsa `.vscode/` kuralını daraltın. Kilit dosyalarını uygun paket yöneticisi politikasına göre izleyin.

## Değişiklik kontrolü

```sh
git status --short
git diff --check
git diff --cached --check
git diff --cached
```

Kontroller sadece Git/metin tutarlılığı sağlar. Test altyapısı eklendikten sonra davranış testleri ve ilgili lint/derleme kontrolleri ayrıca çalıştırılmalıdır.

## İlk çalışan teslimat

Tek bir temel kullanım akışı, belgelenmiş kurulum/çalıştırma komutları ve bu akışın kabul ölçütünü doğrulayan bir test hazırlayın. Ardından aynı doğrulamayı CI'ye taşıyın. Dağıtım ortamı ve lisans ayrı kararlar olarak kaydedilsin.
