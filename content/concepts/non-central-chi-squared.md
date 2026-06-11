---
baslik: "Merkez-Dışı Khi-Kare Dağılımı"
slug: "non-central-chi-squared"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [olasilik, dagilim, faiz-orani]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Merkez-Dışı Khi-Kare Dağılımı

## Özü
Bağımsız Gaussian değişkenlerin kareleri toplamının, ortalamaları sıfırdan farklı olduğunda izlediği iki-parametreli dağılımdır.

## Tanım
$\chi^2(k, \lambda)$ dağılımı, $k$ serbestlik derecesi ve $\lambda$ merkez-dışılık parametresine sahiptir; $\lambda = 0$ klasik khi-kareye indirgenir. Finansal matematikte bu dağılım, [[cir-modeli]]'nin geçiş yoğunluğu olarak ortaya çıkar: kareli-difüzyon yapısı, ölçeklenmiş bir merkez-dışı khi-kare üzerinden tam-dağılım simülasyonuna olanak verir (Broadie-Kaya algoritması). Bu sayede [[heston-stokastik-volatilite]] varyans sürecinin kesin örneklemesi yapılabilir; sayısal diskretizasyon hatasından (örn. [[euler-maruyama]]) bağımsız simülasyon mümkün olur.

## Formül
CIR sürecinin geçiş dağılımı:
$$
r_t \mid r_s \sim \frac{1}{2c} \chi^2\!\left(\frac{4\kappa\theta}{\sigma^2},\, 2c r_s e^{-\kappa(t-s)}\right)
$$
$c = \frac{2\kappa}{\sigma^2(1 - e^{-\kappa(t-s)})}$, $k = 4\kappa\theta/\sigma^2$ serbestlik derecesi.

## Ana Bağlamlar
- [[cir-modeli]] — dağılımın doğal olarak ortaya çıktığı süreç
- [[heston-stokastik-volatilite]] — varyans sürecinin kesin simülasyonu
- [[feller-kosulu]] — serbestlik derecesinin >2 olmasını garantiler

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — Heston/CIR simülasyon teorisi
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kesin örnekleme baseline'ı

## Kaynak
[[broadie-kaya-2006]], [[cir-1985]]
