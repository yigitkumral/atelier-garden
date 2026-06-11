---
baslik: "A Fast Quantum Mechanical Algorithm for Database Search"
slug: "grover-1996"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, algoritma, arama]
citekey: grover1996
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Grover 1996 — A Fast Quantum Mechanical Algorithm for Database Search

## Künye
Lov K. Grover, "A Fast Quantum Mechanical Algorithm for Database Search", *Proceedings of the 28th Annual ACM Symposium on Theory of Computing (STOC '96)*, 212–219, 1996.

## Ana Argüman
$N$ elemanlı yapısız bir veritabanında işaretli tek bir öğe için klasik arama $\mathcal{O}(N)$ sorgu gerektirirken, kuantum bilgisayar bunu $\mathcal{O}(\sqrt{N})$ sorguda çözer.

## Yöntem
Üniform süperpozisyon $|s\rangle = N^{-1/2}\sum_x |x\rangle$ üzerine iki yansımanın çarpımı uygulanır:
- $S_\chi = I - 2|\chi\rangle\langle\chi|$ — işaretli durum üstüne yansıma (oracle)
- $S_s = 2|s\rangle\langle s| - I$ — başlangıç süperpozisyonu üstüne yansıma

Bu iki yansımanın bileşkesi (Grover iterasyonu) Bloch küresinde işaretli yöne $\mathcal{O}(\sqrt{N})$ adımda taşır.

## Bulgular
- Speedup: quadratic, kanıtlanan optimal (Bennett-Bernstein-Brassard-Vazirani lower bound).
- Genelleştirme: amplitude amplification (Brassard 2002) ve QAE'nin doğrudan atası.

## Etkisi
Shor algoritmasıyla birlikte kuantum hesaplamanın iki temel taşı. Tüm [[qae]], [[qmci]], [[montanaro-2015]] çizgisi Grover'ın iterasyonuna dayanır. Türev fiyatlamada quadratic hızlanmanın matematiksel kaynağı budur.

## İlgili Kavramlar
- [[qae]]
- [[qmci]]
- [[qet]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — temel ata algoritma
- [Seminer](../../projects/ders/2026-bahar-seminer/) — kuantum giriş slaydı
