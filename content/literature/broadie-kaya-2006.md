---
baslik: "Exact Simulation of Stochastic Volatility and Other Affine Jump Diffusion Processes"
slug: "broadie-kaya-2006"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [montecarlo, heston, stokastik-volatilite]
citekey: broadie2006
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Broadie-Kaya 2006 — Exact Simulation of Stochastic Volatility

## Künye
Mark Broadie, Özgür Kaya, "Exact Simulation of Stochastic Volatility and Other Affine Jump Diffusion Processes", *Operations Research*, 54(2), 217–231, 2006.

## Ana Argüman
Heston modelinde varyans sürecinin geçiş yoğunluğu non-central chi-squared, entegre varyansın koşullu dağılımı ise karakteristik fonksiyon üzerinden tersine çevrilebilir; bu sayede $S_T$ ve $V_T$ **ayrıklaştırma hatasız** (exact) örneklenebilir.

## Yöntem
Heston SDE:
$$
dS_t = rS_t\, dt + \sqrt{V_t}\, S_t\, dW^S_t, \quad dV_t = \kappa(\theta - V_t)\, dt + \sigma_v \sqrt{V_t}\, dW^V_t.
$$

Algoritma adımları:
1. $V_T \mid V_0$ → non-central chi-squared dağılımdan örnekle (CIR exact transition).
2. $\int_0^T V_s\, ds \mid V_0, V_T$ → karakteristik fonksiyonu kapalı formda; sayısal Fourier inversion ile yoğunluğu çıkar, örnekle.
3. $\int_0^T \sqrt{V_s}\, dW^V_s$ → yukarıdaki integral ve $V_0, V_T$ üzerinden cebirsel olarak çözülür.
4. $S_T$ → koşullu log-normal.

## Bulgular
- Hiçbir Euler/Milstein bias yok — strong order $\infty$.
- Maliyet: Fourier inversion adımı ~50-100 grid noktası, makul.
- Andersen QE ve diğer "almost exact" şemalardan daha hassas; biraz daha pahalı.
- Feller koşulu ihlal edildiğinde bile (sınırda) çalışıyor.

## Etkisi
Heston MC fiyatlamasının altın standardı. Kuantum bağlamda Herman 2026, Broadie-Kaya'yı [[fast-forwardability]] uygulayan kanonik klasik prosedür olarak referans verir; karakteristik fonksiyon yolu kuantum durum yükleme stratejisinin hazır altyapısıdır.

## İlgili Kavramlar
- [[heston-stokastik-volatilite]]
- [[karakteristik-fonksiyon]]
- [[non-central-chi-squared]]
- [[fast-forwardability]]
- [[cir-modeli]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Heston exact simülasyonu, kuantum yükleme stratejisi
