---
baslik: "Bouchaud — Volatility Clustering ve Fat Tails"
slug: "bouchaud-volatility-clustering"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [literature, bouchaud, ekonofizik, volatilite-clustering, fat-tail]
yazarlar: ["Bouchaud, Jean-Philippe", "Potters, Marc"]
yil: 2003
turu: kitap-ve-makale-kumesi
citekey: bouchaud-volatility
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Bouchaud — Volatility Clustering ve Fat Tails

## Künye
Ana referans: Bouchaud, J.-P. & Potters, M. (2003). *Theory of Financial Risk and Derivative Pricing: From Statistical Physics to Risk Management* (2. baskı). Cambridge University Press. Tamamlayıcı: Bouchaud ve grubunun (Capital Fund Management) 1990'lar-2010'lar makaleleri. Ekonofizik perspektifiyle finansal piyasa istatistiklerinin sistematik tarama metni.

## Ana Argüman
Finansal piyasaların üç ana ampirik "stylized facts" özelliği vardır: (1) getirilerin **fat-tailed** dağılımı (bkz. [[fat-tailed-dagilim]]), (2) **volatilite kümeleri** — yüksek volatilite günleri yüksek volatiliteyi izler, otokorelasyon $\rho(|r_t|, |r_{t+\tau}|)$ uzun-vadeli pozitif, (3) **levarage effect** — negatif getirilerin volatiliteyi pozitif getirilerden daha çok artırması (asimetri). Bu üç olgu klasik Black-Scholes/Markowitz çerçevesi tarafından açıklanmaz; multifraktal/stokastik volatilite modelleri tarafından açıklanır.

## Yöntem
- Çoklu zaman serisi (hisse, vadeli, döviz) üzerinde mutlak getiri otokorelasyon fonksiyonunun (ACF) hesabı: $\rho(\tau) = \text{Corr}(|r_t|, |r_{t+\tau}|)$
- Power-law fit: $\rho(\tau) \sim \tau^{-\beta}$ (volatilite ACF'sinin yavaş azalması — long memory)
- Random Matrix Theory (RMT) ile kovaryans matrisinin gürültü filtrasyonu
- Monte Carlo modelleri ile teorik karşılaştırma

## Bulgular
- Volatilite ACF üssel azalmaz; yaklaşık power-law $\beta \approx 0.2 - 0.3$ — saatlerce hatta haftalarca süren memory
- Getiri kuyrukları için $\alpha \approx 3-4$ (Mandelbrot 1963 önerdiği $<2$ değil; ancak Gauss da değil)
- Leverage effect tipik 5-15 işlem günü relaxation süresi ile gözlenir
- Kovaryans matrisinin eigenvalue dağılımı Marchenko-Pastur'la kısmen uyumlu, fakat birkaç "outlier" eigenvalue gerçek piyasa modlarını yansıtır

## Etkisi
- Ekonofizik akımının pratisyen finansa (özellikle quant hedge fund'lar) en doğrudan köprüsü; yazarlar CFM'in kurucularındandır
- Volatilite kümeleri olgusu modern stokastik volatilite modellerinin (Heston, GARCH, MRW) ana motivasyonu
- Yiğit Kumral'ın seminer ve FPA projelerinde "stylized facts" çerçevesi olarak kullanılır
- Tauron'da fraktal cezanın motivasyonu: volatilite ACF'sinin uzun-vadeli yapısı ölçek-bağımlı parametrelere ihtiyaç gösterir

## İlgili Kavramlar
- [[fat-tailed-dagilim]] — birinci stylized fact
- [[multifraktal-spektrum]] — modern açıklama çerçevesi
- [[heston-stokastik-volatilite]] — leverage effect içeren parametrik model
- [[zeta-q-olcekleme]] — multifraktal genelleştirme

## Atıf Yapan Projeler
- [Seminer](../../projects/) — "stylized facts" anlatımının ana kaynağı
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — kovaryans matrisi RMT analizinin referansı
- [Tauron](../../projects/tauron/) — multifraktal ceza terimi motivasyonu
