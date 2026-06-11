---
baslik: "Newton-Raphson Yöntemi"
slug: "newton-raphson-yontemi"
olusturuldu: 2026-05-11
guncellendi: 2026-05-11
etiketler: [numerik, optimizasyon, implied-volatility, sayisal-yontem]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Newton-Raphson Yöntemi

## Özü
Türevlenebilir bir fonksiyonun sıfırını (kökünü) iteratif olarak bulan, kuadratik yakınsayan sayısal yöntemdir. Finansta Black-Scholes formülünden implied volatility çıkarımının standart aracıdır.

## Tanım
Sürekli türevlenebilir $f(x)$ fonksiyonunun $f(x) = 0$ denklemini çözmek için, başlangıç tahmini $x_0$'dan itibaren ardışık yaklaşımlar:

$$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$$

Geometrik anlamı: $(x_n, f(x_n))$ noktasından çizilen teğet doğrunun x-eksenini kestiği nokta bir sonraki iterasyondur. İterasyon kök yakınında ikinci dereceden yakınsar — her adımda hata yaklaşık olarak karesine düşer.

## Yakınsama ve Tuzakları
- **Kuadratik yakınsama:** $|x_{n+1} - x^*| \leq C \cdot |x_n - x^*|^2$ (kök yakınında)
- **Durdurma kriteri:** $|x_{n+1} - x_n| < \epsilon$ veya $|f(x_n)| < \epsilon$
- **Risk 1:** $f'(x_n) \to 0$ olursa iterasyon patlar (yatay teğet)
- **Risk 2:** Kötü başlangıç tahmini yakınsamayı kaçırabilir, döngüye düşebilir
- **Avantaj:** İyi başlangıç + düzgün $f$ ile çok az iterasyonda yüksek doğruluk

## Finansta Uygulanması — Implied Volatility
Black-Scholes opsiyon fiyatı $C_{BS}(\sigma)$ volatiliteye göre monoton arttığı (vega > 0) için tek bir köke yakınsar. Piyasa fiyatı $C_{piyasa}$ verildiğinde:

$$\sigma_{n+1} = \sigma_n - \frac{C_{BS}(\sigma_n) - C_{piyasa}}{\nu(\sigma_n)}$$

Burada $\nu = \partial C / \partial \sigma$ vega'dır (bkz. [[greeks]]). Başlangıç tahmini genellikle $\sigma_0 = 0.2$ (yıllık %20) alınır; tipik olarak 3-5 iterasyonda yakınsar.

## Ana Bağlamlar
- [[black-scholes]] — implied volatility çözümünün ana motoru
- [[greeks]] — vega ile türev hesabı
- [[monte-carlo-entegrasyonu]] — alternatif sayısal yaklaşım (köke gitmek yerine integral)
- [[euler-maruyama]] — başka bir numerik yöntem (SDE çözümü için)

## Projelerde Kullanım
- [Seminer 2026 Bahar](../../projects/ders/2026-bahar-seminer/) — Black-Scholes sunumunda implied volatility çıkarım yöntemi olarak kısa atıf. Hakan Hoca: "Detayına girme, sayısal yöntemin tanımını ver, geç."
