---
baslik: "Andersen & Piterbarg (2007) — Moment Explosions in Stochastic Volatility Models"
slug: "andersen-piterbarg-2007"
yazarlar: ["Leif B. G. Andersen", "Vladimir V. Piterbarg"]
yil: 2007
dergi: "Finance and Stochastics"
volume: 11
issue: 1
sayfalar: "29-50"
doi: "10.1007/s00780-006-0011-7"
citekey: "andersenpiterbarg2007"
etiketler: [finans, stokastik-volatilite, moment-patlama, ileri-konu]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Andersen & Piterbarg (2007) — Moment Explosions in Stochastic Volatility Models

## Künye
Andersen, L. B. G., & Piterbarg, V. V. (2007). Moment Explosions in Stochastic Volatility Models. *Finance and Stochastics*, 11(1), 29-50. https://doi.org/10.1007/s00780-006-0011-7

## Ana Argüman
[[heston-stokastik-volatilite]] ve onun benzeri ailesi modeller içinde, log-fiyatın moment üreten fonksiyonu yalnızca model parametrelerine bağlı kritik bir vadeye kadar sonludur; bu eşiğin ötesinde yüksek dereceli momentler patlar. Patlama vadesi, parametrelerin ve moment derecesinin eksiksiz fonksiyonu olarak kapalı-form karakterize edilebilir.

## Yöntem
Yazarlar, Heston'un karakteristik fonksiyonunu çözen Riccati ODE'lerinin patlama zamanlarını analitik olarak inceler; affin terim yapılı modelleri içeren genel sınıf için patlama eşiği ve patlamadan korunma rejimini ayırt eder. Kritik moment fonksiyonu $\bar{u}(T)$ ve [[vol-of-vol]] / [[leverage-effect]] korelasyonu ile [[mean-reversion]] hızının bu eşiğe nasıl katkı yaptığı türetilir.

## Bulgular
Variance swap, derinden out-of-the-money opsiyon, log-kontrat ve volatilite türevleri için naif Monte Carlo varyansının sonsuz olabileceği rejimler net olarak haritalanır. Teori, hangi vadelerde hangi moment dereceleri için iskonto-altında integrallenmenin geçerli olduğunu söyler ve sayısal şemalar (kontrol değişken, [[mlmc]]) için gerekli düzeltmelerin tasarım rehberini sunar.

## Etkisi
Stokastik volatilite literatüründe parametrik kalibrasyonun teorik sınırlarını çizen referans makaledir; [[volatility-smile]]'in kuyruk asimptotiği ve volatilite türevi piyasasının doğru fiyatlamasında temel araçtır. Kuantum hesaplama makaleleri (örn. Quantum Speedups for Derivative Pricing) tarafından da test rejimlerini tanımlamada referans alınır.

## İlgili Kavramlar
- [[heston-stokastik-volatilite]]
- [[moment-patlama]]
- [[vol-of-vol]]
- [[leverage-effect]]
- [[volatility-smile]]

## Atıf yapan projeler
- [Seminer](../../projects/ders/2026-bahar-seminer/)
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/)
