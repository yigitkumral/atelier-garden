---
baslik: "Quantum Amplitude Amplification and Estimation"
slug: "brassard-2002"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, qae, hizlanma]
citekey: brassard2002
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Brassard et al. 2002 — Quantum Amplitude Amplification and Estimation

## Künye
Gilles Brassard, Peter Høyer, Michele Mosca, Alain Tapp, "Quantum Amplitude Amplification and Estimation", *Contemporary Mathematics*, 305, 53–74, 2002. (arXiv:quant-ph/0005055)

## Ana Argüman
Grover arama algoritması, yapısız veritabanı arama özel hâlinden çıkarılarak **herhangi bir kuantum süreci** üstüne genelleştirilebilir; aynı şekilde işaretli genliğin değeri $\mathcal{O}(1/\varepsilon)$ kuantum sorgu maliyetiyle tahmin edilebilir.

## Yöntem
$\mathcal{A}|0\rangle = \sqrt{1-a}|\psi_0\rangle + \sqrt{a}|\psi_1\rangle$ devresi için:
- **Amplitude amplification:** $\mathcal{Q} = -\mathcal{A}S_0\mathcal{A}^{-1}S_\chi$ operatörü Grover iterasyonunu genelleştirir.
- **Amplitude estimation:** $\mathcal{Q}$ üzerine quantum phase estimation uygulanarak $a$'nın değeri bulunur.

Hata: $|\hat{a} - a| \le 2\pi\sqrt{a(1-a)}/M + \pi^2/M^2$ — $M$ Grover iterasyon sayısı.

## Bulgular
- **Quadratic speedup:** Klasik MC $\mathcal{O}(1/\varepsilon^2)$ → kuantum $\mathcal{O}(1/\varepsilon)$.
- Tanımlı genel oracle modeli sayesinde her olasılıksal hesaplama hızlandırılabilir.
- Sayma problemi (counting): işaretli öğe sayısı tahmini.

## Etkisi
Tüm modern kuantum-MC çatısının kurucu makalesi. [[montanaro-2015]] bu sonucu MC entegrasyonuna formal olarak uyarladı; [[stamatopoulos-2020]] ve [[herman-2026]] türev fiyatlamaya getirdi. Modern IQAE, MLQAE, QoPrime varyantları aynı temel iterasyonu paylaşır.

## İlgili Kavramlar
- [[qae]]
- [[qmci]]
- [[grover-1996]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — fiyatlamanın kuantum çekirdeği
- [Seminer](../../projects/ders/2026-bahar-seminer/) — hızlanma teorisi temeli
