---
baslik: "Multilevel Monte Carlo Path Simulation"
slug: "giles-2008"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [montecarlo, mlmc, varyans-azaltma]
citekey: giles2008
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Giles 2008 — Multilevel Monte Carlo Path Simulation

## Künye
Michael B. Giles, "Multilevel Monte Carlo Path Simulation", *Operations Research*, 56(3), 607–617, 2008.

## Ana Argüman
SDE-tabanlı MC fiyatlamada farklı çözünürlükteki ayrıklaştırmaları teleskopik biçimde birleştirerek standart MC'nin $\mathcal{O}(\varepsilon^{-3})$ maliyetini $\mathcal{O}(\varepsilon^{-2}\log^2\varepsilon)$ veya $\mathcal{O}(\varepsilon^{-2})$'ye indirmek mümkündür.

## Yöntem
Teleskop kimliği:
$$
\mathbb{E}[P_L] = \mathbb{E}[P_0] + \sum_{\ell=1}^L \mathbb{E}[P_\ell - P_{\ell-1}],
$$
her seviyedeki düzeltme aynı Brown yörüngesiyle eşleştirilir (coupling). Strong order $\beta$ ve maliyet üstü $\gamma$ arasındaki ilişki toplam maliyet rejimini belirler.

## Bulgular
- Avrupa opsiyonu + Euler ($\beta=1$) → $\mathcal{O}(\varepsilon^{-2}\log^2\varepsilon)$
- Avrupa + Milstein ($\beta=2$) → $\mathcal{O}(\varepsilon^{-2})$ — optimal
- Lookback, bariyer, Asya: payoff'a özel coupling teknikleri (Brownian bridge interpolation)
- Numerik deney: Heston, GBM modellerde 10x-100x hızlanma.

## Etkisi
Modern finans MC'sinin standart yöntemi. Kuantum bağlamda An 2021 ve sonrası MLMC + QAE birleşik algoritmalar geliştirdi; bu hibridler Herman 2026'nın da değerlendirdiği rejimlerden biri.

## İlgili Kavramlar
- [[mlmc]]
- [[milstein-semasi]]
- [[euler-maruyama]]
- [[levy-area]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum-MLMC bağlamı (An 2021)
- [Seminer](../../projects/ders/2026-bahar-seminer/) — varyans azaltma örneği
