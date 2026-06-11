---
baslik: "Markowitz Paralelliği"
slug: "markowitz-paralelligi"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [markowitz, kuadratik, fraktal, paralel-yapi]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Markowitz Paralelliği — Biçim Aynı, C Teorik Değil

## Özü
Fraktal portföy analizinin klasik Markowitz teorisiyle **biçimsel** olarak aynı kuadratik formu paylaştığı, fakat alttaki matrisin ($\Sigma$ yerine $C_t$) teorik değil ampirik bir nesne olduğu önemli kavramsal gözlem.

## Tanım
[[markowitz-portfoy-teorisi]]'nde portföy varyansı $\sigma_p^2 = w^T \Sigma w$ kuadratik formdadır; $\Sigma$ ise dağılımsal varsayımlar (genelde Gauss) altında ikinci moment tanımıyla teorik bir nesnedir. FPA'nın temel gözlemi: portföy Hurst de yaklaşık $H_p \approx c_t + w^T C_t w$ ile aynı **kuadratik form** biçimine sahiptir (bkz. [[portfoy-hurst-kuadratik-form]]). Yani biçimsel iskelet aynı: ağırlık vektörünün simetrik bir matrisle skaler çarpımı. Ancak büyük fark: $\Sigma$ kapalı-form teorik bir tanıma sahipken, $C_t$ ampirik bir fit'tir; teorik bir multifraktal model üzerinden türetilemez (en azından şimdilik). Bu paralellik hem kuvvetli (klasik Markowitz çözüm tekniklerini fraktal duruma uyarlamayı mümkün kılar) hem zayıftır (teorik temelden yoksun olduğu için aşırı-yorum tehlikeli; bkz. [[out-of-sample-cokus]]).

## Formül
Klasik:
$$
\sigma_p^2 = w^T \Sigma w
$$
Fraktal analog:
$$
H_p(w; t) \approx c_t + w^T C_t w
$$
Ortak çözüm iskeleti (Lagrange ile kapalı form):
$$
w^* = M^{-1} (\alpha \mu + \beta \mathbf{1}), \quad M \in \{\Sigma, C_t\}
$$

## Ana Bağlamlar
- [[markowitz-portfoy-teorisi]] orijinal teori
- [[portfoy-hurst-kuadratik-form]] fraktal analog
- [[abcd-parametreleri]] ortak çözüm iskeleti
- [[fraktal-duzeltme-cezasi]] Tauron'un alternatif yaklaşımı

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — projenin kavramsal "köprü" mesajı: yeni teori değil, klasik teorinin fraktal-genişletilmiş ampirik bir uzantısı
- [Tauron](../../projects/tauron/) — fraktal cezalı objectifin de aynı biçimsel iskelete oturduğu gösterimi
- [Seminer](../../projects/) — "Markowitz devam ediyor, sadece matrisi değişiyor" mesajı

## Kaynak
[[aygoren-uyar-2023]], [[markowitz-1952]]
