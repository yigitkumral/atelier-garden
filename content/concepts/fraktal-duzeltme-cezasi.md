---
baslik: "Fraktal Düzeltme Cezası"
slug: "fraktal-duzeltme-cezasi"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, multifraktal, optimizasyon, tauron]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Fraktal Düzeltme Cezası (Tauron)

## Özü
Klasik Markowitz hedef fonksiyonuna eklenen, multifraktal yapıyı ($\lambda, \zeta_q$) cezalandıran ek terim — Tauron'un ana matematiksel katkısı.

## Tanım
Klasik mean-variance optimizasyonu yalnızca $w^T \Sigma w$ kuadratik formunu kullanır; bu, Gaussian/lineer dünyada doğrudur. Ancak fiyatlar multifraktal ise yüksek-q momentler (yani fat tail riskler ve volatilite kümeleri) dahil edilmelidir. Fraktal düzeltme cezası, yüksek-q momentlerden gelen riski portföy ağırlıklarına bir ceza olarak yansıtır. En yaygın form, [[multifraktallik-siddeti-lambda]] ile orantılı bir ceza: $\lambda$ büyüdükçe (multifraktallık güçlüyse) optimizasyon daha az volatil ve daha düşük-konsantrasyon portföylere yönelir. Ceza terimi [[tau-tarama]] ile birlikte kullanıldığında ufka-bağımlı çözüm yüzeyi üretir. Tauron'un katkısı bu cezanın somut, kalibre edilebilir formunu önermek ve simülatörle sezgi inşa etmektir.

## Formül
Tauron objektifi (genel form):
$$
\min_w \;\; \tfrac{1}{2} w^T \Sigma(\tau) w \;+\; \kappa \cdot P_{\text{frac}}\big(w; \lambda(\tau), \zeta_q(\tau)\big)
$$
Önerilen bir form:
$$
P_{\text{frac}}(w) = \lambda(\tau) \cdot \sum_{i,j} w_i w_j \, \big| \zeta_2^{(i,j)}(\tau) - 2H_{i,j}(\tau) \big|
$$
$\kappa$ regularizasyon katsayısı (kullanıcı parametresi); $\lambda = 0$ limitinde klasik Markowitz'e geri çöker.

## Ana Bağlamlar
- [[markowitz-portfoy-teorisi]] genişletilen klasik temel
- [[multifraktallik-siddeti-lambda]] ana kalibrasyon parametresi
- [[zeta-q-olcekleme]] ceza yapısının ham girdisi
- [[tau-tarama]] ufka göre ceza değişimi
- [[markowitz-paralelligi]] biçimsel devamlılık

## Projelerde Kullanım
- [Tauron](../../projects/tauron/) — projenin ana matematiksel kalbi; simülatörde kullanıcı $\kappa$ ve $\lambda$ ile etkileşir
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — ceza terimi alternatif olarak değerlendirilen kuadratik form yapısıyla karşılaştırılır
- [Seminer](../../projects/) — Markowitz → fraktal Markowitz geçişinin kavramsal anlatımı

## Kaynak
[[sornette-multifractal]], [[aygoren-uyar-2023]]
