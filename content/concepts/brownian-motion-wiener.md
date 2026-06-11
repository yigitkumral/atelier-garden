---
baslik: "Brown Hareketi (Wiener Süreci)"
slug: "brownian-motion-wiener"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [stokastik-surec, matematiksel-finans]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Brown Hareketi (Wiener Süreci)

## Özü
Sürekli yörüngeli, bağımsız ve normal dağılımlı artımları olan, hiçbir noktada türevlenemeyen kanonik stokastik süreçtir.

## Tanım
Wiener süreci $W_t$, $W_0 = 0$ ile başlayan, neredeyse her yerde sürekli ama hiçbir yerde diferansiyellenebilir olmayan bir Markov sürecidir. Ayrık olmayan zaman aralıklarındaki artımları bağımsızdır ve $W_t - W_s \sim \mathcal{N}(0, t-s)$ kuralına uyar. Sürecin kuadratik varyasyonu $t$'ye eşittir; bu, [[ito-calculus]]'un ünlü $(dW_t)^2 = dt$ kuralının kaynağıdır. Modern matematiksel finansta tüm difüzyon-tabanlı modellerin sürücü gürültüsüdür.

## Formül
$$
W_t - W_s \sim \mathcal{N}(0, t-s), \quad 0 \le s < t
$$
Kuadratik varyasyon:
$$
\langle W \rangle_t = t
$$

## Ana Bağlamlar
- [[ito-calculus]] — türevsizlikten doğan stokastik kalkülüsün temeli
- [[geometric-brownian-motion]] — finansa adapte edilmiş çarpımsal versiyon
- [[drift]] — Wiener bileşeniyle kombine edilen deterministik bileşen
- [[levy-area]] — çoklu Wiener bileşenlerinin etkileşimi

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — stokastik finansın temel taşı
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — diskretizasyon ve kuantum simülasyonun başlangıç noktası

## Kaynak
[[hull-2008]]
