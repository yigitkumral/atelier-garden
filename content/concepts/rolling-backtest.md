---
baslik: "Rolling Backtest"
slug: "rolling-backtest"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [backtest, validasyon, fpa]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Rolling Backtest (29 Rebalans, 4 Strateji)

## Özü
Kayan pencere üzerinde dönemsel olarak portföy ağırlıklarının yeniden dengelenmesi (rebalancing) ve out-of-sample performansın izlenmesi — FPA'nın temel doğrulama protokolü.

## Tanım
FPA pipeline'ında rolling backtest kuralları: (a) eğitim penceresi (örn. 252 işlem günü) üzerinde optimum ağırlık $w^*$ hesaplanır, (b) bu ağırlık takip eden gelecek pencerede (örn. 21 işlem günü) tutulur, (c) pencere kaydırılır ve süreç tekrarlanır. Toplam 29 rebalans noktası tipik bir orta-uzun çalışma dönemi (yaklaşık 5 yıl) verir. Karşılaştırılan 4 strateji: (1) klasik mean-variance Markowitz, (2) minimum-varyans, (3) eşit-ağırlık (1/N baseline), (4) Hurst-tabanlı (FPA önerisi). Performans metrikleri: realize edilen Sharpe, max drawdown, turnover, ortalama portföy Hurst $H_p$. Bulgu: Hurst-tabanlı stratejinin in-sample avantajı out-of-sample'da büyük ölçüde kaybolur; eşit-ağırlık baseline'ı şaşırtıcı biçimde rekabetçidir (bu, klasik Markowitz literatüründeki DeMiguel-2009 bulgusunun fraktal varyantıdır). Sonuç [[out-of-sample-cokus]] anlatısını destekler.

## Formül
Pencere kaydırma:
$$
[t, t + W_{\text{train}}] \to w^*(t), \qquad \text{tutuş: } [t + W_{\text{train}}, t + W_{\text{train}} + W_{\text{hold}}]
$$
Sharpe (out-of-sample):
$$
\text{SR}_{\text{oos}} = \frac{\bar{r}_p - r_f}{\sigma_p}
$$
Turnover:
$$
\text{TO} = \frac{1}{T-1} \sum_{k=1}^{T-1} \| w_{k+1} - w_k^- \|_1
$$

## Ana Bağlamlar
- [[out-of-sample-cokus]] gözlem sonucu
- [[markowitz-paralelligi]] karşılaştırma temeli
- [[survivorship-bias-duzeltmesi]] veri setinin temizliği
- [[block-bootstrap]] güven aralıkları

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — projenin ana validasyon iskeletini oluşturur, faz1 ve faz2 raporlarının metrik kaynağı
- [Tauron](../../projects/tauron/) — fraktal cezalı portföyün de aynı pipeline ile test edilmesi planı
- [IMF527 Portföy](../../projects/ders/) — klasik Markowitz uygulamasının görsel paraleli

## Kaynak
[[aygoren-uyar-2023]]
