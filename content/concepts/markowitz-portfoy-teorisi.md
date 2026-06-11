---
baslik: "Markowitz Portföy Teorisi"
slug: "markowitz-portfoy-teorisi"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, optimizasyon, portfoy]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Markowitz Portföy Teorisi

## Özü
Yatırımcının beklenen getiri ile varyans arasında bir ödünleşme yaptığı, çoklu varlık seçiminde çeşitlendirmenin matematiksel temelini kuran modern portföy teorisidir.

## Tanım
Teori, bireysel varlık getirilerinin ortalama vektörü $\mu$ ve kovaryans matrisi $\Sigma$ verildiğinde, ağırlık vektörü $w$'nin seçimini bir kuadratik optimizasyon problemi olarak kurar. Yatırımcının amacı, sabit bir hedef getiri $\mu^*$ için portföy varyansını minimize etmek ya da sabit bir varyans için beklenen getiriyi maksimize etmektir. Çözüm kümesi $\mu$-$\sigma$ düzleminde [[etkin-sinir]] olarak adlandırılan bir hiperbol oluşturur. Markowitz, çeşitlendirmenin etkisini formüle ederek riskin yalnızca tekil varyansların değil, varlıklar arası kovaryansların da fonksiyonu olduğunu göstermiştir.

## Formül
Standart problem:
$$
\min_w \; \tfrac{1}{2} w^T \Sigma w \quad \text{s.t.} \quad w^T \mu = \mu^*, \; w^T \mathbf{1} = 1
$$
Portföy varyansı:
$$
\sigma_p^2 = w^T \Sigma w
$$
Burada $w \in \mathbb{R}^N$ varlık ağırlıkları, $\Sigma$ ise [[kovaryans-matrisi]]'dir.

## Ana Bağlamlar
- [[etkin-sinir]] çözüm kümesinin geometrisini tanımlar
- [[abcd-parametreleri]] kapalı-form çözüm iskeletini sağlar
- [[minimum-varyans-portfoyu]] etkin sınırın en sol noktasıdır
- [[kovaryans-matrisi]] çeşitlendirme etkisinin ana girdisidir
- [[markowitz-1952]] orijinal makaledir

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — 11 portföyün karar matrisi tam olarak bu kuadratik problemin çözümüdür
- [Tauron](../../projects/tauron/) — multifraktal düzeltmenin uygulandığı klasik temel
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — kuadratik form analizinin (örn. $H_p \approx c_t + w^T C_t w$) çıkış noktası

## Kaynak
[[markowitz-1952]]
