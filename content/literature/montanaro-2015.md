---
baslik: "Quantum Speedup of Monte Carlo Methods"
slug: "montanaro-2015"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, montecarlo, hizlanma]
citekey: montanaro2015
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Montanaro 2015 — Quantum Speedup of Monte Carlo Methods

## Künye
Ashley Montanaro, "Quantum Speedup of Monte Carlo Methods", *Proceedings of the Royal Society A*, 471(2181), 20150301, 2015. (arXiv:1504.06987)

## Ana Argüman
Klasik Monte Carlo'nun beklenen değer tahmininde $\mathcal{O}(\sigma^2/\varepsilon^2)$ örnek karmaşıklığı, kuantum amplitude estimation kullanılarak $\mathcal{O}(\sigma/\varepsilon)$'ye indirilebilir — quadratic hızlanma her sınırlı varyanslı $f$ için geçerlidir.

## Yöntem
Üç ana algoritma:
1. **Bounded output ($f \in [0,1]$):** Doğrudan QAE uygula → $\mathcal{O}(1/\varepsilon)$ sorgu.
2. **Bounded variance:** $\mathbb{E}[X]$, $\mathrm{Var}(X) \le \sigma^2$ verili → adaptive QAE → $\mathcal{O}(\sigma/\varepsilon)$.
3. **General real-valued:** Median trick + boyut bölme → aynı asimptotik.

Klasik $X$ rastgele değişkeninin Çıkış oracle'ı $\mathcal{A}_X$ olarak kuantum devresine kodlanır; ardından QAE çalıştırılır.

## Bulgular
- Speedup koşulsuz quadratic (varyans bilgisi gerekmiyor).
- Median-of-means yapısı kuantum durumda da işliyor.
- Multi-dimensional / yüksek boyutlu MC için genel speedup.

## Etkisi
Kuantum-MC'nin formal teorik temeli. Sonraki tüm uygulamalı çalışmalar (Stamatopoulos 2020, Chakrabarti 2021, Herman 2026) Montanaro'yu doğrudan referans alır. Türev fiyatlama, risk yönetimi (CVaR), Bayesian inference, MCMC — hepsi bu çatı altında.

## İlgili Kavramlar
- [[qmci]]
- [[qae]]
- [[monte-carlo-entegrasyonu]]
- [[brassard-2002]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — temel speedup teoremi
- [Seminer](../../projects/ders/2026-bahar-seminer/) — kuantum-finans tezinin teorik dayanağı
