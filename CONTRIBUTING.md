# VUAV Tech: katkı kuralları

Bu kurallar organizasyondaki bütün repolar için geçerlidir. Görevler, deadline’lar ve review süreci [Takım Portalı](https://app.vuav.net)’nda yürür; GitHub kodun ve dosyaların yaşadığı yerdir.

## 1. Dallar

- `main` her zaman çalışır durumdadır. Doğrudan `main`’e push yapılmaz.
- Her iş kendi dalında yapılır. Dal adı portal görev anahtarıyla başlar:
  `ELK-12-batarya-failsafe`, `YAZ-7-yolo-yeniden-egitim`.
- İş bitince **pull request** açılır ve en az bir kişi review eder.

## 2. Commit mesajları

- Kısa, emir kipinde, ne yaptığını söyleyen bir başlık: `Batarya failsafe eşiklerini ekle`.
- Gerekirse bir boş satırdan sonra neden yaptığını açıkla.
- Portal görevinin anahtarını yaz: `ELK-12`.

## 3. Pull request

- Şablonu doldur: ne değişti, nasıl test edildi, kanıt.
- Reviewer, portaldaki görevin reviewer’ıdır. PR onaylanınca portaldaki görevi de “Review’a gönder”le kapatırsın; kanıt olarak PR linkini eklersin.
- Büyük değişiklikleri parçala; bir PR tek bir işi yapsın.

## 4. Uçuş-kritik değişiklikler (A sınıfı)

Uçuş parametreleri, motor/güç sistemi, failsafe ve otopilot kodu A sınıfıdır:

1. SITL’de test edilir; log PR’a eklenir.
2. Test kartı doldurulur.
3. Uçuş Test Direktörü onayı olmadan `main`’e girmez.
4. Yarışmadan 2 hafta önce **config freeze**: bu tarihten sonra yalnızca güvenlik düzeltmeleri.

## 5. Gizli bilgiler

- Şifre, API anahtarı, token, servis hesabı dosyası **asla** repoya, issue’ya ya da PR’a yazılmaz. Bitwarden’da durur.
- Yanlışlıkla commit’lediysen silmek yetmez: hemen kaptanına haber ver; anahtar iptal edilip yenilenir.

## 6. Büyük dosyalar

- 50 MB üstü dosyalar (log, veri seti, video) repoya girmez. Drive’a koy, linkini README’ye ya da PR’a yaz.
- CAD dosyaları Onshape’te, PCB dosyaları KiCad projesi olarak `avionics-pcb` reposunda durur.
