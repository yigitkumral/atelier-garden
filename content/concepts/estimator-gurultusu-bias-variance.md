---
baslik: "Tahminci Gürültüsü: Bias-Variance Analizi"
slug: "estimator-gurultusu-bias-variance"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [istatistik, bootstrap, tahmin, gurultu, fpa-bulgu]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Tahminci Gürültüsü ve Bias-Variance Analizi

## Özü
Hurst, $\zeta_q$ ve $C_t$ matrisleri gibi fraktal tahmincilerin sonlu örneklemde nasıl gürültülendiğinin sistematik incelenmesi; FPA'nın temel metodolojik bulgularından biri.

## Tanım
Fraktal tahminciler (örn. R/S Hurst, structure function $\zeta_q$, kuadratik form $C_t$) finansal serilerde tipik olarak yüksek varyansa ve yapısal bias'a sahiptir. Sebepler: (a) sonlu örneklem boyu — özellikle uzun-vadeli $\tau$'da örneklem azalır, (b) heteroskedastik volatilite, (c) fat-tailed dağılımlar momentlerin yakınsamasını yavaşlatır (bkz. [[fat-tailed-dagilim]]), (d) zaman-bağımlılık [[block-bootstrap]] gibi uyarlamalar gerektirir. FPA'da bootstrap ($B = 1000$ tipik) ile her tahmincinin örneklem dağılımı çıkarılır; sonuç: tahminlerin standart hatası tipik olarak nokta-tahminin %15-30'u kadar büyüklükte. Bu, in-sample fit'in bile geniş güven bantları taşıdığını gösterir; out-of-sample'da çöküş (bkz. [[out-of-sample-cokus]]) buna eklendiğinde, "noktasal $H_p$ tahminine güvenmek" pozisyonu kırılır.

## Formül
Bias-variance ayrışımı:
$$
\mathbb{E}\big[(\hat{\theta} - \theta)^2\big] = \underbrace{\big(\mathbb{E}[\hat{\theta}] - \theta\big)^2}_{\text{Bias}^2} + \underbrace{\text{Var}(\hat{\theta})}_{\text{Variance}}
$$
Bootstrap standart hata:
$$
\widehat{\text{SE}}(\hat{\theta}) = \sqrt{\frac{1}{B-1} \sum_{b=1}^{B} (\hat{\theta}^{(b)} - \bar{\hat{\theta}})^2}
$$

## Ana Bağlamlar
- [[block-bootstrap]] zaman-bağımlı resampling
- [[out-of-sample-cokus]] gürültünün operasyonel sonucu
- [[m-q-tau-momentleri]] tahmin edilen yapı
- [[fat-tailed-dagilim]] yakınsama yavaşlığı kaynağı

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — faz2'nin omurgası: her ana tahminci için bootstrap ile güven aralığı raporlanır
- [Tauron](../../projects/tauron/) — $\lambda$ ve $\zeta_q$ tahminlerinin güven aralıklarının kalibrasyonda kullanılması
- [Seminer](../../projects/) — "fraktal tahminciler hassas" mesajının teknik dayanağı

## Kaynak
[[aygoren-uyar-2023]]
