---
baslik: "Sharpe Oranı"
slug: "sharpe-orani"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, performans, risk]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Sharpe Oranı

## Özü
Risk-free oran üzerinde elde edilen aşan getirinin toplam standart sapmaya bölümü olan, birim risk başına ödüllendirmeyi ölçen klasik performans göstergesidir.

## Tanım
Sharpe oranı, William Sharpe (1966) tarafından "reward-to-variability ratio" olarak önerilmiştir; bir portföyün getiri profilini risk-free varlığa göre normalize eder. [[sermaye-tahsis-dogrusu-cal]]'in eğimi tam olarak [[tangent-portfoy]]'un Sharpe oranıdır; bu nedenle Sharpe maksimizasyonu, risk-free varlık varsayımı altında [[markowitz-portfoy-teorisi]]'nin doğal hedef fonksiyonuna dönüşür. Sharpe oranı toplam riski (volatiliteyi) ceza yazdığı için sistematik ve özgül risk ayrımı yapmaz; bu yönüyle Treynor oranı veya Information Ratio'dan ayrışır. Ek olarak, getiri dağılımının asimetrisi ve fat-tailed-dagilim özellikleri Sharpe'ın tek başına yetersiz kaldığı durumlardır.

## Formül
$$
S = \frac{\mathbb{E}[R_p] - r_f}{\sigma_p}
$$
Tangent portföyde maksimize edilen değer:
$$
S_T = \sqrt{(\mu - r_f \mathbf{1})^T \Sigma^{-1} (\mu - r_f \mathbf{1})}
$$

## Ana Bağlamlar
- [[tangent-portfoy]] Sharpe'ı maksimize eden noktadır
- [[sermaye-tahsis-dogrusu-cal]] eğimi $S_T$
- [[risk-free-varlik]] tanımın referans noktasıdır
- [[markowitz-portfoy-teorisi]] içinde alternatif hedef fonksiyon

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — 11 portföyün karşılaştırma metriklerinden biri
- [Tauron](../../projects/tauron/) — multifraktal ceza ile düzeltilmiş "fraktal Sharpe" varyantı tanımlanır
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — Hurst-bağımlı performans karşılaştırmasında temel kontrol metriği

## Kaynak
[[markowitz-1952]]
