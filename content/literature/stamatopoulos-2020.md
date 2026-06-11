---
baslik: "Option Pricing using Quantum Computers"
slug: "stamatopoulos-2020"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, opsiyon-fiyatlama, deney]
citekey: stamatopoulos2020
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Stamatopoulos et al. 2020 — Option Pricing using Quantum Computers

## Künye
Nikitas Stamatopoulos, Daniel J. Egger, Yue Sun, Christa Zoufal, Raban Iten, Ning Shen, Stefan Woerner, "Option Pricing using Quantum Computers", *Quantum*, 4, 291, 2020. (arXiv:1905.02666)

## Ana Argüman
[[qae]] tabanlı kuantum opsiyon fiyatlama, Avrupa, Asya ve bariyer opsiyonlar için NISQ-uyumlu küçük devrelerde uçtan uca uygulanabilir; klasik MC'ye göre quadratic asimptotik hızlanma korunur.

## Yöntem
- Black-Scholes log-normal dağılımı qGAN (kuantum üretici düşman ağ) veya Grover-Rudolph ile yükle.
- Payoff $\Phi(S_T) = \max(S_T - K, 0)$ için linear/lineer-parça yaklaşım, kontrollü rotasyon devreleriyle genliğe kodla.
- IQAE (Iterative Quantum Amplitude Estimation, Grinko 2019) ile faz tahmini olmadan $\mathbb{E}[\Phi]$ tahmin et.
- IBM Q donanımında küçük kubit deneyleri.

## Bulgular
- 3-qubit deneylerde Avrupa call opsiyonu fiyatı %1 hata ile çıkıyor.
- Asya opsiyonu için path-summing devresi geometric average ile kodlanıyor.
- Bariyer opsiyonu hit/no-hit indikatörü ek kubitle.
- Donanım gürültüsü altında IQAE error mitigation gerekiyor.

## Etkisi
Kuantum-finans literatürünün ilk uçtan uca pratik referansı. Herman 2026 bu çalışmayı Black-Scholes-ötesi modellere genişletme motivasyonu olarak sunar.

## İlgili Kavramlar
- [[qae]]
- [[qmci]]
- [[kuantum-turev-fiyatlama]]
- [[geometric-brownian-motion]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Black-Scholes baseline ve Asya opsiyon yapısı
- [Seminer](../../projects/ders/2026-bahar-seminer/) — uygulanmış kuantum-finans örneği
