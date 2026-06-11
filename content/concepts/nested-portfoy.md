---
baslik: "Nested Portföy"
slug: "nested-portfoy"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, portfoy, hiyerarsi]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Nested Portföy

## Özü
Bir veya daha fazla bileşeni başka bir portföy olan, yani iç-içe (hiyerarşik) ağırlık katmanlarıyla tanımlanan sentetik portföy yapısıdır.

## Tanım
Nested (iç-içe) portföy yapısında dış katman, alt-portföyleri tek bir varlık gibi ele alıp onlara üst-seviye ağırlıklar atar; alt-portföyler ise kendi içinde varlık ağırlıkları taşır. Örnek: dış ağırlık $w_T = (0.6, 0.4)$ "hisse alt-portföyü" ve "tahvil alt-portföyü"ne; alt-portföyler kendi içinde $N_1$ ve $N_2$ varlığa dağıtılmış olabilir. Nihai varlık-seviyesi ağırlık vektörü $w$ tensör çarpımı/zincirleme ile elde edilir. Bu yapı, hiyerarşik risk paritesi, fon-of-fund tasarımları ve [[markowitz-portfoy-teorisi]]'nin two-fund/three-fund separation teoremlerinde doğal olarak ortaya çıkar; özellikle [[risk-free-varlik]] + [[tangent-portfoy]] kombinasyonu en yalın iki katmanlı nested örnektir.

## Formül
İki katman: $w_{\text{toplam},i} = u_k \cdot v_{i|k}$, burada $u_k$ alt-portföy $k$'nın dış ağırlığı, $v_{i|k}$ varlık $i$'nin alt-portföy içindeki payı. Portföy varyansı:
$$
\sigma_p^2 = u^T \Sigma_{\text{alt}} u
$$
burada $\Sigma_{\text{alt}}$ alt-portföy getirilerinin kovaryans matrisidir.

## Ana Bağlamlar
- [[markowitz-portfoy-teorisi]] separation teoremleri nested yapı kurar
- [[tangent-portfoy]] + [[risk-free-varlik]] iki katmanlı en yalın nested
- [[kovaryans-matrisi]] alt-portföy seviyesinde yeniden tanımlanır

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — risk-free + riskli karışımı zaten iki katmanlı nested yapı sayılır
- [Tauron](../../projects/tauron/) — sektör/varlık-sınıfı bazlı multifraktal ağırlıklandırma için nested şablon
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — rejim-bazlı alt-portföy ağırlık birleşiminde nested yapı

## Kaynak
[[markowitz-1952]]
