---
baslik: "Heston (1993) — A Closed-Form Solution for Options with Stochastic Volatility"
slug: "heston-1993"
yazarlar: ["Steven L. Heston"]
yil: 1993
dergi: "Review of Financial Studies"
volume: 6
issue: 2
sayfalar: "327-343"
doi: "10.1093/rfs/6.2.327"
citekey: "heston1993"
etiketler: [finans, stokastik-volatilite, opsiyon-fiyatlama]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Heston (1993) — A Closed-Form Solution for Options with Stochastic Volatility

## Künye
Heston, S. L. (1993). A Closed-Form Solution for Options with Stochastic Volatility with Applications to Bond and Currency Options. *Review of Financial Studies*, 6(2), 327-343. https://doi.org/10.1093/rfs/6.2.327

## Ana Argüman
Volatiliteyi sabit kabul etmeyen, anlık varyansın CIR-tipi bir karekök süreciyle evriltildiği bir model çerçevesinde, Avrupa opsiyonları için karakteristik fonksiyon kapalı formda elde edilebilir; bu sayede [[volatility-smile]] gibi ampirik gözlemler analitik tractability'yi feda etmeden modellenebilir.

## Yöntem
Hisse log-fiyatı log-normal difüzyon, anlık varyans [[cir-modeli]] yapısında karekök-difüzyon olarak tanımlanır; iki Wiener sürücü arasında $\rho$ korelasyonu vardır. Risk-nötr ölçü altında karakteristik fonksiyon Riccati ODE çözümlerinden inşa edilir; opsiyon fiyatı ters Fourier integrali olarak ifade edilir. Geleneksel sayısal Fourier kuadratur veya FFT yöntemleriyle çok hızlı değerleme sağlanır.

## Bulgular
Volatilite mean-reversion'u, [[vol-of-vol]] ve [[leverage-effect]] korelasyonu birlikte kalibre edildiğinde piyasa-implied volatilite eğrisinin hem eğikliği hem de zaman-yapısı oldukça iyi yakalanabilmektedir. Aynı çerçeve tahvil ve döviz opsiyonlarına da genişletilebilir.

## Etkisi
Stokastik volatilite literatürünün sektörel standardı haline gelen Heston modeli, türev masalarının kalibrasyon altyapısının çekirdeğidir. Sonraki SLV (stochastic-local volatility) ve rough volatility çalışmaları bu çerçeveyi referans alır; kuantum türev fiyatlama makalelerinin de testbed'idir.

## İlgili Kavramlar
- [[heston-stokastik-volatilite]]
- [[cir-modeli]]
- [[volatility-smile]]
- [[leverage-effect]]
- [[karakteristik-fonksiyon]]

## Atıf yapan projeler
- [Seminer](../../projects/ders/2026-bahar-seminer/)
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/)
