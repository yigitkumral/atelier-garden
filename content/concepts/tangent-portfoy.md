---
baslik: "Tangent Portföy"
slug: "tangent-portfoy"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, portfoy, sharpe, cal]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Tangent Portföy

## Özü
Risk-free varlık mevcutken Sharpe oranını maksimize eden, [[etkin-sinir]]'e [[sermaye-tahsis-dogrusu-cal]] doğrusunun teğet olduğu noktadaki riskli portföydür.

## Tanım
Tangent portföy (T), risk-free oran $r_f$'den başlatılan bir doğrunun riskli varlık etkin sınırına teğet geçtiği noktayı temsil eder. Bu doğrunun eğimi, mümkün olan en yüksek [[sharpe-orani]]'dır. Two-fund separation teoremine göre, [[risk-free-varlik]] varsayıldığında tüm rasyonel yatırımcıların tutması gereken riskli kompozisyon yalnızca $T$'dir; risk iştahı farkı tek başına $r_f$ ile $T$ arasındaki kaldıraç oranını belirler. Tangent portföy ayrıca CAPM'nin pazar portföyü kavramının kuramsal kökenidir.

## Formül
$$
w_T = \frac{\Sigma^{-1}(\mu - r_f \mathbf{1})}{\mathbf{1}^T \Sigma^{-1}(\mu - r_f \mathbf{1})}
$$
Tangent portföyün Sharpe oranı:
$$
S_T = \sqrt{(\mu - r_f \mathbf{1})^T \Sigma^{-1} (\mu - r_f \mathbf{1})}
$$

## Ana Bağlamlar
- [[sermaye-tahsis-dogrusu-cal]] $r_f$ ile $T$'yi birleştiren doğrudur
- [[sharpe-orani]] tangent portföyde maksimize edilir
- [[risk-free-varlik]] varsayımı olmazsa tangent kavramı tanımsız kalır
- [[etkin-sinir]] hiperbolüne teğet geçer

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — 11 portföyden biri max-Sharpe (tangent) olarak çözülür
- [Tauron](../../projects/tauron/) — multifraktal düzeltilmiş Sharpe altında tangent kayması incelenir
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — getiri-rejim duyarlı tangent karşılaştırması

## Kaynak
[[markowitz-1952]]
