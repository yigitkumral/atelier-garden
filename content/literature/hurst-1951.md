---
baslik: "Hurst (1951) — Long-Term Storage Capacity of Reservoirs"
slug: "hurst-1951"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [literature, hurst, klasik, hidroloji]
yazarlar: ["Hurst, Harold Edwin"]
yil: 1951
turu: makale
citekey: hurst1951
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Hurst (1951) — Long-Term Storage Capacity of Reservoirs

## Künye
Hurst, H. E. (1951). *Long-term storage capacity of reservoirs*. Transactions of the American Society of Civil Engineers, 116, 770-808. [[hurst-exponent]] kavramının doğum belgesi; finansal değil, hidrolojik kaynaklı.

## Ana Argüman
Nil nehrinin yıllık taşkın seviyeleri üzerinde Hurst, baraj kapasitesi tasarımı için gerekli depolama hacmini analiz ederken, gözlemlenen aralık/standart sapma oranının ($R/S$) zaman penceresi $\tau$ ile $\tau^{1/2}$'den daha hızlı büyüdüğünü fark etti. Klasik bağımsız-Gaussian varsayımı $\tau^{1/2}$ ölçeklenmesini öngörürken, Nil verisi $\tau^{0.7}$ civarı bir üs verdi. Bu, doğal süreçlerde **uzun-vadeli pozitif bağımlılığın** ilk ve en iyi belgelenmiş kantitatif kanıtıydı.

## Yöntem
[[rescaled-range-rs]] yöntemi: kümülatif sapma aralığı $R(\tau)$ ile standart sapma $S(\tau)$ oranlanır, ardından $\log(R/S)$ vs $\log \tau$ regresyonunun eğimi $H$ olarak alınır. Hurst, çeşitli doğal serilerde (nehir akışları, ağaç halkaları, sediment kalınlıkları) bu yöntemi sistematik olarak uyguladı.

## Bulgular
- Nil nehri için $H \approx 0.7$ (anlamlı şekilde 0.5'in üstünde)
- 75 farklı doğal seride ortalama $H \approx 0.73$; Brownian beklenen 0.5 değil
- Doğal süreçlerin "hatırladığı" — sıcak yıllar sıcak yılları, kurak dönemler kurak dönemleri takip ediyor
- Bu, daha sonra Mandelbrot tarafından "Joseph etkisi" (Yusuf Peygamber'in 7 bolluk + 7 kıtlık yılı kıssasına atıfla) olarak adlandırıldı

## Etkisi
- 1960'larda Mandelbrot tarafından finansa taşındı (fractional Brownian motion teorisi)
- Edgar Peters'ın [[fraktal-piyasa-hipotezi-fmh]] çalışmasının ampirik temellerinden
- Modern multifraktal analizde özel nokta ($H = \zeta_2 / 2$) olarak hâlâ merkezi
- "Hurst exponent" terminolojisi yazarın adını taşıyor, finansal istatistik standardı

## İlgili Kavramlar
- [[hurst-exponent]] — doğrudan tanım
- [[rescaled-range-rs]] — yöntem
- [[zeta-q-olcekleme]] — modern genelleştirme
- [[fraktal-piyasa-hipotezi-fmh]] — finans uygulaması

## Atıf Yapan Projeler
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — temel parametre kaynağı
- [Tauron](../../projects/tauron/) — multifraktal $\lambda$'nın klasik öncülü
- [Seminer](../../projects/) — Hurst kavramının tarihsel girişi
