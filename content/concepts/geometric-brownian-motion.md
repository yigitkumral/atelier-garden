---
baslik: "Geometrik Brown Hareketi (GBM)"
slug: "geometric-brownian-motion"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, stokastik-surec, fiyat-modeli]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Geometrik Brown Hareketi (GBM)

## Özü
Hisse fiyatlarını sabit yüzde [[drift]] ve sabit yüzde volatilite ile modelleyen, log-normal dağılımlı klasik stokastik diferansiyel denklemdir.

## Tanım
GBM, fiyatın logaritmasının Brown hareketi izlediği bir süreçtir; bu sayede fiyat negatif değer alamaz ve oransal getiriler sabit dağılım parametreleriyle modellenir. Bir [[brownian-motion-wiener]] sürücüsü altında, küçük zaman aralığındaki yüzdesel değişim deterministik bir [[drift]] terimi ile orantılı rastgele bir bileşenin toplamıdır. Klasik [[black-scholes]] çerçevesinin temel varsayımıdır ve [[ito-calculus]] uygulanarak kapalı-form çözüme ulaşılır.

## Formül
$$
dS_t = \mu S_t \, dt + \sigma S_t \, dW_t
$$
Çözüm:
$$
S_t = S_0 \exp\!\left((\mu - \tfrac{1}{2}\sigma^2)t + \sigma W_t\right)
$$
$\mu$ büyüme oranı, $\sigma$ volatilite, $W_t$ standart Wiener sürecidir. $-\tfrac{1}{2}\sigma^2$ düzeltme terimi Itô lemmasından doğar.

## Ana Bağlamlar
- [[brownian-motion-wiener]] — sürücü gürültü kaynağı
- [[ito-calculus]] — kapalı-form çözüm aracı
- [[black-scholes]] — GBM varsayımı altında türetilen kapalı form
- [[heston-stokastik-volatilite]] — volatiliteyi sabit kabul etmeyen genişletme

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — klasik fiyat modeli
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum Monte Carlo'da örneklenen baseline süreci

## Kaynak
[[black-scholes-1973]], [[hull-2008]]
