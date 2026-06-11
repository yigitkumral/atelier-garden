---
baslik: "Kovaryans Matrisi"
slug: "kovaryans-matrisi"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, istatistik, lineer-cebir, portfoy]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Kovaryans Matrisi

## Özü
Varlık getirileri arasındaki ortak değişkenliği tutan, simetrik ve pozitif yarı-tanımlı $N \times N$ matristir; portföy varyansının tek girdisi $\Sigma$'dır.

## Tanım
$N$ varlıktan oluşan bir evrende getiri vektörü $r$ rastgele bir değişken olduğunda, kovaryans matrisi $\Sigma_{ij} = \mathrm{Cov}(r_i, r_j)$ ile tanımlanır. Köşegen elemanlar tekil varyanslardır; köşegen-dışı elemanlar varlık çiftleri arasındaki ortak değişkenliği yansıtır. Çeşitlendirme, çoğu çiftin pozitif fakat 1'den küçük korelasyona sahip olması sayesinde tekil varyansların doğrudan toplamından küçük portföy varyansına yol açar. $\Sigma$ pratikte tahmincidir ve örneklem boyutu $T$ ile varlık sayısı $N$ aynı mertebede olduğunda yüksek koşullanma sayılı olur, bu da [[abcd-parametreleri]] üzerinden estimator-gurultusu-bias-variance ve out-of-sample-cokus problemlerini doğurur.

## Formül
Örneklem kovaryansı:
$$
\hat{\Sigma} = \frac{1}{T-1} \sum_{t=1}^{T} (r_t - \bar{r})(r_t - \bar{r})^T
$$
Portföy varyansı:
$$
\sigma_p^2 = w^T \Sigma w = \sum_{i,j} w_i w_j \Sigma_{ij}
$$

## Ana Bağlamlar
- [[markowitz-portfoy-teorisi]] kuadratik formun çekirdeği
- [[abcd-parametreleri]] $\Sigma^{-1}$ üzerinden tanımlı
- [[minimum-varyans-portfoyu]] yalnızca $\Sigma$'ya bağlıdır
- [[tangent-portfoy]] hem $\mu$ hem $\Sigma$'yı kullanır

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — 11 portföy hesabının ana girdisi
- [Tauron](../../projects/tauron/) — multifraktal düzeltme sonrası $\Sigma$'nın zaman-bağımlı yeniden tahmini
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — $C_t$ Hurst-uzay kovaryans analogu

## Kaynak
[[markowitz-1952]]
