---
baslik: "Düşük-Rütbeli Eigendecomposition"
slug: "eigendecomposition-dusuk-rutbeli"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [lineer-cebir, eigendecomposition, boyut-dusurme, fpa]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Düşük-Rütbeli Eigendecomposition

## Özü
Bir simetrik matrisin (örn. $C_t$, $\Sigma$) yalnızca en büyük birkaç eigenvalue/eigenvektör çiftiyle yaklaşılması — finansal kovaryans ve Hurst-eşleme matrislerinde standart boyut düşürme tekniği.

## Tanım
$C_t \in \mathbb{R}^{N \times N}$ simetrik matrisi $C_t = U \Lambda U^T = \sum_{i=1}^N \lambda_i u_i u_i^T$ olarak ayrıştırılır. Finansal verilerde tipik bulgu: ilk birkaç eigenvalue (örn. 3-5) toplam varyansın %70-90'ını açıklar — kalan eigenvalues gürültüye yakındır. Düşük-rütbeli yaklaşım $C_t \approx U_k \Lambda_k U_k^T$ ($k \ll N$) hem hesap maliyetini hem de aşırı-uyumu (overfitting) azaltır. Marchenko-Pastur teoremi, sonlu örneklemde hangi eigenvalues'un "sinyal" hangilerinin "gürültü" olduğunu istatistiksel olarak ayırt etmeye olanak tanır. FPA'da bu yapı [[portfoy-hurst-kuadratik-form]]'un $C_t$ matrisi için kullanılır; ilk eigenvektör genelde "piyasa modu", ikinci ve üçüncü ise sektörel/stil faktörleridir. [[subspace-stability]] analizi bu ayrıştırma üzerine kurulur.

## Formül
$$
C_t = \sum_{i=1}^{N} \lambda_i u_i u_i^T, \quad \lambda_1 \ge \lambda_2 \ge \dots \ge \lambda_N
$$
Düşük-rütbeli yaklaşım:
$$
C_t \approx C_t^{(k)} = \sum_{i=1}^{k} \lambda_i u_i u_i^T
$$
Marchenko-Pastur sınırı (gürültü kümesi): $\lambda_{\pm} = \sigma^2 (1 \pm \sqrt{N/T})^2$.

## Ana Bağlamlar
- [[portfoy-hurst-kuadratik-form]] $C_t$ ayrıştırılan matris
- [[subspace-stability]] eigenvektör kayması ölçümü
- [[kovaryans-matrisi]] benzer yapı, klasik durumda
- [[markowitz-paralelligi]] ortak araç

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — $C_t$ analizinin teknik omurgası
- [Tauron](../../projects/tauron/) — multifraktal-genelleştirilmiş kovaryans yapılarının düşük-rütbeli yaklaşımı
- [Seminer](../../projects/) — "az sayıda faktör çoğu varyansı açıklar" görseli

## Kaynak
[[aygoren-uyar-2023]]
