---
baslik: "Markowitz (1952) — Portfolio Selection"
slug: "markowitz-1952"
yazarlar: ["Harry Markowitz"]
yil: 1952
dergi: "Journal of Finance"
volume: 7
issue: 1
sayfalar: "77-91"
doi: "10.2307/2975974"
citekey: "markowitz1952"
etiketler: [finans, klasik, portfoy]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Markowitz (1952) — Portfolio Selection

## Künye
Markowitz, H. (1952). Portfolio Selection. *Journal of Finance*, 7(1), 77–91. DOI: 10.2307/2975974.

## Ana Argüman
Yatırımcı kararının yalnızca beklenen getiri maksimizasyonuna indirgenemeyeceğini, varyansın da bağımsız bir karar değişkeni olduğunu savunur. Çeşitlendirme rastgele bir uygulama değil, varlıklar arası kovaryansların aktif olarak yönetildiği matematiksel bir işlemdir. Makale bu çerçevede beklenen getiri ile varyans arasındaki ödünleşmeyi optimize eden portföy kümesini "etkin küme" olarak tanımlar.

## Yöntem
Çoklu varlık getirileri rastgele değişken kabul edilir; portföy ağırlıkları $w$ üzerinde tanımlı beklenen getiri $w^T\mu$ ve varyans $w^T \Sigma w$ kullanılarak ikinci dereceden bir optimizasyon problemi kurulur. Bütçe kısıtı $w^T \mathbf{1} = 1$ ve hedef getiri kısıtı $w^T \mu = \mu^*$ altında varyans minimize edilir; problemin Lagrange çözümü, etkin sınırın geometrisini analitik olarak verir. Makalede çözüm hem grafiksel (E-V düzlemi) hem de küçük örnek üzerinden sayısal olarak gösterilmiştir.

## Bulgular
- Etkin küme $\mu$-$\sigma^2$ düzleminde bir parabol ($\mu$-$\sigma$ düzleminde hiperbol) çizer.
- Çeşitlendirmenin etkisi, kovaryans matrisi $\Sigma$'nın köşegen-dışı yapısına bağlıdır; düşük korelasyonlu varlıklar portföy varyansını dramatik biçimde düşürür.
- Yatırımcı tercihi, tüm uygulanabilir portföy uzayında değil, yalnızca etkin küme üzerinde tanımlanır.

## Etkisi
Modern Portfolio Theory'nin (MPT) temelini atmıştır; Markowitz bu çalışmayla 1990 Nobel Ekonomi Ödülü'nü Sharpe ve Miller ile paylaşmıştır. Çalışma, Tobin'in (1958) [[risk-free-varlik]] eklenmesi, Sharpe'ın (1964) CAPM ve [[sharpe-orani]] türetimleri için zemin oluşturmuştur. Pratikte ise "kovaryans matrisi tahmin gürültüsü" ve "estimator-gurultusu-bias-variance" tartışmalarını başlatmış; out-of-sample-cokus literatürünün çıkış noktası olmuştur.

## İlgili Kavramlar
- [[markowitz-portfoy-teorisi]]
- [[etkin-sinir]]
- [[minimum-varyans-portfoyu]]
- [[tangent-portfoy]]
- [[sermaye-tahsis-dogrusu-cal]]
- [[abcd-parametreleri]]
- [[kovaryans-matrisi]]
- [[sharpe-orani]]
- [[risk-free-varlik]]
- [[nested-portfoy]]

## Atıf yapan projeler
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/)
- [Tauron](../../projects/tauron/)
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/)
