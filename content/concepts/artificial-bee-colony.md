---
baslik: "Yapay Arı Kolonisi Algoritması (Artificial Bee Colony — ABC)"
slug: "artificial-bee-colony"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [optimizasyon, metasezgisel, surul-zekasi, algoritma, finans-uygulamasi]
aliases: ["ABC", "Artificial Bee Colony", "Yapay Arı Kolonisi", "Karaboğa algoritması"]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Yapay Arı Kolonisi Algoritması (ABC)

**Dervis Karaboğa** tarafından 2005'te Erciyes Üniversitesi'nde önerilen, **bal arılarının nektar arayış davranışından** esinlenmiş bir [[metaheuristic-optimization|metasezgisel optimizasyon]] algoritması. [[swarm-intelligence|Sürü zekası]] ailesinin önemli bir üyesidir.

## Temel Mekanizma

Üç tip arı paralel çalışır:

- **Employed bees (görevli arılar):** Mevcut çözüm civarında lokal arama yapar — exploitation
- **Onlooker bees (gözcü arılar):** Görevli arıların fitness-orantılı bilgi paylaşımına (waggle dance) göre olasılıkla iyi çözümlere yönelir
- **Scout bees (kâşif arılar):** `limit` parametresi aşılan terkedilmiş çözümlerin yerine rasgele yeni nokta üretir — exploration

Yeni komşu üretimi: $x'_i = x_i + \phi_i \cdot (x_i - x_k)$, $\phi \in [-1,1]$.

## Avantajlar

- Az kontrol parametresi (modification rate, scout production period, limit)
- Parametre duyarlılığı düşük
- Sürekli, ayrık ve karma optimizasyon problemlerine uyarlanabilir
- Türkiye kaynaklı yerel metodolojik miras

## Sınırlar

- Yakınsama hızı [[markowitz-portfoy-teorisi|PSO'dan daha yavaş]] olabilir
- Yüksek-boyutlu problemlerde scout faz oranı dikkatli ayarlanmalı

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — Kalayci-Aygören 2017 makalesinin temel algoritması; Smart Connections embedded vektörlerle olası sentez aranıyor
- Potansiyel: [Tauron](../../projects/tauron/) multifraktal portföyle hibrit kullanım

## Kaynak

- **[[kalayci-aygoren-2017]]** — ABC ile [[cardinality-constrained-portfolio|kardinalite kısıtlı portföy optimizasyonu]] ana referansı
- Karaboga, D. (2005). "An idea based on honey bee swarm for numerical optimization." TR06, Erciyes University
- Karaboga, D., Basturk, B. (2007). *Journal of Global Optimization*, 39(3), 459-471

## İlgili Kavramlar

- [[metaheuristic-optimization]]
- [[swarm-intelligence]]
- [[cardinality-constrained-portfolio]]
- [[markowitz-portfoy-teorisi]]
