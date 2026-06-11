---
baslik: "Parabolik Fit Modeli ζ(q) = aq² + bq + c"
slug: "parabolik-fit-modeli"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, multifraktal, parametrelendirme, fit]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Parabolik Fit Modeli (ζ_q için)

## Özü
[[zeta-q-olcekleme]] eğrisini üç parametreyle ($a, b, c$) yakalayan, multifraktal analizde standart hâle gelmiş kompakt parametrik model.

## Tanım
Empirik olarak finansal serilerde $\zeta_q$ neredeyse içbükey bir parabol gibi davranır; bu nedenle $\zeta_q = a q^2 + b q + c$ formu pratik bir fit'tir. Üç parametrenin yorumu net: $c$ sabit kayma terimi (genelde 0 alınır ya da sıfıra yakın çıkar), $b$ baskın Hurst-benzeri ölçek üsteli, $a < 0$ ise multifraktallığın eğrilik şiddetidir. $a = 0$ tek-fraktal limittir. Bu form üzerinden multifraktal spektrum analitik olarak Legendre dönüşümü ile çıkarılabilir (bkz. [[multifraktal-spektrum]]) ve şiddet için tek-skalar ölçü $\lambda = \sqrt{-2a}$ tanımlanır (bkz. [[multifraktallik-siddeti-lambda]]).

## Formül
$$
\zeta_q = a q^2 + b q + c
$$
Parametre kısıtı: $a \le 0$ (içbükeylik). Sınırlar:
- $a = 0$ → monofraktal (tek $H = b$)
- $|a|$ büyük → güçlü multifraktallık

Hurst:
$$
H = \frac{\zeta_2}{2} = \frac{4a + 2b + c}{2} = 2a + b + \frac{c}{2}
$$

## Ana Bağlamlar
- [[zeta-q-olcekleme]] fit edilen eğri
- [[multifraktallik-siddeti-lambda]] $a$'nın tek-sayı özeti
- [[multifraktal-spektrum]] parabolik durumda kapalı form
- [[m-q-tau-momentleri]] $\zeta_q$'yu hesaplayan ham veri

## Projelerde Kullanım
- [Tauron](../../projects/tauron/) — fraktal düzeltme cezasının parametrelendirilmesi tam olarak $(a, b, c)$ üzerinden yürür
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — varlık-bazlı fit, sonra portföy ağırlıklarıyla harmanlama analizi
- [Seminer](../../projects/) — kompakt sunum için tercih edilen parametrelendirme

## Kaynak
[[sornette-multifractal]]
