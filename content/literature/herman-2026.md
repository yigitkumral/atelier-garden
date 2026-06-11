---
baslik: "Quantum Speedups for Derivative Pricing Beyond Black-Scholes"
slug: "herman-2026"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, fiyatlama, ana-makale]
citekey: herman2026
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Herman et al. 2026 — Quantum Speedups for Derivative Pricing Beyond Black-Scholes (ANA MAKALE)

## Künye
Dylan Herman, Cody Googin, Xiaoyuan Liu, Alexey Galda, Ilya Safro, Yue Sun, Marco Pistoia, Yuri Alexeev, "Quantum Speedups for Derivative Pricing Beyond Black-Scholes", *arXiv:2602.03725*, 105 sayfa, 2026 (CC-BY 4.0). Çeviri çalışması: PAU-Claude / Quantum Computing projesi.

## Özet
Black-Scholes ötesi modellerin (Heston, SABR, Lévy süreçleri, jump-diffusion) kuantum bilgisayarda nasıl etkin biçimde simüle edileceğini ve quadratic hızlanmanın korunması için gereken teknik koşulları sistematik olarak inceleyen kapsamlı çalışma. Üç ana algoritmik araç birleştirilir: [[qae]] (Brassard 2002, Montanaro 2015), [[qet]]/QSVT (Gilyén 2018), ve [[fast-forwardability]] (yeni terminoloji).

## Ana Argüman
Pratik kuantum türev fiyatlama, sadece [[qae]] uygulamasından ibaret değildir; **dağılım yükleme**, **yörünge simülasyonu** ve **payoff aritmetiği** alt-rutinleri yeterince ucuz olmazsa quadratic kazanç yutulur. Makale, hangi finansal modeller için bu koşulların sağlandığını teorem-düzeyinde karakterize eder.

## Contributions (Ana Katkılar)
1. **Fast-forwardability formal tanımı:** Bir SDE'nin marjinal $X_T$ dağılımını $\mathcal{O}(\text{poly}\log T)$ kuantum maliyetiyle yükleme koşulu.
2. **Karakterizasyon:** Affine modeller (Heston, CIR), jump-diffusion ve Lévy süreçleri fast-forwardable; yol-bağımlı türevler için reparameterization gerekli.
3. **QSVT-tabanlı algoritmalar:** Karakteristik fonksiyondan yoğunluk türetip Chebyshev polinomları üzerinden yükleme.
4. **Resource estimation:** Heston Avrupa call için ~10^7 T-gate, ~5000 mantıksal kubit; Black-Scholes Asya için ~10^8 T-gate.
5. **Pratik eşik (threshold) analizi:** Klasik MC'yi gerçekten geçecek devre-derinliği rejimi.

## Yöntem
- Block-encoding teorisi + QSVT angle-finding (Wang-Dong-Lin 2022).
- Karakteristik fonksiyon yarı-analitik formülleri (Heston Riccati ODE çözümü, Carr-Madan FFT, Lewis formülü).
- [[mcardle-2022]] dağılım yükleme tekniğinin uyarlanması.
- Yol-bağımlı durum için [[chakrabarti-2021]] reparameterization birleştirilir.

## Key Results (Ana Sonuçlar)
- **Avrupa opsiyonu, fast-forwardable model:** Klasik $\mathcal{O}(\sigma^2/\varepsilon^2)$ → kuantum $\mathcal{O}(\sigma/\varepsilon)$ (saf quadratic).
- **Yol-bağımlı opsiyon (Asya, bariyer):** Reparameterization sonrası quadratic korunur, ancak pre-factor büyük.
- **Heston modeli:** [[broadie-kaya-2006]] exact simulation + QAE → en iyi pratik kuantum aday.
- **Jump-diffusion (Merton, Kou):** Lévy karakteristik fonksiyonu üstünden direkt yükleme.
- **Negatif sonuç:** Genel bir SDE'nin tam yörüngesini yüklemek (yapısız Euler/Milstein zinciri) kuantum hızlanmasını yutar.

## Etkisi
Bu makale, kuantum-finans literatüründe Stamatopoulos 2020'nin ardından gelen ikinci nesil pratiklik analizinin omurga referansı. PAU-Claude / Quantum Computing projesi:
- (a) Tam Türkçe çeviri (LaTeX pixel-perfect)
- (b) Türkçe yorum balonlarıyla yorumlu makale (reader-profile-aware)
- (c) Pedagojik Türkçe Eğitim Rehberi
biçiminde üç paralel iş kolu üretiyor.

## İlgili Kavramlar
- [[qae]]
- [[qmci]]
- [[qet]]
- [[fast-forwardability]]
- [[kuantum-turev-fiyatlama]]
- [[karakteristik-fonksiyon]]
- [[heston-stokastik-volatilite]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — projenin ana kaynağı (çeviri + yorum + rehber)
- [Seminer](../../projects/ders/2026-bahar-seminer/) — sunum ana referansı
