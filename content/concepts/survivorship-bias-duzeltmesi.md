---
baslik: "Survivorship Bias Düzeltmesi"
slug: "survivorship-bias-duzeltmesi"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [veri-kalitesi, bias, backtest, fpa]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Survivorship Bias Düzeltmesi

## Özü
Yalnızca bugünkü işlem gören (hayatta kalmış) hisseleri kullanarak yapılan backtestin gerçeği abartılı olarak iyimser göstermesi sorununu, delisted (borsadan çıkmış) hisseleri dahil ederek düzeltme yaklaşımı.

## Tanım
Borsalardan zaman içinde iflas, satın alma, halka açıklığı sona erme gibi nedenlerle hisseler düşer. Eğer backtest yalnızca **bugün** işlem gören hisseleri kullanırsa, batan hisseler örneklemden silinmiştir; sonuç sistematik olarak yukarı saplı. Bu, akademik literatürde 200-400 baz puan/yıl performans abartısına yol açabildiği belirlenmiştir. Düzeltme: backtest tarihinde aktif olan tüm hisselerin tarihsel verisini kullanmak (CRSP, Compustat tarzı veritabanları). FPA pipeline'ında Borsa İstanbul / S&P 500 örnekleminde delisting tarihleri takip edilir; portföy bir hisseyi tutuyorsa ve hisse delist olursa pozisyon delisting tarihinde nakdi etkiye dönüştürülür ve yeniden dengeleme zamanına kadar bekletilir. Bu, backtest sonuçlarının dürüstlüğü için zorunlu bir adımdır.

## Formül
Düzeltilmiş getiri zinciri (delisting durumu):
$$
r_t^{(i)} = \begin{cases} (P_t^{(i)} - P_{t-1}^{(i)}) / P_{t-1}^{(i)} & \text{aktif ise} \\ -1 \cdot (1 - \text{recovery rate}) & \text{delisting günü} \\ 0 & \text{delisting sonrası} \end{cases}
$$
Düzeltme öncesi/sonrası Sharpe farkı tipik: $\Delta \text{SR} \approx 0.1 - 0.4$.

## Ana Bağlamlar
- [[rolling-backtest]] uygulama bağlamı
- [[out-of-sample-cokus]] gerçekçi değerlendirme
- [[markowitz-portfoy-teorisi]] backtest edilen klasik temel

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — veri katmanının zorunlu temizleme adımı
- [Tauron](../../projects/tauron/) — kalibrasyon verisinin de aynı düzeltmeyle hazırlanması gerekir
- [IMF527 Portföy](../../projects/ders/) — ödevde kullanılan tarihsel veri için de prensip aynıdır

## Kaynak
Standart finans literatürü (Brown, Goetzmann, Ross 1992); FPA pipeline rapor metni.
