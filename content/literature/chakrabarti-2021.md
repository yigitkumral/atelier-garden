---
baslik: "Threshold Quantum Speedup for Path-Dependent Derivatives"
slug: "chakrabarti-2021"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, yol-bagimli, fiyatlama]
citekey: chakrabarti2021
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Chakrabarti et al. 2021 — Path-Dependent Derivatives via Reparameterization

## Künye
Shouvanik Chakrabarti, Rajiv Krishnakumar, Guglielmo Mazzola, Nikitas Stamatopoulos, Stefan Woerner, William J. Zeng, "A Threshold for Quantum Advantage in Derivative Pricing", *Quantum*, 5, 463, 2021. (arXiv:2012.03819)

## Ana Argüman
Yol-bağımlı opsiyonlarda (Asya, lookback, autocallable, TARN) kuantum hızlanmasını koruyabilmek için tüm Brown yörüngesini ayrıklaştırarak kuantum durumuna yüklemek yerine **dağılım reparameterization** ile boyut sayısı düşürülmeli; aksi hâlde devre derinliği quadratic kazancı yutar.

## Yöntem
- Standart yaklaşım: $T/\Delta t$ adımlık Brown artımları $\Delta W_1, \dots, \Delta W_N$ kuantum durumuna yükle, yörünge devresel olarak topla — pahalı.
- Reparameterization: yörüngeyi düşük-boyutlu Karhunen-Loève (Brown bridge) bileşenleri olarak yaz; yüksek-frekanslı bileşenleri kes.
- Payoff hesabını ana bileşenler üzerinden yap → daha sığ devre.
- Resource estimation: TARN otokollar için 8000 mantıksal kubit, $10^7$ T-gate (klasik MC ile karşılaştırmalı).

## Bulgular
- Yol-bağımlı opsiyonlarda klasik MC'ye göre **threshold** ötesi (yeterli devre derinliği toleransı varsa) quadratic hızlanma korunabilir.
- TARN, autocallable gibi karmaşık ürünlerde kuantum speedup pratikte ulaşılması zor ama matematiksel olarak mümkün.

## Etkisi
Herman 2026'nın yol-bağımlı opsiyon bölümünde doğrudan referans verilir; reparameterization tekniği [[fast-forwardability]] kavramıyla birleşir.

## İlgili Kavramlar
- [[kuantum-turev-fiyatlama]]
- [[fast-forwardability]]
- [[qae]]
- [[asyali-opsiyonu]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — yol-bağımlı genişletme stratejisi
