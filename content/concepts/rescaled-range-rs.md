---
baslik: "Rescaled Range (R/S) Analizi"
slug: "rescaled-range-rs"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [hurst, fraktal, tahmin, klasik]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Rescaled Range (R/S) Analizi

## Özü
[[hurst-exponent]] tahmininin klasik (1951'de Hurst tarafından önerilen) yöntemi: kümülatif sapma aralığının standart sapmaya oranının zaman penceresi ile ölçeklenmesinden $H$ okunur.

## Tanım
$X_1, X_2, \dots, X_N$ bir zaman serisi ve $\bar{X}$ örneklem ortalaması olsun. Her pencere uzunluğu $\tau$ için: (1) ortalama-merkezli kümülatif toplam $Y_k = \sum_{i=1}^{k}(X_i - \bar{X})$ hesaplanır, (2) aralık $R(\tau) = \max_k Y_k - \min_k Y_k$ alınır, (3) standart sapma $S(\tau)$ hesaplanır, (4) oran $R/S$ formüle edilir. Beklenti $\mathbb{E}[R/S] \sim \tau^H$ olduğundan, $\log(R/S)$ vs $\log \tau$ regresyonunun eğimi $H$'yi verir. Yöntem basit ve sezgisel olmasına rağmen kısa-vadeli korelasyonlardan ve gürültüden ciddi bias'a sahiptir; bu yüzden modern alternatifler (DFA, MFDFA, [[m-q-tau-momentleri]] yapı fonksiyonu) tercih edilir. Yine de finansal literatürde tarihsel referans rolünü korur.

## Formül
$$
R(\tau) = \max_{1 \le k \le \tau} Y_k - \min_{1 \le k \le \tau} Y_k
$$
$$
S(\tau) = \sqrt{\frac{1}{\tau} \sum_{i=1}^{\tau} (X_i - \bar{X})^2}
$$
$$
\mathbb{E}[R/S](\tau) \sim \tau^H \implies H = \text{slope}\big( \log \mathbb{E}[R/S] \text{ vs } \log \tau \big)
$$

## Ana Bağlamlar
- [[hurst-exponent]] doğrudan tahmin hedefi
- [[m-q-tau-momentleri]] modern multifraktal alternatif
- [[estimator-gurultusu-bias-variance]] bias kaynakları
- [[fraktal-piyasa-hipotezi-fmh]] tarihsel uygulama bağlamı

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — baseline tahminci olarak rapor edilir; modern yöntemlerle karşılaştırma yapılır
- [Tauron](../../projects/tauron/) — $\zeta_q$'nun özel hâli ($q=1$ benzeri) olarak referans değer
- [Seminer](../../projects/) — Hurst kavramının tarihsel girişinde anlatılır

## Kaynak
[[hurst-1951]], [[mandelbrot-hudson]]
