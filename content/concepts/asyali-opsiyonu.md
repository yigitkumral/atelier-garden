---
baslik: "Asyalı Opsiyon"
slug: "asyali-opsiyonu"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, ekzotik-opsiyon, path-dependent]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Asyalı Opsiyon

## Özü
Payoff'u yörünge boyunca dayanak fiyatın ortalamasına bağlı olan path-dependent ekzotik opsiyon ailesidir.

## Tanım
Asyalı (Asian) opsiyonlar, vade payoff'unu nokta fiyat $S_T$ yerine $[0, T]$ aralığındaki ortalamaya endeksler; bu, manipülasyon riskini düşürür ve dayanak volatilitesini ortalama etkisiyle yumuşatır. Aritmetik ortalama varyantı için kapalı form yoktur — log-normal toplamlar kapanmaz — ve değerleme [[monte-carlo-entegrasyonu]] veya PDE yöntemleriyle yapılır; geometrik ortalama varyantı log-normalliği koruduğu için [[black-scholes]]-benzeri analitik formüle sahiptir. Yörünge bağımlılığı, [[greeks]]'in türetilmesini de zorlaştırır ve [[mlmc]] / [[qae]] gibi varyans-azaltma tekniklerinin doğal hedefidir.

## Formül
Aritmetik Asyalı call payoff (sürekli ortalama):
$$
h = \max\!\left(\frac{1}{T}\int_0^T S_t\, dt - K,\, 0\right)
$$
Geometrik Asyalı:
$$
h = \max\!\left(\exp\!\left(\frac{1}{T}\int_0^T \ln S_t\, dt\right) - K,\, 0\right)
$$

## Ana Bağlamlar
- [[payoff-fonksiyonu]] — yörünge bağımlı yapı
- [[avrupa-opsiyonu]] — path-independent karşıtı
- [[monte-carlo-entegrasyonu]] — aritmetik varyantın değerlemesi
- [[qae]] — kuantum hızlanmanın hedef ürünü

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — ekzotik opsiyonlara giriş
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Monte Carlo'da kuantum hızlanmanın gösterildiği ürün

## Kaynak
[[hull-2008]], [[glasserman-2003]]
