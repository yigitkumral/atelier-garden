---
baslik: "Sornette — Multifractal Returns ve Ekonofizik"
slug: "sornette-multifractal"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [literature, sornette, multifraktal, ekonofizik, tauron-temel]
yazarlar: ["Sornette, Didier"]
yil: 2003
turu: kitap-ve-makale-kumesi
citekey: sornette-multifractal
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Sornette — Multifractal Returns ve Ekonofizik

## Künye
Ana referans: Sornette, D. (2003). *Why Stock Markets Crash: Critical Events in Complex Financial Systems*. Princeton University Press. Tamamlayıcı: Sornette ve grubunun (Muzy, Bacry, Delour, Filimonov) 1990'lar-2000'ler boyunca ürettiği multifraktal yürüyüş (MMAR, MRW — Multifractal Random Walk) makaleleri. Tauron projesinin **ana matematiksel temel** kaynağı.

## Ana Argüman
Finansal getiriler yalnızca fat-tailed değil, aynı zamanda **multifraktaldir**: farklı zaman ölçeklerinde farklı düzensizlik (singularity) profilleri sergiler. Sornette'nin grubu, MRW (Multifractal Random Walk) modelini önererek, log-volatilitenin Gaussian fakat uzun-vadeli korelasyonlu bir süreç olarak modellenmesinin gözlemsel verileri çok iyi açıkladığını gösterdi. MRW modeli iki parametreyle ($\lambda^2$ multifraktallık şiddeti ve $T$ integral ölçek) tüm $\zeta_q$ eğrisini üretir.

## Yöntem
- Yapı fonksiyonu (structure function, [[m-q-tau-momentleri]]) hesaplaması
- $\zeta_q$ eğrisinin parabolik fit'i ile [[parabolik-fit-modeli]] parametrelendirmesi
- $\lambda^2$ ve integral ölçeğin tahmini için maksimum likelihood / GMM
- Kritik nokta (logaritmik-periyodik) yapıların kriz öncesi imzaları

## Bulgular
- Hisse indeksleri için tipik $\lambda^2 \in [0.02, 0.04]$ — yani $\lambda \in [0.14, 0.20]$ (bkz. [[multifraktallik-siddeti-lambda]])
- $\zeta_q$ eğrisi parabolik forma çok iyi uyuyor; Hurst $H = \zeta_2/2 \approx 0.5 - 0.55$ tipik
- MRW model simülasyonları gerçek verinin volatilite kümeleri, fat-tail, ölçek-değişmezlik özelliklerini yeniden üretiyor
- Kriz öncesi log-periyodik salınım imzası (1987, 2000, 2008 örneklerinde geriye dönük doğrulanmış)

## Etkisi
- Ekonofizik akımının kurucu metinlerinden
- Multifraktal finans literatürü için gold-standard model (MRW)
- Tauron projesinin matematiksel kalbi: fraktal düzeltme cezası tam olarak Sornette tarafından önerilen $(\lambda, \zeta_q)$ parametre çiftine kalibre edilir
- Operasyonel uygulamada hâlâ tartışmalı: model parametre tahmini gürültülü, out-of-sample tahmin gücü sınırlı

## İlgili Kavramlar
- [[multifraktal-spektrum]] — Sornette grubunun başlıca aracı
- [[zeta-q-olcekleme]] — temel ölçüm
- [[parabolik-fit-modeli]] — standart parametrelendirme
- [[multifraktallik-siddeti-lambda]] — özet skaler
- [[fraktal-duzeltme-cezasi]] — Tauron uygulaması

## Atıf Yapan Projeler
- [Tauron](../../projects/tauron/) — projenin matematiksel temeli
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — multifraktal genişletme tartışmasında referans
- [Seminer](../../projects/) — modern multifraktal yapı anlatımı
