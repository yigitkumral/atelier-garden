---
baslik: "Greeks (Risk Duyarlılıkları)"
slug: "greeks"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, risk-yonetimi]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Greeks (Risk Duyarlılıkları)

## Özü
Bir opsiyon fiyatının dayanak fiyat, volatilite, zaman ve faiz gibi parametrelere göre kısmi türevlerine verilen kolektif isimdir.

## Tanım
Greeks, türev portföylerinin risk profilini ayrıştırmak ve hedge etmek için kullanılan diferansiyel duyarlılıklardır. **Delta** ($\Delta = \partial V/\partial S$) yön riski; **Gamma** ($\Gamma = \partial^2 V/\partial S^2$) Delta'nın değişimi; **Vega** ($\nu = \partial V/\partial \sigma$) volatilite duyarlılığı; **Theta** ($\Theta = \partial V/\partial t$) zaman aşınması; **Rho** ($\rho = \partial V/\partial r$) faiz duyarlılığıdır. [[black-scholes]] çerçevesinde tümü kapalı form alır; [[heston-stokastik-volatilite]] gibi modellerde sayısal türev veya pathwise/likelihood-ratio yöntemleri kullanılır. [[delta-hedging]] gibi dinamik stratejilerin operasyonel temelidir.

## Formül
Black-Scholes call için:
$$
\Delta = \Phi(d_1), \quad \Gamma = \frac{\phi(d_1)}{S_0 \sigma \sqrt{T}}, \quad \nu = S_0 \phi(d_1)\sqrt{T}
$$
$$
\Theta = -\frac{S_0 \phi(d_1)\sigma}{2\sqrt{T}} - rKe^{-rT}\Phi(d_2), \quad \rho = KT e^{-rT}\Phi(d_2)
$$

## Ana Bağlamlar
- [[black-scholes]] — Greeks'in kapalı-form türetildiği model
- [[delta-hedging]] — Delta'nın operasyonel kullanımı
- [[heston-stokastik-volatilite]] — sayısal Greeks gerektiren genişletme
- [[avrupa-opsiyonu]] — Greeks'in en saf hesaplandığı sözleşme

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — risk yönetimi pedagojisi
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum türev hesaplamasının hedef metriği

## Kaynak
[[black-scholes-1973]], [[hull-2008]]
