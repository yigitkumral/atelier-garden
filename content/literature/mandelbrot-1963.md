---
baslik: "Mandelbrot (1963) — The Variation of Certain Speculative Prices"
slug: "mandelbrot-1963"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [literature, mandelbrot, klasik, fat-tail]
yazarlar: ["Mandelbrot, Benoit"]
yil: 1963
turu: makale
citekey: mandelbrot1963
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Mandelbrot (1963) — The Variation of Certain Speculative Prices

## Künye
Mandelbrot, B. (1963). *The variation of certain speculative prices*. The Journal of Business, 36(4), 394-419. Modern fraktal finans literatürünün başlangıç makalesi.

## Ana Argüman
Pamuk vadeli işlem fiyatları üzerinde Mandelbrot, günlük getirilerin dağılımının Gaussian olmadığını — kuyrukların çok daha kalın olduğunu ve dağılımın **Pareto-Lévy stable** ailesine ait olduğunu öne sürdü. Bu, Bachelier (1900)'un Brownian motion temelli fiyat modelinin ve dolayısıyla onun üzerine inşa edilecek Black-Scholes'in (1973) Gauss varsayımının ampirik olarak hatalı olduğunun ilk net iddiasıydı.

## Yöntem
- Pamuk fiyat serisinin (1816-1958, yaklaşık 142 yıl) günlük getirileri
- Logaritmik fiyat farklarının kuyruk dağılımının analizi: $P(|X| > x) \sim x^{-\alpha}$ Pareto-tipi azalmaya uyup uymadığı
- Kümülatif dağılım grafiklerinin log-log çizimi (lineer ise power-law)
- Karakteristik üs $\alpha$'nın tahmini

## Bulgular
- Pamuk fiyatları için $\alpha \approx 1.7$ — varyans **sonsuz** (çünkü $\alpha < 2$)
- Bu, Markowitz mean-variance çerçevesinin matematiksel olarak ill-defined olabileceğini ima eder (sonlu varyans şart)
- Lévy stable dağılımlar **ölçek-değişmez** (self-similar) — fraktal yapının olasılıksal versiyonu
- Daha sonra ampirik tartışma $\alpha$'nın 2'nin altında mı üstünde mi olduğu üzerine odaklandı; hisse senedi getirileri için bugünkü konsensüs $\alpha \approx 3-4$ (varyans sonlu, fakat dördüncü moment problemli)

## Etkisi
- Modern finansal matematik için **paradigma kıran** makale
- Black-Scholes ve Markowitz dünyasının matematiksel kalbinin (Gauss) sorgulanması
- Daha sonraki [[multifraktal-spektrum]] çalışmalarının (1972, 1997) tohumu
- Edgar Peters [[fraktal-piyasa-hipotezi-fmh]]'sinin önemli kavramsal motivatörü
- Bouchaud, Sornette gibi modern econophysics akımlarının kurucu metni

## İlgili Kavramlar
- [[fat-tailed-dagilim]] — doğrudan tanım
- [[levy-1951]] — alttaki olasılık teorisi
- [[fraktal-piyasa-hipotezi-fmh]] — kavramsal devamı
- [[volatility-smile]] — Black-Scholes'in Gauss yetersizliğinin opsiyon piyasası izi

## Atıf Yapan Projeler
- [Seminer](../../projects/) — "neden Gauss yetmez?" anlatımının kurucu kaynağı
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — teorik çerçeve referansı
- [Tauron](../../projects/tauron/) — fraktal cezanın ampirik motivasyonu
