---
baslik: "Kuantum Türev Fiyatlama"
slug: "kuantum-turev-fiyatlama"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, finans, fiyatlama]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Kuantum Türev Fiyatlama

## Özü
Finansal türev araçların (opsiyon, forward, faiz türevi vb.) fiyatını, Black-Scholes ötesi modellerde [[qae]] + [[qmci]] + [[fast-forwardability]] üçlüsüyle quadratic kuantum hızlanmasıyla hesaplama çerçevesi; Herman et al. 2026'nın ana katkısı.

## Tanım
Risk-nötr fiyat:

$$
\Pi_0 = e^{-rT}\, \mathbb{E}^{\mathbb{Q}}[\Phi(\{S_t\}_{t \in [0,T]})],
$$

burada $\Phi$ payoff fonksiyonu (yol-bağımlı veya değil), $S_t$ altında yatan varlık fiyatı bir SDE ile yönetilir.

**Klasik:** Monte Carlo $\mathcal{O}(\sigma^2/\varepsilon^2)$ örnek.

**Kuantum çerçeve (Herman et al. 2026):**
1. $S_T$ (veya yörünge) dağılımını [[fast-forwardability]] üzerinden kuantum durumuna yükle.
2. Payoff $\Phi$'yi genliğe kodla — verimli aritmetik veya [[mcardle-2022]] tarzı doğrudan yükleme.
3. [[qae]] uygula — $\mathcal{O}(1/\varepsilon)$ kuantum sorgu maliyetiyle $\Pi_0$ tahmin.

**Kapsanan modeller:**
- Black-Scholes (zaten log-normal — trivial fast-forward)
- [[heston-stokastik-volatilite]] — Broadie-Kaya exact + Fourier
- SABR, jump-diffusion, Lévy süreçleri — karakteristik fonksiyon yolu
- Yol-bağımlı Asya/lookback — Chakrabarti 2021 reparameterization

**Engeller:** Devre derinliği, $T$-bağımlı pre-factor, hata kalibrasyonu, NISQ-ötesi donanım. Pratik üstünlük (quantum advantage) henüz teorik; Stamatopoulos 2020 ve sonrası küçük örnek devreleri göstermiş.

## Ana Bağlamlar
- [[qae]] — motor
- [[qmci]] — entegrasyon çerçevesi
- [[fast-forwardability]] — koşul
- [[karakteristik-fonksiyon]] — yarı-analitik yol
- [[heston-stokastik-volatilite]] — kanonik test modeli

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — projenin ana konusu (Herman et al. çevirisi + yorumları)
- [Seminer](../../projects/ders/2026-bahar-seminer/) — sunum çekirdeği

## Kaynak
[[herman-2026]], [[stamatopoulos-2020]], [[chakrabarti-2021]]
