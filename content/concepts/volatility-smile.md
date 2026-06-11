---
baslik: "Volatilite Gülümsemesi"
slug: "volatility-smile"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, opsiyon-fiyatlama, ampirik]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Volatilite Gülümsemesi

## Özü
Aynı vade için farklı kullanım fiyatlarında piyasa-implied volatilitelerinin sabit kalmayıp eğik veya simetrik bir desen oluşturmasıdır.

## Tanım
[[black-scholes]] modeli sabit volatilite varsayar; ancak gerçek piyasalarda Black-Scholes formülünü tersine çevirip her opsiyon için "implied volatility" hesaplandığında, bu değerler kullanım fiyatına göre değişir. Hisse senedi opsiyonlarında genellikle düşük strike'larda (out-of-the-money put) yüksek implied vol görülür ve eğri "smirk" şeklinde solak olur; bunun ardındaki ekonomik mekanizma [[leverage-effect]] ve fiyat dağılımının sol kuyruğunun şişkinliğidir. [[heston-stokastik-volatilite]] gibi stokastik volatilite modelleri bu deseni doğal olarak üretir.

## Formül
$\sigma_{\text{imp}}(K, T)$ — Black-Scholes formülünü piyasa fiyatına eşitleyen volatilite:
$$
C^{\text{piyasa}} = C^{\text{BS}}(S_0, K, T, r, \sigma_{\text{imp}}(K,T))
$$

## Ana Bağlamlar
- [[black-scholes]] — gülümsemenin "yokluğunu" varsayan modelin sapması
- [[heston-stokastik-volatilite]] — gülümsemeyi üreten model
- [[leverage-effect]] — eğikliğin ekonomik nedeni
- [[fat-tailed-dagilim]] — kuyruk olasılıkları gülümsemeye yansır

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — modeller arası karşılaştırma için ampirik kontrol
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kalibrasyon hedefi olarak sıkça kullanılır

## Kaynak
[[hull-2008]], [[heston-1993]]
