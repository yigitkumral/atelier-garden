---
baslik: "Etkin Sınır"
slug: "etkin-sinir"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, optimizasyon, portfoy, geometri]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Etkin Sınır

## Özü
Verilen bir varyans seviyesi için maksimum beklenen getiriyi (ya da verilen getiri için minimum varyansı) sağlayan portföylerin $\mu$-$\sigma$ düzlemindeki geometrik yer eğrisidir.

## Tanım
Etkin sınır (efficient frontier), Markowitz probleminin tüm hedef getiri değerleri $\mu^*$ üzerinde taranmasıyla elde edilen çözüm kümesinin üst koludur. $\sigma^2$-$\mu$ düzleminde bir parabol, $\sigma$-$\mu$ düzleminde ise bir hiperboldür. Hiperbolün en sol noktası [[minimum-varyans-portfoyu]] olup bu noktanın altındaki kol "yetersiz" portföyleri içerir ve dışlanır. Risk-free varlık eklendiğinde sınır, yerini düz bir doğru olan [[sermaye-tahsis-dogrusu-cal]]'a bırakır; bu doğru hiperbole [[tangent-portfoy]] noktasında teğet geçer.

## Formül
Kapalı formda etkin sınır, [[abcd-parametreleri]] cinsinden:
$$
\sigma_p^2 = \frac{1}{D}\left(C \mu_p^2 - 2B \mu_p + A\right)
$$
burada $D = AC - B^2$. Bu, $\sigma^2$-$\mu$ düzleminde bir paraboldür.

## Ana Bağlamlar
- [[markowitz-portfoy-teorisi]] etkin sınırı üreten optimizasyon problemidir
- [[minimum-varyans-portfoyu]] hiperbolün ucunu işaretler
- [[tangent-portfoy]] CAL ile temas noktasıdır
- [[abcd-parametreleri]] geometriyi parametreleştirir

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — 11 portföyün konumlandığı eğri
- [Tauron](../../projects/tauron/) — multifraktal düzeltme sonrası "fraktal etkin sınırın" karşılaştırma referansı
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — Hurst-getiri düzlemindeki muadili olan frontier-elipsi-hurst-getiri için klasik analog

## Kaynak
[[markowitz-1952]]
