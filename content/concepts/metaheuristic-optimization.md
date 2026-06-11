---
baslik: "Metasezgisel Optimizasyon (Metaheuristic Optimization)"
slug: "metaheuristic-optimization"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [optimizasyon, algoritma, np-zor, heuristik]
aliases: ["metaheuristic", "metasezgisel", "metaheuristic optimization"]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Metasezgisel Optimizasyon

**NP-zor problemlerde** polinom zamanda kesin çözüm bulunamadığında kullanılan **doğa veya fizik esintili yaklaşık çözüm** algoritmalarının üst-sınıfı. "Meta" = problem üstü; "heuristic" = sezgisel arama.

## Temel İlkeler

- **Exploration (keşif)** vs **exploitation (sömürü)** dengesi
- Popülasyon tabanlı veya tek çözüm tabanlı olabilir
- Garantili global optimum bulamaz; **yeterince iyi yaklaşık** çözüm verir
- Az parametre ile geniş problem ailesine uyarlanabilir

## Yaygın Aileler

| Aile | Örnekler | İlham |
|---|---|---|
| Evrimsel | Genetik Algoritma (GA), Diferansiyel Evrim (DE) | Doğal seçilim, mutasyon |
| Sürü zekası ([[swarm-intelligence]]) | PSO, [[artificial-bee-colony\|ABC]], ACO, Firefly | Hayvan kolonileri |
| Fiziksel | Simulated Annealing (SA), Gravitational Search | Termodinamik, çekim |
| İmmun-esintili | Immune Algorithm (IA) | Bağışıklık sistemi |
| Yerel arama | Tabu Search (TS) | Bellek-temelli arama |

## Avantaj ve Sınırlar

| Avantaj | Sınır |
|---|---|
| NP-zor problemler için pratik çözüm | Garantili optimum yok |
| Esnek (formülasyona uyarlanabilir) | Parametre ayarı önemli (DOE gerekebilir) |
| Az matematiksel önkoşul | Yakınsama tahmini zor |

## Finansta Kullanımı

Portföy optimizasyonu, özellikle [[cardinality-constrained-portfolio|kardinalite kısıtlı portföy]] gibi NP-Complete problemlerde:
- GA (Chang ve diğerleri, 2000)
- PSO (Cura, 2009)
- ABC ([[kalayci-aygoren-2017|Kalayci-Aygören, 2017]])
- ABC-Firefly hibrit (Tuba-Bacanin, 2014)

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — ABC seçimi metasezgisel ailedeki konum
- Potansiyel: [Tauron](../../projects/tauron/), [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/)

## İlgili Kavramlar

- [[swarm-intelligence]]
- [[artificial-bee-colony]]
- [[cardinality-constrained-portfolio]]
- [[markowitz-portfoy-teorisi]]
