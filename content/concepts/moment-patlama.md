---
baslik: "Moment Patlaması"
slug: "moment-patlama"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [olasilik, stokastik-volatilite, ileri-konu]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Moment Patlaması

## Özü
Bir stokastik sürecin yeterince yüksek dereceli momentinin sonlu olamayıp belli bir vadeden sonra ıraksamasıdır.

## Tanım
[[heston-stokastik-volatilite]] ve diğer pozitif-volatilite modellerinde, log-fiyatın moment üreten fonksiyonu yalnızca belli bir kritik vadeye kadar tüm dereceler için sonlu kalır; bu vadeden sonra üst-eşik momentler sonsuz olur. Andersen ve Piterbarg (2007), Heston için kritik momentin kapalı-form karakterizasyonunu vermiştir. Pratik sonuç: ağır kuyruklu opsiyon (örn. variance swap, derinden out-of-the-money) fiyatlamalarında naif Monte Carlo varyansı sonsuz olabilir; bu durum [[mlmc]] ve özel kontrol-değişken teknikleriyle yönetilir. Patlama, [[volatility-smile]]'in kuyruk asimptotiği üzerinde de doğrudan etkilidir.

## Formül
Heston'da kritik moment $\bar{u}(T)$:
$$
\mathbb{E}[S_T^u] < \infty \iff u \le \bar{u}(T)
$$
Eşik aşıldığında moment sonsuza ıraksar.

## Ana Bağlamlar
- [[heston-stokastik-volatilite]] — patlamanın incelendiği baz model
- [[vol-of-vol]] — yüksek değerleri eşiği daraltır
- [[volatility-smile]] — kuyruk asimptotiği patlamayla ilişkili
- [[fat-tailed-dagilim]] — patlamanın istatistiksel imzası

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — stokastik vol modellerinin matematiksel sınırı
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum hız vaadinin kontrol edileceği patolojik rejim

## Kaynak
[[andersen-piterbarg-2007]], [[heston-1993]]
