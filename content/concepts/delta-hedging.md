---
baslik: "Delta Hedging"
slug: "delta-hedging"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, risk-yonetimi, hedge]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Delta Hedging

## Özü
Bir opsiyon pozisyonunu, Delta katsayısı kadar dayanak varlık ters yönlü tutarak yön (fiyat) riskinden anlık olarak nötralleştirme stratejisidir.

## Tanım
Bir call satıcısı, Delta birimi kadar dayanak hisse alıp short opsiyon ile birleştirirse oluşan portföyün ilk derecede fiyat hareketine duyarsız olduğu gösterilebilir. [[black-scholes]] türetiminde tam da bu hedge edilmiş portföyün risksiz faizden büyümesi gerekliliği PDE'yi doğurur. Ancak Delta, fiyat değiştikçe değiştiğinden ([[greeks]] içinde Gamma) sürekli yeniden dengeleme gerekir; ayrık zaman, işlem maliyetleri ve sabit-volatilite varsayımının ihlali Delta hedging'in pratik etkinliğini sınırlar. [[heston-stokastik-volatilite]] altında volatilite riski de kalır ve Vega-hedge eklenir.

## Formül
Hedge portföy değeri:
$$
\Pi_t = V_t - \Delta_t S_t, \quad d\Pi_t = \left(\frac{\partial V}{\partial t} + \frac{1}{2}\sigma^2 S_t^2 \frac{\partial^2 V}{\partial S^2}\right) dt
$$
Birinci dereceden $S$ duyarlılığı sıfırlanır; risksizlik koşulu $d\Pi_t = r\Pi_t\, dt$.

## Ana Bağlamlar
- [[greeks]] — Delta katsayısının kaynağı
- [[black-scholes]] — türetiminin merkez fikri
- [[geometric-brownian-motion]] — hedge'in doğru çalıştığı süreç
- [[ito-calculus]] — hedge portföy diferansiyelinin türetilmesi

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — risk-nötr fiyatlama hikayesinin omurgası
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum Delta tahminlerinin operasyonel testi

## Kaynak
[[black-scholes-1973]], [[hull-2008]]
