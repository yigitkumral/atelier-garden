---
baslik: "Quantum Singular Value Transformation and Beyond"
slug: "gilyen-2018"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, qsvt, lineer-cebir]
citekey: gilyen2018
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Gilyén et al. 2018 — Quantum Singular Value Transformation

## Künye
András Gilyén, Yuan Su, Guang Hao Low, Nathan Wiebe, "Quantum Singular Value Transformation and Beyond: Exponential Improvements for Quantum Matrix Arithmetics", *Proceedings of STOC 2019*, 193–204, 2019. (arXiv:1806.01838, 2018)

## Ana Argüman
Block-encoded bir matrise polinom dönüşümleri uygulamayı tek bir genel çerçevede toplayan QSVT (Quantum Singular Value Transformation), HHL, Hamilton simülasyonu, amplitude amplification ve Grover gibi büyük algoritma ailelerini özel hâlleri olarak içeren birleştirici teori sunar.

## Yöntem
$U$ block-encodes $A$ ($\|A\| \le 1$). QSVT, $U$ ve $U^{-1}$'in alternasyonuyla faz açıları $\Phi = (\phi_1, \dots, \phi_d)$ kontrolünde:
$$
U_\Phi \quad \Rightarrow \quad \text{block contains } P^{(SV)}(A),
$$
parite-kısıtlı polinom $P$ derecesi $d$. Polinom yaklaşımıyla herhangi bir düzgün $f(A)$ uygulanabilir. Faz açıları ön-hesaplanır (Remez, Wang-Dong-Lin angle finder).

## Bulgular
- Hamilton simülasyonu: Jacobi-Anger ile $\cos(tA)$, $\sin(tA)$ polinom yaklaşımı → optimal sorgu karmaşıklığı.
- HHL: Chebyshev rasyonel yaklaşım $\sim 1/x$ → koşul sayısına optimal bağımlılık.
- Amplitude amplification: $\mathrm{sgn}$ yaklaşımı → Grover.
- Block-encoded Markov zinciri yansıması, projektörler.

## Etkisi
Kuantum algoritma tasarımının "lego seti". Herman 2026'nın [[fast-forwardability]] çerçevesinde SDE süreç simülasyonu ve karakteristik fonksiyon yüklemesi için doğrudan kullanılır.

## İlgili Kavramlar
- [[qet]]
- [[hhl-2009]]
- [[grover-1996]]
- [[fast-forwardability]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al. arka planı (Bölüm 3-4)
