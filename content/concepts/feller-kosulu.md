---
baslik: "Feller Koşulu"
slug: "feller-kosulu"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [olasilik, stokastik-volatilite, parametre]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Feller Koşulu

## Özü
Karekök-difüzyon süreçlerinin pozitif yarı eksende kalmasını ve sıfır sınırına ulaşmamasını garanti eden parametrik eşitsizliktir.

## Tanım
[[cir-modeli]] ve [[heston-stokastik-volatilite]]'nin varyans sürecinde, parametreler $2\kappa\theta \ge \sigma^2$ koşulunu sağlıyorsa süreç kesinlikle pozitif kalır; sınır olarak sıfır "ulaşılamaz" hale gelir. Koşul ihlal edilirse süreç sıfıra dokunabilir, bu da [[non-central-chi-squared]] geçiş yoğunluğunun serbestlik derecesinin 2'nin altına düşmesi anlamına gelir ve sayısal şemalarda (örn. naif [[euler-maruyama]]) negatif değerler üretir. Pratikte Heston kalibrasyonu Feller'ı sıkça ihlal eder; full-truncation veya tam-dağılım simülasyon teknikleri bu sorunu yönetir.

## Formül
$$
2\kappa\theta \ge \sigma^2
$$
$\kappa$ mean-reversion hızı, $\theta$ uzun-vade ortalaması, $\sigma$ difüzyon (Heston'da [[vol-of-vol]]).

## Ana Bağlamlar
- [[cir-modeli]] — koşulun ilk türetildiği süreç
- [[heston-stokastik-volatilite]] — varyans için pozitiflik gereği
- [[vol-of-vol]] — koşulun üst sınırı ile ilişkili parametre
- [[non-central-chi-squared]] — koşul ihlalinde değişen serbestlik derecesi

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — stokastik volatilite kalibrasyonu uyarısı
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — simülasyon doğruluğu için kontrol parametresi

## Kaynak
[[cir-1985]], [[andersen-piterbarg-2007]]
