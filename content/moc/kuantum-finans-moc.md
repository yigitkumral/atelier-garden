---
baslik: "Kuantum Finans — Map of Content (MOC)"
slug: "kuantum-finans-moc"
tip: moc
olusturuldu: 2026-05-24
guncellendi: 2026-05-24
etiketler: [moc, kuantum, finans, opsiyon-fiyatlama, monte-carlo]
aliases: ["Quantum Finance", "Quantum Computing Finance", "QFinance"]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Kuantum Finans — Map of Content

Bu MOC, kuantum bilgisayarlarla finansal türev fiyatlama, Monte Carlo hızlandırma, opsiyon değerleme ve Black-Scholes-ötesi modellerin tüm vault notlarını, projeleri ve literature referanslarını tek dosyadan navigable yapar. Herman et al. (2026) çevirisi ve PAÜ Seminer'i bu MOC'un birincil çıktı odaklarıdır.

## Niçin Bu MOC?

Atelier'de kuantum-finans ekseninde **2 aktif proje (Herman çevirisi + Seminer), 17+ literature kaynağı ve 25+ atomic concept** var — bu çok dağınık bir alan. Klasik finans literatürü (Black-Scholes, Heston, Hull) ile kuantum bilgisayar literatürü (QAE, HHL, Grover) köprülenmek zorunda. MOC bu iki dünyayı birleştirir.

## Ana Literature Kaynakları

### Kuantum-Finans Çekirdek

| Citekey | Künye | Rol |
|---------|-------|-----|
| [@herman2026] | [[herman-2026]] — Herman et al. (2026) — Quantum Speedups for Derivative Pricing Beyond Black-Scholes | **105-sayfa ana referans, Atelier çevirisinin kaynağı** |
| [@stamatopoulos2020] | [[stamatopoulos-2020]] — Stamatopoulos et al. (2020) — Option Pricing using Quantum Computers | Klasik MC 1/√N vs kuantum AE 1/N |
| [@stamatopoulos2022] | [[stamatopoulos-2022]] — Stamatopoulos et al. (2022) — Quantum Gradient Algorithms for Market Risk | 28-qubit basket Greek, banka uygulaması |
| [@woerner2019] | [[woerner-egger-2019]] — Woerner & Egger (2019) — Quantum Risk Analysis | npj Quantum Information, IBM Q kullanımı |
| [@chakrabarti2021] | [[chakrabarti-2021]] — Chakrabarti et al. (2021) — Quantum option pricing | JPMorgan grubu, fault-tolerant analiz |

### Klasik Finans Çekirdek (Quantum'un Karşılaştığı Klasik)

| Citekey | Künye | Rol |
|---------|-------|-----|
| [@black1973] | [[black-scholes-1973]] — Black & Scholes (1973) — The Pricing of Options | Klasik opsiyon fiyatlama formülü |
| [@heston1993] | [[heston-1993]] — Heston (1993) — Closed-Form Solution for Stochastic Volatility | Stokastik volatilite, BS-ötesi |
| [@cir1985] | [[cir-1985]] — Cox, Ingersoll, Ross (1985) — Faiz Modeli | Mean-reversion, square-root diffusion |
| [@hull2008] | [[hull-2008]] — Hull (2008) — Options, Futures, Derivatives | Pedagojik referans |
| [@andersen-piterbarg-2007] | [[andersen-piterbarg-2007]] — Andersen & Piterbarg (2007) — Moment Patlamaları | Heston'da moment kararsızlığı |
| [@broadie2006] | [[broadie-kaya-2006]] — Broadie & Kaya (2006) — Exact Heston Simulation | Klasik Heston'un kesin simülasyonu |

### Kuantum Algoritma Çekirdeği

| Citekey | Künye | Rol |
|---------|-------|-----|
| [@grover1996] | [[grover-1996]] — Grover (1996) — Quantum Search Algorithm | Amplitude amplification temeli |
| [@brassard2002] | [[brassard-2002]] — Brassard et al. (2002) — Quantum Amplitude Amplification & Estimation | QAE'nin teorik temeli |
| [@montanaro2015] | [[montanaro-2015]] — Montanaro (2015) — Quantum Speedup of Monte Carlo Methods | QMCI teorik makale |
| [@hhl2009] | [[hhl-2009]] — Harrow, Hassidim, Lloyd (2009) — Quantum Linear Solver | Doğrusal sistemler için hızlandırma |
| [@gilyen2018] | [[gilyen2018]] — Gilyen et al. (2018) — Quantum Singular Value Transformation | QSVT, modern kuantum algoritmaları |
| [@mcardle2022] | [[mcardle-2022]] — McArdle et al. (2022) — Quantum Computational Chemistry | Yan bağlam: kuantum simülasyon |
| [@an2021] | [[an-2021]] — An (2021) — Quantum Time-Marching | Zaman-yürüyüş tabanlı kuantum çözüm |

### Klasik Monte Carlo Yan Literatürü

