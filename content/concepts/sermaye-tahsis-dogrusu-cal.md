---
baslik: "Sermaye Tahsis Doğrusu (CAL)"
slug: "sermaye-tahsis-dogrusu-cal"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, portfoy, cal, risk-free]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Sermaye Tahsis Doğrusu (CAL)

## Özü
Risk-free varlık ile [[tangent-portfoy]]'un doğrusal kombinasyonlarını $\mu$-$\sigma$ düzleminde gösteren, eğimi maksimum [[sharpe-orani]]'na eşit olan doğrudur.

## Tanım
Capital Allocation Line (CAL), $r_f$'den başlayıp tangent portföye ulaşan ve onun ötesinde (kaldıraçlı) uzayan düz bir çizgidir. Riskli varlıklar arasında [[etkin-sinir]] eğri iken, [[risk-free-varlik]] erişilebildiğinde etkin küme bu eğriden CAL doğrusuna yükselir; çünkü her riskli portföy noktasından geçen bir doğru, sınıra teğet olandan daha düşük Sharpe oranı verir. CAL'in özel hâli, riskli varlık olarak pazar portföyü alındığında elde edilen Capital Market Line (CML) kavramıdır.

## Formül
$$
\mu_p = r_f + \frac{\mu_T - r_f}{\sigma_T} \, \sigma_p
$$
Doğrunun eğimi tangent portföyün Sharpe oranıdır:
$$
S_T = \frac{\mu_T - r_f}{\sigma_T}
$$

## Ana Bağlamlar
- [[tangent-portfoy]] doğrunun temas noktasıdır
- [[risk-free-varlik]] başlangıç noktasıdır ($\sigma=0$)
- [[sharpe-orani]] doğrunun eğimidir
- [[etkin-sinir]] CAL'in geçtiği eğridir

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — risk-free dahil 11 portföyden biri CAL üzerinde lokalize edilir
- [Tauron](../../projects/tauron/) — multifraktal Sharpe altında CAL eğiminin değişimi
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — fraktal düzeltilmiş CAL referansı

## Kaynak
[[markowitz-1952]]
