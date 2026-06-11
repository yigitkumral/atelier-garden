---
baslik: "Multifraktallık Şiddeti λ"
slug: "multifraktallik-siddeti-lambda"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, multifraktal, parametre, siddet]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Multifraktallık Şiddeti (λ)

## Özü
Multifraktallığı tek bir pozitif sayıyla özetleyen, parabolik fit'in eğriliğinden türetilen şiddet ölçüsü.

## Tanım
[[parabolik-fit-modeli]] çerçevesinde $\zeta_q = a q^2 + b q + c$ ifadesindeki $a$ katsayısı multifraktal eğriliği gösterir; ancak $a$ negatif ve ölçeği yorumlaması zor olduğundan literatürde standart hâle gelmiş özet $\lambda = \sqrt{-2a}$ kullanılır. $\lambda$ sıfıra yakın değer monofraktal limit, büyük $\lambda$ ise güçlü multifraktallık (geniş $f(\alpha)$ spektrumu, ağır volatilite kümeleri, fat tail) anlamına gelir. Bu skaler, [[multifraktal-spektrum]] genişliği $\Delta \alpha$ ile orantılıdır ve hem teorik (kaskade modelleri, log-normal multifraktal yürüyüş) hem ampirik (finansal seriler için tipik $\lambda \in [0.1, 0.4]$) bağlamlarda doğrudan yorumlanabilir.

## Formül
$$
\lambda = \sqrt{-2a}
$$
Spektrum genişliği ile ilişki (parabolik durum):
$$
\Delta \alpha \approx 2 \lambda \sqrt{q_{\max}^2 - q_{\min}^2}
$$
Tipik finansal değerler: $\lambda \in [0.1, 0.4]$ aralığında; $\lambda = 0$ saf Brownian.

## Ana Bağlamlar
- [[parabolik-fit-modeli]] kaynak parametre
- [[zeta-q-olcekleme]] altta yatan ölçek yapısı
- [[multifraktal-spektrum]] $\lambda$ ile genişler
- [[fraktal-duzeltme-cezasi]] Tauron formülünde girdi

## Projelerde Kullanım
- [Tauron](../../projects/tauron/) — Markowitz hedef fonksiyonuna eklenen fraktal cezanın gücünü doğrudan $\lambda$ kalibre eder
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — varlık-bazlı multifraktallık şiddetinin portföy düzeyine yansıması incelenir
- [Seminer](../../projects/) — tek-sayı sunumda tercih edilen şiddet özeti

## Kaynak
[[sornette-multifractal]], [[bouchaud-volatility-clustering]]
