---
baslik: "ABCD Parametreleri"
slug: "abcd-parametreleri"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, portfoy, optimizasyon, kapali-form]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# ABCD Parametreleri

## Özü
Markowitz probleminin Lagrange çözümünden çıkan ve [[etkin-sinir]] hiperbolünü tek bir kapalı form ifadeyle parametreleyen dört skaler değişkendir.

## Tanım
$\mu$ getiri vektörü, $\Sigma$ kovaryans matrisi ve $\mathbf{1}$ birler vektörü verildiğinde tanımlanan $A$, $B$, $C$ skalerleri ile bunların kombinasyonu $D = AC - B^2$, etkin sınırın geometrisini, [[minimum-varyans-portfoyu]]'nun yerini ve [[tangent-portfoy]]'un parametrelerini hesaplamaya yeterlidir. Bu nedenle pratikte tek bir matris tersi $\Sigma^{-1}$ alındıktan sonra $A$, $B$, $C$ skalerleri tek geçişte hesaplanır ve tüm sınır türetilir. ABCD parametreleştirmesi, Markowitz probleminin sayısal yapısını dört skalere indirgediği için iskelet rolü üstlenir.

## Formül
$$
A = \mu^T \Sigma^{-1} \mu, \quad B = \mu^T \Sigma^{-1} \mathbf{1}, \quad C = \mathbf{1}^T \Sigma^{-1} \mathbf{1}, \quad D = AC - B^2
$$
Etkin sınır:
$$
\sigma_p^2 = \frac{C \mu_p^2 - 2 B \mu_p + A}{D}
$$
MVP varyansı $1/C$, MVP getirisi $B/C$.

## Ana Bağlamlar
- [[markowitz-portfoy-teorisi]] kapalı çözümün omurgası
- [[etkin-sinir]] geometrisini tam tanımlar
- [[minimum-varyans-portfoyu]] $w = \Sigma^{-1}\mathbf{1}/C$
- [[kovaryans-matrisi]] tersinin alınması ön şart

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — 11 portföyün hesabı doğrudan A, B, C, D kullanılarak yapılır
- [Tauron](../../projects/tauron/) — multifraktal modelde $\Sigma$ yerine düzeltilmiş kovaryans konularak ABCD yeniden hesaplanır
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — kuadratik form $w^T C_t w$'nin $A,B,C$ analoglarına çevrimi

## Kaynak
[[markowitz-1952]]
