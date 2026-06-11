---
baslik: "Quantum Eigenvalue Transformation (QET / QSVT)"
slug: "qet"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, lineer-cebir, algoritma]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Quantum Eigenvalue Transformation (QET / QSVT)

## Özü
Bir bloğa-kodlanmış (block-encoded) operatör $A$'nın özdeğerlerine veya tekil değerlerine polinom dönüşümü $p(A)$ uygulamayı sağlayan birleştirici kuantum algoritma çerçevesi (Gilyén 2018); HHL, Hamilton simülasyonu, amplitude amplification gibi algoritmaları tek prensip altında toplar.

## Tanım
$A$ matrisi $\|A\| \le 1$, $U$ unitarisi içinde "block-encoded" — yani $A = (\langle 0|^{\otimes a} \otimes I)\, U\, (|0\rangle^{\otimes a} \otimes I)$.

QSVT (Quantum Singular Value Transformation), $U$ ve $U^{-1}$'in alternasyonu artı tek-kubitli faz dönüşleriyle (faz açıları $\Phi = (\phi_1, \dots, \phi_d)$) yeni bir unitari oluşturur ve bunun bloğunda $p(A)$ ortaya çıkar:

$$
U_{\Phi}\quad \Rightarrow \quad \text{block contains } p^{(SV)}(A),
$$

burada $p$ derecesi $d$, parite kısıtlı bir polinom ($d$ tek ise tek fonksiyon, çift ise çift). Polinom yaklaşımıyla **herhangi bir düzgün fonksiyon** $f(A)$ elde edilebilir.

**Birleştirme gücü:**
- $f(x) = 1/x$ → HHL (lineer sistem çözümü)
- $f(x) = \cos(tx)$ → Hamilton simülasyonu
- $f(x) = \mathrm{sgn}(x)$ → amplitude amplification (Grover)
- Eşik fonksiyonu → projektörler, Markov zinciri yansıması

QSVT, kuantum algoritma tasarımının "lego seti" — özellikle Herman et al. 2026 makalesinde [[fast-forwardability]] için kullanılır.

## Ana Bağlamlar
- [[gilyen-2018]] — kurucu makale
- [[hhl-2009]] — özel hâli
- [[grover-1996]] — başka özel hâli
- [[fast-forwardability]] — QSVT-tabanlı uygulama
- [[qae]] — amplitude amplification ile bağlantı

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al.'in arka plan teorisi (Bölüm 3-4)

## Kaynak
[[gilyen-2018]], [[herman-2026]]
