---
baslik: "Fraktal Piyasa Hipotezi (FMH)"
slug: "fraktal-piyasa-hipotezi-fmh"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [hipotez, fraktal, peters, paradigma]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Fraktal Piyasa Hipotezi (FMH)

## Özü
Etkin Piyasa Hipotezi'ne (EPH) alternatif olarak Edgar Peters tarafından sistematize edilmiş; piyasaların farklı ufuklardaki yatırımcıların etkileşiminden doğan **ölçek-değişmez** (scale-invariant) bir yapıya sahip olduğunu öne süren paradigma.

## Tanım
EPH, getirilerin i.i.d., dağılımın Gaussian olduğunu ve piyasanın bilgiye anında ve doğru fiyatlama yaptığını varsayar. FMH ise (1) farklı zaman ufuklarındaki yatırımcıların (gün-içi tüccardan emekli fonuna) bilgiyi farklı ölçeklerde kullandığını, (2) bunun sonucunda fiyat serilerinin uzun-vadeli hafıza taşıdığını ($H \neq 0.5$, [[hurst-exponent]]), (3) dağılımın fat-tailed olduğunu (bkz. [[fat-tailed-dagilim]]), (4) volatilite kümeleri ve multifraktal yapı oluştuğunu öne sürer. FMH, EPH'yi tamamen reddetmez; "piyasa belirli ufuklarda etkin gibidir, başka ufuklarda hatırlar" şeklinde nüanslandırır. Hipotez tartışmalıdır — bazı eleştirmenler ($H \neq 0.5$ gözleminin sonlu örneklem artefaktı olabileceğini iddia ederler — bkz. [[estimator-gurultusu-bias-variance]]). Yine de modern multifraktal finans literatürünün kavramsal temelidir.

## Formül
Ölçek-değişmezlik (FMH'nin ampirik imzası):
$$
P(|r_\tau| > x) \sim x^{-\beta}, \qquad \beta \in (2, 5) \text{ tipik}
$$
Multifraktal genelleştirme:
$$
\mathbb{E}[|r_\tau|^q] \sim \tau^{\zeta_q}, \quad \zeta_q \neq qH
$$
Klasik EPH limiti: $\zeta_q = q/2$ (Brownian).

## Ana Bağlamlar
- [[hurst-exponent]] FMH'nin imza parametresi
- [[fat-tailed-dagilim]] dağılımsal tezahür
- [[multifraktal-spektrum]] modern kantitatif çerçeve
- [[zeta-q-olcekleme]] EPH'den sapma ölçümü

## Projelerde Kullanım
- [Seminer](../../projects/) — paradigmal çerçeveleyici sunum öğesi; "neden fraktal bakış?" sorusunun cevabı
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — projenin felsefi arka planı
- [Tauron](../../projects/tauron/) — multifraktal cezanın motivasyonel temeli

## Kaynak
[[peters-1991]], [[mandelbrot-hudson]]
