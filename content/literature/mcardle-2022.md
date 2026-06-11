---
baslik: "Arithmetic-Free Quantum Distribution Loading"
slug: "mcardle-2022"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, dağılım-yükleme, qmci]
citekey: mcardle2022
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# McArdle et al. 2022 — Arithmetic-Free Quantum Distribution Loading

## Künye
Sam McArdle, András Gilyén, Mario Berta, "A streamlined quantum algorithm for topological data analysis with exponentially fewer qubits", + ilgili çizgide *Quantum Algorithms for Distribution Loading*, ~2022. (Atıf çatısı: Herman et al. 2026'nın "P-loader" tartışması.)

## Ana Argüman
[[qmci]]'da en pahalı bileşenlerden biri olan dağılım yükleme ($|0\rangle \to \sum_x \sqrt{p(x)}|x\rangle$) klasik aritmetik devreler yerine **doğrudan polinom-yaklaşımı** ile yapıldığında devre derinliği önemli ölçüde azalır.

## Yöntem
- Hedef yoğunluk $p(x)$ Chebyshev veya Fourier polinomuyla yaklaşıkla.
- [[qet]] (QSVT) ile bu polinomu blok-kodlanmış konum operatörüne uygula.
- Sonuç: $\sqrt{p(x)}$ genlikleri doğrudan yüklenir; ara aritmetik devrelere gerek yok.

Alternatif: Grover-Rudolph (2002) integral-yaklaşım yöntemi — ama exponential maliyet, log-concave dağılımlar için.

## Bulgular
- Log-normal, Heston marjinal, CIR non-central chi-squared yoğunlukları için $\mathcal{O}(\text{poly}\log(1/\varepsilon))$ derinlik.
- Aritmetik içermeme (no addition/multiplication subroutines) NISQ-yakın donanımda büyük tasarruf.
- QMCI hızlanmasının "yutulmamasını" sağlayan kritik bileşen.

## Etkisi
Herman 2026'nın türev fiyatlama hızlanmasının pratik korunabilirliği için zorunlu; aksi hâlde [[qae]]'nin quadratic kazancı yükleme adımının exponential maliyetinde kaybolur.

## İlgili Kavramlar
- [[qmci]]
- [[qet]]
- [[fast-forwardability]]

## Atıf Yapan Projeler
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al.'in P-loader argümanı
