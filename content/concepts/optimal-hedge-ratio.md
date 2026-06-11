---
baslik: "Optimal Hedge Ratio (Minimum Variance Hedge Ratio)"
slug: "optimal-hedge-ratio"
olusturuldu: 2026-05-24
guncellendi: 2026-05-24
etiketler: [finans, turev, hedge, risk-yonetimi, korelasyon, regresyon]
aliases: [h-star, minimum-variance-hedge, korelasyon-hedge]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Optimal Hedge Ratio (Minimum Variance Hedge Ratio)

## Özü
Hedge edilen pozisyonun toplam varyansını minimize eden, fiziki risk birimi başına tutulması gereken futures kontrat oranı. Mükemmel hedge mümkün değilse (cross-hedge, [[basis-risk]] varsa) "1:1 hedge" yanlıştır; optimal oran korelasyon × volatilite çarpışmasıyla bulunur.

## Tanım
Hedger fiziki olarak $S$ tutar, futures'ta $F$ pozisyon açar. Hedge sonu net pozisyon değişimi:
$$
\Delta P = \Delta S - h \cdot \Delta F
$$
$\text{Var}(\Delta P)$ minimize edilirse:
$$
h^* = \rho \cdot \frac{\sigma_S}{\sigma_F}
$$
Burada $\rho$ spot ve futures fiyat değişimleri arasındaki **korelasyon**, $\sigma_S, \sigma_F$ standart sapmalardır.

Bu formül Hull Ch. 3'te türetilmiştir; OLS regresyonunda $\Delta S = \alpha + h^* \Delta F + \epsilon$ denkleminin $h^*$ katsayısıdır.

**Hedge etkinliği** (variance reduction) ise:
$$
\text{Effectiveness} = \rho^2
$$
$\rho = 1$ olursa hedge mükemmel (etkinlik %100); $\rho < 1$ olursa kısmi.

## Türk Gıda Toptancısı için Uygulama
TR yerel buğday fiyatı ile Euronext Milling Wheat (EBM1) korelasyonunu hesapla:

1. **Veri:** Son 2-3 yıl haftalık TR yerel buğday alış fiyatı (TMO, ticaret borsası) + EBM1 kapanış fiyatı (EUR/TL'ye çevrilmiş).
2. **Korelasyon:** Pandas/NumPy ile $\rho$ hesapla.
3. **Volatilite oranı:** $\sigma_{S}/\sigma_F$ standart sapmalardan.
4. **Hedge ratio:** $h^* = \rho \cdot \sigma_S / \sigma_F$
5. **Kontrat sayısı:** Fiziki risk (ton) × $h^*$ ÷ kontrat büyüklüğü (EBM1 için 50 ton).

**Pratik kural** (ChatGPT GPT-5 önerisi): Türkiye gibi basis riski yüksek pazarda başlangıç için **%30–60 hedge oranı** önerilir. $h^* = 0.8$ hesaplansa bile şirket içi limit %50'ye çekilir → margin call tamponu artar.

## Hedge Etkinliği Eşikleri
| $\rho^2$ | Hedge Kararı |
|---|---|
| > 0.80 | Güçlü hedge; uygulanabilir |
| 0.50 - 0.80 | Orta hedge; kısmi (%50-60) ile dene |
| 0.30 - 0.50 | Zayıf hedge; futures yerine forward / opsiyon düşün |
| < 0.30 | Hedge önerilmez; cross-hedge anlamsız |

## Ana Bağlamlar
- [[basis-risk]] — h* mükemmel hedge'i mümkün kılmaz, basis kalır
- [[futures-hedging-stratejileri]] — h* uygulanırken kullanılır
- [[korelasyon]] (eğer mevcutsa) — $\rho$ tanımı
- [[varyans]] / [[regresyon-analizi]] — formülün türetildiği istatistiksel zemin

## Projelerde Kullanım
- [Gıda Toptancı Emtia Hedging](../../projects/gida-toptanci-emtia-hedging/) — TR yerel vs global futures korelasyon hesabı Faz 2 görevi
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — multifraktal analiz $\rho$ tahminlerini zenginleştirebilir
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — minimum variance prensibi portföy teorisiyle ortak

## Kaynak
- Hull, J. (2018). *Options, Futures, and Other Derivatives*, Ch. 3 "Hedging Strategies Using Futures"
- Ederington, L. H. (1979). "The Hedging Performance of the New Futures Markets". *Journal of Finance*, 34(1).
