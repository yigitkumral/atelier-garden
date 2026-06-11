---
baslik: "Towards Quantum Advantage in Financial Market Risk using Quantum Gradient Algorithms"
slug: "stamatopoulos-2022"
olusturuldu: 2026-05-11
guncellendi: 2026-05-11
etiketler: [kuantum, greeks, gradient-estimation, piyasa-riski, hedging]
citekey: stamatopoulos2022
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Stamatopoulos et al. 2022 — Quantum Gradient Algorithms for Financial Market Risk

## Künye
Nikitas Stamatopoulos, Guglielmo Mazzola, Stefan Woerner, William J. Zeng, "Towards Quantum Advantage in Financial Market Risk using Quantum Gradient Algorithms", *Quantum*, 6, 770, 2022. (arXiv:2111.12509v2) — Goldman Sachs & Co. + IBM Quantum (IBM Research Zurich).

## Ana Argüman
Finansal türevlerin **piyasa riski (Greekler — Delta, Gamma, Vega, Theta, Rho)** kuantum gradient estimation algoritmalarıyla, klasik finite-difference yaklaşımına göre **iki ayrı eksende kuadratik avantaj** ile hesaplanabilir: (1) hedef hata $\varepsilon$ ölçeklemesinde $O(1/\varepsilon^2) \to O(1/\varepsilon)$, (2) Greek sayısı $k$ üzerinde ek kuadratik kazanım. Türev fiyatlamasındaki [[stamatopoulos-2020|Stamatopoulos 2020]] hızlandırmasının doğal Greek-uzantısı.

## Yöntem
- **Quantum gradient estimation** (Jordan 2005, Gilyén 2018 evrimi): payoff fonksiyonunun çoklu parametreye göre türevini paralel kuantum sorgularıyla tahmin.
- **Maximum Likelihood Estimation (MLE) kombinasyonu:** Ölçüm sonrası klasik post-processing ile gradient olasılık dağılımının modunu, mediandan daha iyi tahmin et.
- **Basket option** (path-dependent, çok-varlıklı) üzerinde Vega ($\partial\theta/\partial\sigma$) hesabı sayısal demo.
- Kaynak ihtiyacı analizi: [[chakrabarti-2021|Chakrabarti et al. 2021]] türev fiyatlama threshold'una göre Greek hesabı için **logical clock rate gereksinimi 50 MHz → 7 MHz** (4 Greek için).
- Paralelizasyon: 60 QPU üzerinde her cihazın gereksinimi ~100 kHz'e düşer.

## Bulgular
- Greekler için praktik kaynak ihtiyacı teorik üst-sınırlardan **anlamlı şekilde düşük**.
- Türev fiyatlama için yetersiz olan kuantum donanımı (klasiğe karşı avantajsız), **Greek hesabı için yeterli olabilir** — risk yönetimi kuantum-finans alanında en erken pratik uygulama adayı.
- MLE + gradient kombinasyonu, ham gradient ölçümünden ciddi varyans-azaltma sağlıyor.

## Etkisi
Finansta kuantum üstünlüğüne (quantum advantage) **risk yönetimi tarafından** yaklaşmanın somut yol haritası. Pricing kuantum avantajına ulaşmadan önce hedging/Greek hesabında pratik faydanın görülebileceği teziyle, finansal kurumların kuantum yatırımı stratejisini şekillendirir.

## BS-İçi Kuantum Önemi (Yigit'in Sorusu)
Bu makale **Black-Scholes modelinin kendi içinde** kuantum uygulamasının en yetkin örneklerinden biridir:
- BS dağılımı (log-normal $S_T$) altında Greek ($\Delta, \Gamma, \nu, \Theta, \rho$) hesabı doğrudan ele alınır.
- Klasik finite-difference (her parametreye ayrı MC simülasyonu) yerine tek kuantum sorgusu seti.
- Delta hedging gibi pratik portföy uygulamalarında **anlık güncelleme** olasılığı: bir bankanın portföy Delta'sını saniyede tazeleme.
- Hocanın Slayt 20 ("banka bilançosu = dinamik portföy") tezine doğrudan altyapı: çoklu Greek + çoklu vade + döviz pozisyon ağırlık matrisi anlık hesaplanabilir.

## İlgili Kavramlar
- [[greeks]]
- [[delta-hedging]]
- [[qae]]
- [[kuantum-turev-fiyatlama]]
- [[black-scholes-modeli]]

## Atıf Yapan Projeler
- [Seminer](../../projects/ders/2026-bahar-seminer/) — BS-içi kuantum araştırma kolu (Slayt 18 veya 20'ye 1 cümle eklenebilir)
- [Tauron](../../projects/tauron/) — banka bilançosu portföy tezi için kuantum altyapı referansı
