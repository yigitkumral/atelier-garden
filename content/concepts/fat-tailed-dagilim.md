---
baslik: "Fat-Tailed Dağılım"
slug: "fat-tailed-dagilim"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [dagilim, kuyruk, levy, mandelbrot]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Fat-Tailed (Kalın-Kuyruklu) Dağılım

## Özü
Aşırı (extreme) olayların Gauss dağılımının öngördüğünden çok daha yüksek olasılıkla gerçekleştiği, kuyruk olasılığı $P(|X| > x)$ üssel değil polinom-azalan dağılım sınıfı.

## Tanım
Klasik Black-Scholes ve Markowitz çerçeveleri Gauss varsayımına dayanır; bu varsayım finansal verilerde sürekli ihlal edilir. Mandelbrot'un 1963 makalesi pamuk fiyatları üzerinde gösterdi ki kuyruk olasılığı $P(|X| > x) \sim x^{-\alpha}$ formundadır ve $\alpha \in (1, 4)$ aralığındadır — Pareto-Lévy stable dağılım. $\alpha < 2$ ise varyans sonsuzdur; $\alpha < 1$ ise ortalama bile sonsuzdur. Ampirik olarak hisse senedi günlük getirileri için $\alpha \approx 3-4$ tipiktir (varyans sonlu, fakat dördüncü moment sonsuz veya çok büyük). Bu, Markowitz'in $w^T \Sigma w$ kullanımının ($\Sigma$ ikinci moment) marjinal olarak savunulabilir, fakat extreme risk ölçütlerinin (Value-at-Risk, Expected Shortfall) Gauss varsayımıyla ciddi şekilde eksik tahmin edileceği anlamına gelir. Multifraktal yapı (bkz. [[multifraktal-spektrum]]) fat-tail davranışının ölçek-bağımlı genelleştirilmesidir.

## Formül
Power-law kuyruk:
$$
P(|X| > x) \sim C \, x^{-\alpha}, \quad x \to \infty
$$
Lévy stable karakteristik fonksiyon:
$$
\varphi(t) = \exp\left(i \mu t - |\sigma t|^\alpha [1 - i \beta \, \text{sgn}(t) \tan(\pi \alpha / 2)]\right)
$$
$\alpha = 2$ → Gauss; $\alpha < 2$ → fat-tailed.

## Ana Bağlamlar
- [[fraktal-piyasa-hipotezi-fmh]] dağılımsal imza
- [[multifraktal-spektrum]] genelleştirme
- [[estimator-gurultusu-bias-variance]] yüksek momentlerin gürültüsü kaynağı
- [[volatility-smile]] Black-Scholes Gauss eksikliğinin opsiyon piyasası izi

## Projelerde Kullanım
- [Seminer](../../projects/) — "neden Gauss yetmez?" anlatımının ana grafiği (log-log kuyruk)
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — momentlerin yakınsamasındaki yavaşlığın açıklaması
- [Tauron](../../projects/tauron/) — fraktal cezanın yüksek-q momentleri dahil etmesinin motivasyonu

## Kaynak
[[mandelbrot-1963]], [[levy-1951]], [[mandelbrot-hudson]]
