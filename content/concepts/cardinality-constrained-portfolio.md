---
baslik: "Kardinalite Kısıtlı Portföy Optimizasyonu (CCPO)"
slug: "cardinality-constrained-portfolio"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [portfoy, optimizasyon, np-complete, markowitz, kisit]
aliases: ["CCPO", "Cardinality Constrained Portfolio Optimization"]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Kardinalite Kısıtlı Portföy Optimizasyonu (CCPO)

[[markowitz-portfoy-teorisi|Klasik Markowitz mean-variance modeli]]ne **portföyde tam olarak K hisse senedi tutulmalı** kısıtının eklenmiş hali. Gerçekçi yatırımcı kısıtları (yönetim maliyeti, çeşitlendirme limiti) için pratik öneme sahip.

## Matematiksel Form

$$\min \lambda \cdot w^T \Sigma w - (1-\lambda) \cdot w^T \mu$$

Kısıtlar:
- $\sum w_i = 1$ (toplam ağırlık)
- $\sum z_i = K$ (tam K hisse, $z_i \in \{0,1\}$ binary)
- $\varepsilon_i z_i \leq w_i \leq \delta_i z_i$ (alt/üst sınır)

## Hesaplama Karmaşıklığı

Klasik Markowitz **kuadratik programlama (QP)** problemidir — polinom zamanda kesin çözüm vardır. Kardinalite kısıtı eklendiğinde **karma tamsayılı kuadratik programlama (MIQP)** olur ve **NP-Complete** sınıfına geçer. Büyük portföylerde (N > 100) kesin çözüm yöntemleri (CPLEX, branch-and-bound) makul sürede çözüm üretemez; **metasezgisel yaklaşımlar** zorunlu olur.

## Çözüm Yaklaşımları

| Aile | Örnekler |
|---|---|
| Kesin | Lagrangian relaxation (Shaw 2008), Convex relaxation (Cui 2013), Local relaxation + CPLEX (Murray-Shek 2012) |
| Tek çözümlü heuristik | Tabu Search, Simulated Annealing |
| Popülasyon tabanlı | GA, PSO, ACO, [[artificial-bee-colony|ABC]], Firefly, Cuckoo |
| Hibrit | GA+SA, ABC+Firefly (Tuba-Bacanin 2014), GRASP+QP (Baykasoğlu 2015) |

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — Kalayci-Aygören 2017 makalesinin merkez problemi
- Potansiyel: [Tauron](../../projects/tauron/), [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) ile karşılaştırmalı analiz

## Kaynak

- **[[kalayci-aygoren-2017]]** — ABC ile CCPO ana çalışması
- Chang, T.J., Meade, N., Beasley, J.E., Sharaiha, Y.M. (2000). *Computers & Operations Research*, 27, 1271-1302 (standart formülasyon)
- Moral-Escudero ve diğerleri (2006). NP-Complete kanıtı

## İlgili Kavramlar

- [[markowitz-portfoy-teorisi]]
- [[artificial-bee-colony]]
- [[metaheuristic-optimization]]
- [[etkin-sinir]]
- [[minimum-varyans-portfoyu]]
