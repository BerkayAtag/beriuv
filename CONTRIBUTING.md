# Katkı rehberi

1. Değişikliğin amacını ve beklenen davranışı tanımlayın.
2. İlk commit sonrasında `master` üzerinden kısa ömürlü bir dal açın: `git switch -c feat/kisa-aciklama`.
3. İlgili kod, doküman ve davranış testini birlikte güncelleyin. Henüz test altyapısı yoksa bunu açıkça belirtin.
4. `git diff --check` çalıştırın; teknoloji seçildikten sonra tanımlanan lint, test ve derleme kontrollerini de çalıştırın.
5. Commit öncesi farkı inceleyin. Anahtar, parola, gerçek `.env`, kişisel veya kurumsal veri eklemeyin; `.gitignore` bir sır tarayıcısı değildir.
6. Commit mesajını değişikliğin amacını anlatacak şekilde yazın; örnek: `feat: add initial user flow`.
7. Pull request açıklamasına problemi, sonucu ve doğrulama yöntemini yazın. İlk commit sonrası değişiklikleri PR ile değerlendirmek önerilir.

Bağımlılık ve kilit dosyalarını birlikte güncelleyin. Teknoloji ve mimari kararlarını `docs/DECISIONS.md` içinde kaydedin.