| Citekey | Künye | Rol |
|---------|-------|-----|
| [@glasserman2003] | [[glasserman-2003]] — Glasserman (2003) — Monte Carlo Methods in Financial Engineering | Klasik MC referansı (kitap) |
| [@giles2008] | [[giles-2008]] — Giles (2008) — Multilevel Monte Carlo | MLMC, klasık varyans azaltma |

## Concept Ailesi

### Kuantum Algoritma Katmanı

- [[qae]] — Quantum Amplitude Estimation (kuadratik hızlandırma çekirdeği)
- [[qmci]] — Quantum Monte Carlo Integration
- [[qet]] — Quantum Expectation Value türeticisi
- [[fast-forwardability]] — sabit-derinlik kuantum simülasyon kavramı
- [[kuantum-turev-fiyatlama]] — derivatives pricing pipeline
- [[boyutluluk-laneti]] — yüksek-boyut MC zorluğu, kuantum üstünlüğü

### Klasik Finans Çekirdeği

- [[black-scholes]] — BS formülü ve varsayımları
- [[heston-stokastik-volatilite]] — stochastic vol modeli
- [[geometric-brownian-motion]] — GBM, BS'in temel süreci
- [[brownian-motion-wiener]] — Wiener süreci tanım
- [[drift]] — sürüklenme parametresi
- [[vol-of-vol]] — volatilitenin volatilitesi
- [[mean-reversion]] — geri çekme dinamiği
- [[cir-modeli]] — CIR faiz modeli
- [[feller-kosulu]] — CIR pozitiflik koşulu
- [[leverage-effect]] — fiyat-volatilite korelasyonu
- [[volatility-smile]] — IV smile/skew

### Opsiyon ve Türev Yapıları

- [[avrupa-opsiyonu]] — vanilla opsiyon
- [[asyali-opsiyonu]] — ortalama-tabanlı egzotik
- [[payoff-fonksiyonu]] — K/Z eğrisi
- [[greeks]] — Delta/Gamma/Vega/Theta
- [[delta-hedging]] — replicasyon stratejisi
- [[karakteristik-fonksiyon]] — Fourier dönüşüm yaklaşımı

### Sayısal & Stokastik Hesap

- [[ito-calculus]] — stokastik integral temeli
- [[euler-maruyama]] — birinci-derece ayrık SDE çözücü
- [[milstein-semasi]] — ikinci-derece ayrık SDE
- [[monte-carlo-entegrasyonu]] — klasik MC tabanı
- [[mlmc]] — Multilevel Monte Carlo
- [[non-central-chi-squared]] — CIR'in dağılımı
- [[moment-patlama]] — Heston moment kararsızlığı
- [[levy-area]] — yüksek-derece şemalar için
- [[bipartite-korelasyon]] — quantum amplitude analizi
- [[kovaryans-matrisi]] — multi-asset bağımlılık

## İlgili Projeler

| Proje | Bağlam |
|-------|--------|
| [Herman 2026 Çeviri Eğitim](../../projects/herman-2026-ceviri-egitim/) | Herman et al. (2026) — 105 sayfa Türkçe çeviri + yorum + eğitim rehberi |
| [2026 Bahar Seminer](../../projects/ders/2026-bahar-seminer/) | Quantum Computing in Finance — PAÜ sunumu (23 slayt, Stamatopoulos + Herman ana) |

## Açık Sorular / Araştırma Yönü

- **Kuantum üstünlüğü (advantage):** Hangi finansal problemde gerçek polynomial-üstü hızlandırma? Şu an kanıtlı olanlar: QAE → klasik MC üzerinde **kuadratik**.
- **Donanım gerçeği:** Herman et al. (2026) ile birlikte gelen **resource estimation** — kaç qubit, kaç error-corrected gate gerek? Pratik fault-tolerant hardware henüz uzak.
- **BS-ötesi modeller:** Heston, jump-diffusion, fractional models — kuantum-fast-forwardable mi? Herman'ın merkez katkısı bu sınıflama.
- **Risk metrikleri:** Stamatopoulos 2022 — gradient algoritmalarıyla Greek hesaplama; ALM'de banka uygulaması.

## Sonraki Adımlar (Çeviri ve Yazım İçin)

Bu MOC Herman çevirisi sürecinde bölüm-bazlı **bağlam haritası** olarak kullanılabilir:
1. Çeviri yapılırken her teknik terim → ilgili concept notuna wikilink (örn. "fast-forwardability" → [[fast-forwardability]])
2. Eğitim rehberi yazılırken her bölüm önerilen concept notları sıralanır (öğrenci için "önce şu, sonra şu" rotası)
3. Sunum/seminer hazırlanırken bu MOC slayt-sıralama önerisi haline gelir

---

*Bu MOC'a yeni concept/literature notu eklendiğinde elle güncellenir. Otomatik index için Dataview veya Bases sorgusu da kurulabilir (P2 aksiyonu).*
