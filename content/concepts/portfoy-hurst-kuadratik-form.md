---
baslik: "Portföy Hurst Kuadratik Form"
slug: "portfoy-hurst-kuadratik-form"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, hurst, portfoy, kuadratik, fpa-bulgu]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Portföy Hurst Kuadratik Form: H_p(w; t) ≈ c_t + wᵀC_t w

## Özü
Fractal Portfolio Analysis projesinin merkez bulgusu: portföy seviyesindeki Hurst üsteli, varlık ağırlıklarının kuadratik formu olarak yaklaşık ifade edilebilir.

## Tanım
Aygören-Uyar (2023) makalesinin "objective function bulamadık" problemine cevap olarak FPA'da ampirik şu bulgu: portföy ağırlık vektörü $w$ ile portföy Hurst $H_p$ arasındaki ilişki, yeterince geniş bir varlık evreninde ve sabit bir zaman penceresinde, $H_p(w; t) \approx c_t + w^T C_t w$ kuadratik formuyla iyi yaklaşılır. Buradaki $C_t$ matrisi klasik kovaryans matrisi $\Sigma$'dan farklıdır; ölçek-bağımlı bir Hurst-eşleme matrisidir ve [[eigendecomposition-dusuk-rutbeli]] yapısıyla birkaç eigenvektörle ifade edilebilir. Ancak [[out-of-sample-cokus]] bulgusu, $C_t$'nin zamanla stabil olmadığını ve in-sample fit'in out-of-sample'da bozulduğunu gösterir. Bu, biçimsel olarak [[markowitz-paralelligi]] taşır ama operasyonel olarak doğrudan bir Markowitz-tipi optimizasyon yapmaya yetecek stabiliteye sahip değildir — projenin temel negatif bulgusudur.

## Formül
Yaklaşım:
$$
H_p(w; t) \approx c_t + w^T C_t \, w
$$
Kısıt:
$$
w^T \mathbf{1} = 1, \quad w_i \ge 0 \text{ (long-only)}
$$
$C_t$ pozitif yarı-tanımlı değildir (genelde işaret-belirsiz); $c_t$ konstant kayma terimi, ortalama Hurst seviyesini belirler.

## Ana Bağlamlar
- [[hurst-exponent]] portföy düzeyinde uzantı
- [[markowitz-paralelligi]] biçimsel benzerlik
- [[eigendecomposition-dusuk-rutbeli]] $C_t$'nin yapısı
- [[out-of-sample-cokus]] kritik kısıt
- [[subspace-stability]] eigenvektör kaymaları

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — projenin merkezi bulgusu; faz1 ve faz2 raporlarının temelidir
- [Tauron](../../projects/tauron/) — fraktal düzeltme cezasının alternatifi olarak değerlendirilir; kavramsal akrabalık güçlü
- [Seminer](../../projects/) — "ampirik gözlem ile teorik yapı" örneği olarak sunulabilir

## Kaynak
[[aygoren-uyar-2023]] (öncül problem)
