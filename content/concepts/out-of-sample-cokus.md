---
baslik: "Out-of-Sample Çöküş"
slug: "out-of-sample-cokus"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fpa-bulgu, negatif-bulgu, stabilite, backtest]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Out-of-Sample Çöküş: $C_t$ Zamanla Stabil Değil

## Özü
FPA'nın temel **negatif bulgusu**: portföy Hurst kuadratik form $H_p \approx c_t + w^T C_t w$ matrisi $C_t$ zamana göre kaymaktadır; in-sample fit out-of-sample'da çöker.

## Tanım
[[portfoy-hurst-kuadratik-form]] yaklaşımı in-sample (eğitim penceresi) içinde iyi $R^2$ verir; ancak $C_t$ matrisi rolling pencere kaydırıldığında dramatik biçimde değişir. Eigendecomposition ile bakıldığında özellikle eigenvektörlerin yön değiştirdiği görülür (bkz. [[subspace-stability]]). Sonuç: $t_1$'de elde edilen $w^*$ optimum, $t_2$'de artık optimum değildir ve hatta etkin sınıra yakın bile olmayabilir. Bu çöküş, klasik Markowitz'in kovaryans matrisi $\Sigma$'nın da benzer bir kaderi paylaştığı bilinen bulgusunun fraktal versiyonudur — ancak fraktal yapıda ($C_t$) çöküş daha hızlıdır çünkü Hurst ölçümü kovaryanstan daha az veri-verimlidir. Bu, projenin "ampirik objective function bulduk ama operasyonel olarak güvenilmez" sonucunu doğurur ve [[rolling-backtest]] bulgularıyla doğrulanır.

## Formül
Stabilite ölçüsü:
$$
\Delta_C(t_1, t_2) = \| C_{t_1} - C_{t_2} \|_F / \| C_{t_1} \|_F
$$
Optimumluk kaybı:
$$
\Delta H_p^* = H_p\big(w^*(t_1); t_2\big) - H_p\big(w^*(t_2); t_2\big)
$$
FPA bulgusu: $\Delta_C \gg 0$ ve $\Delta H_p^* > 0$ tutarlı biçimde.

## Ana Bağlamlar
- [[portfoy-hurst-kuadratik-form]] çöken yapı
- [[subspace-stability]] eigenvektör kayması
- [[rolling-backtest]] gözlem pipeline'ı
- [[estimator-gurultusu-bias-variance]] gürültü kaynağı

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — projenin kritik dürüst bulgusu; sonuç bölümünün ana mesajıdır
- [Tauron](../../projects/tauron/) — fraktal cezanın da benzer stabilite sorunlarına maruz kalabileceği dersi
- [Seminer](../../projects/) — "fraktal portföy de regularize edilmedikçe çöker" uyarısı

## Kaynak
[[aygoren-uyar-2023]]
