---
baslik: "Altuzay Stabilitesi"
slug: "subspace-stability"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [eigendecomposition, stabilite, fpa-bulgu]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Altuzay Stabilitesi (Subspace Stability)

## Özü
$C_t$ matrisinin eigenvektörlerinin zamanla yön değiştirip değiştirmediğini ölçen analiz; out-of-sample çöküşün temel mekanizmasını ortaya koyar.

## Tanım
$C_t = U_t \Lambda_t U_t^T$ eigendecomposition'ında (bkz. [[eigendecomposition-dusuk-rutbeli]]), eigenvektörler $U_t$ zaman içinde sabit mi yoksa kayıyor mu? Stabilite ölçütü olarak ardışık zaman noktalarındaki eigenvektörler arasındaki **principal angle** (canonical angle) hesaplanır. Eğer ilk $k$ eigenvektörün gerdiği altuzay sabitse (örn. ilk 3 eigenvektör finansal sektörel yapıyı yansıtıyorsa), eigenvektör yönleri içinde dönmeler olsa bile "rejim" stabildir. FPA bulgusu: ilk birkaç altuzay (ilk 1-2 eigenvektör) görece stabil (piyasa modu), ancak daha küçük eigenvalues'a karşılık gelen altuzaylar zamanla rastgele dönmeler yapar — bu da [[out-of-sample-cokus]] mekanizmasının teknik açıklaması olur. Optimum portföy ağırlıklarının küçük eigenvalues yönlerinde fazla yük taşıması, çözümün kararsız olduğunun erken sinyalidir.

## Formül
Principal angle (iki altuzay arası):
$$
\theta_k(U_{t_1}, U_{t_2}) = \arccos\big(\sigma_k(U_{t_1}^T U_{t_2})\big)
$$
Burada $\sigma_k$ tekil değerler. Stabilite endeksi:
$$
\text{Stab}(t_1, t_2; k) = \prod_{i=1}^{k} \cos \theta_i
$$
$\text{Stab} \to 1$ stabil, $\to 0$ tam dönme.

## Ana Bağlamlar
- [[eigendecomposition-dusuk-rutbeli]] altyapı
- [[out-of-sample-cokus]] doğrudan açıklama
- [[portfoy-hurst-kuadratik-form]] çalışılan yapı
- [[rolling-backtest]] zaman serisi gözlemi

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — çöküşün mekanizmasını gösteren kilit teknik analiz
- [Tauron](../../projects/tauron/) — fraktal-tabanlı kovaryanslarda da benzer stabilite analizinin gerekliliği
- [Seminer](../../projects/) — eigenstructure görselleri sunum malzemesi

## Kaynak
[[aygoren-uyar-2023]]
