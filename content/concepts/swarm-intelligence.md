---
baslik: "Sürü Zekası (Swarm Intelligence)"
slug: "swarm-intelligence"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [algoritma, optimizasyon, biyolojik-esinti, paralellik]
aliases: ["swarm intelligence", "sürü zekası", "kolektif zeka"]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Sürü Zekası

**Basit ajanların** (arı, karınca, kuş, balık, vd.) **yerel etkileşim kurallarından** ortaya çıkan **kolektif problem çözme** davranışı. Merkezi kontrol yok; her ajan komşularıyla iletişim kurar veya çevreyi modifiye eder (örn. feromon).

[[metaheuristic-optimization|Metasezgisel optimizasyon]] ailesinin önemli bir alt-kümesidir.

## Temel İlkeler

- **Dağıtık karar:** Her ajan kendi yerel bilgisine göre hareket eder
- **Stigmergy:** Ajanlar çevre üzerinden dolaylı iletişim kurar (feromon, waggle dance)
- **Emergent behavior:** Tek ajanın yapamayacağı çözümler topluluk seviyesinde ortaya çıkar
- **Robustness:** Bir ajan kaybolsa sistem devam eder

## Algoritma Örnekleri

| Algoritma | İlham | Ana Operatör |
|---|---|---|
| **PSO** (Particle Swarm Optimization) | Kuş/balık sürüleri | Hız vektörü güncelleme (kişisel + global best) |
| **ACO** (Ant Colony Optimization) | Karınca feromonu | Feromon birikimi + buharlaşma |
| **[[artificial-bee-colony\|ABC]]** | Bal arıları, foraging | Employed/onlooker/scout fazları, waggle dance |
| **Firefly** | Ateşböceği parlaklığı | Çekim katsayısı + rasgele yürüyüş |
| **Cuckoo Search** | Guguk kuşu yumurta saklama | Lévy uçuşları + nest replacement |
| **Cat Swarm** | Kedi davranışı (arama/izleme) | Seeking + tracing modları |
| **Fish Swarm** | Balık sürü davranışı | Prey/follow/swarm operatörleri |

## Foraging Metaforu

Foraging (yiyecek arama) sürü zekasında ortak temadır:
- **Exploitation:** Bilinen iyi kaynağın civarını sömürmek
- **Exploration:** Yeni kaynak keşfetmek
- ABC'de bu dengeleme `limit` parametresiyle yapılır

Bu metafor Obsidian Smart Connections'ın "ilgili notları bul" davranışıyla yapısal benzerlik gösterir — kullanıcı "current note" civarındaki semantic komşuları sömürür, bazen unutulmuş notlara "scout" gibi geri döner.

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — foraging metaforu sentez eksenlerinden biri (E2)

## İlgili Kavramlar

- [[artificial-bee-colony]]
- [[metaheuristic-optimization]]
- [[semantic-search]] — foraging metaforu burada da var
