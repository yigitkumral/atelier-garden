---
baslik: "Monte Carlo Methods in Financial Engineering"
slug: "glasserman-2003"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [montecarlo, kitap, finans]
citekey: glasserman2003
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Glasserman 2003 — Monte Carlo Methods in Financial Engineering

## Künye
Paul Glasserman, *Monte Carlo Methods in Financial Engineering*, Springer (Stochastic Modelling and Applied Probability Vol. 53), 2003.

## Ana Argüman
Finansal türev fiyatlama, risk yönetimi ve Greek hesaplamalarında Monte Carlo, yüksek boyutlu integraller karşısında [[boyutluluk-laneti]]'nden korunan tek pratik yöntem. Kitap, ham MC'den ileri varyans azaltma, türev tahmini ve Amerikan opsiyonu LSM'ye kadar tüm cephaneliği matematiksel olarak titiz şekilde sunar.

## Yöntem
Olasılıksal yakınsama teorisi + SDE ayrıklaştırma analizi + uygulamalı algoritma tasarımı. Her bölüm: teorik temel → algoritma → finansal örnek → varyans hesabı.

## Bulgular
- Ham MC: $\mathcal{O}(N^{-1/2})$ standart hata, boyut-bağımsız.
- Varyans azaltma: control variates, antithetic, importance sampling, stratification, low-discrepancy (quasi-MC).
- SDE ayrıklaştırma: [[euler-maruyama]] weak order 1, [[milstein-semasi]] strong order 1 — strong order varyans azaltmada (özellikle [[mlmc]] öncesi) kritik.
- Greek tahmini: pathwise, likelihood ratio, malliavin yöntemleri.
- Amerikan opsiyon: Longstaff-Schwartz regresyon tabanlı.

## Etkisi
Akademik finans MC'sinin standart başvurusu. Sonraki tüm kuantum-MC çalışmaları (Montanaro 2015, Stamatopoulos 2020, Herman 2026) Glasserman'ı klasik baseline olarak referans verir.

## İlgili Kavramlar
- [[monte-carlo-entegrasyonu]]
- [[euler-maruyama]]
- [[milstein-semasi]]
- [[boyutluluk-laneti]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — klasik MC zemini
- [Seminer](../../projects/ders/2026-bahar-seminer/) — temel referans
