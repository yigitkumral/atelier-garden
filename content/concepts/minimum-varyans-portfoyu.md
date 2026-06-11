---
baslik: "Minimum Varyans Portföyü"
slug: "minimum-varyans-portfoyu"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, portfoy, optimizasyon]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Minimum Varyans Portföyü

## Özü
Hedef getiri kısıtı kaldırıldığında yalnızca toplam varyansı minimize eden, [[etkin-sinir]]'in en sol ucunda yer alan portföydür (MVP).

## Tanım
Minimum varyans portföyü (MVP, *minimum variance portfolio*), ağırlıkların tek kısıtının $w^T \mathbf{1} = 1$ olduğu kuadratik problem altında kovaryans matrisinin yapısını yansıtır; beklenen getiri vektörü $\mu$ buraya hiç girmez. Bu, MVP'nin getiri tahmin hatalarına karşı [[tangent-portfoy]]'a kıyasla dayanıklı olmasının nedenidir. Pratikte tahminci gürültüsünün getiri vektöründe varyans-kovaryans matrisinden çok daha büyük olduğu yaygın bulgu, MVP'nin out-of-sample testlerde tangent portföyü genellikle geride bırakmasını açıklar.

## Formül
$$
w_{\text{MVP}} = \frac{\Sigma^{-1} \mathbf{1}}{\mathbf{1}^T \Sigma^{-1} \mathbf{1}}
$$
Karşılık gelen varyans:
$$
\sigma_{\text{MVP}}^2 = \frac{1}{\mathbf{1}^T \Sigma^{-1} \mathbf{1}} = \frac{1}{C}
$$
burada $C$ [[abcd-parametreleri]]'nden gelir.

## Ana Bağlamlar
- [[etkin-sinir]] hiperbolünün uç noktasıdır
- [[markowitz-portfoy-teorisi]] içinde özel hâl
- [[abcd-parametreleri]] $C$ skaleri MVP varyansını verir
- [[kovaryans-matrisi]] tek girdidir; $\mu$ rol almaz

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — 11 portföyden biri MVP olarak hesaplanır, kıyaslama bench'i
- [Tauron](../../projects/tauron/) — fraktal düzeltme öncesi/sonrası MVP kayması simülatörde gösterilir
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — kuadratik form $w^T C_t w$ minimizasyonunun klasik analog

## Kaynak
[[markowitz-1952]]
