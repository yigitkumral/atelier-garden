---
baslik: "Lévy Alanı (Levy Area)"
slug: "levy-area"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [sde, multidimensional, numerik]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Lévy Alanı (Levy Area)

## Özü
İki bağımsız Brown hareketinin $W^i$, $W^j$ aynı zaman aralığında oluşturduğu, kapalı formda örneklenemeyen iki katlı stokastik integral; çok-boyutlu [[milstein-semasi]]'nın ana zorluğu.

## Tanım
$[t, t+\Delta t]$ aralığında iki Brown bileşeni için Lévy alanı:

$$
A^{ij}_{t, t+\Delta t} = \int_t^{t+\Delta t} \big(W^i_s - W^i_t\big)\, dW^j_s - \int_t^{t+\Delta t} \big(W^j_s - W^j_t\big)\, dW^i_s.
$$

Bu büyüklük $\Delta W^i \cdot \Delta W^j$ artımlarının korelasyonundan **ayrı**, yörüngenin "alan süpürdüğü" ek bilgiyi taşır. Lévy 1951'de bu nesnenin dağılımını çalışmış; karakteristik fonksiyonu kapalı formdadır ama doğrudan örneklemek zordur.

**Pratik etkisi:** Çok-boyutlu Milstein şemasında diyagonal olmayan $\sigma_{ij}$ değişkenleri için terim:

$$
\sum_{j \neq i} \tfrac{1}{2} \sigma_{ik}\, \partial_k \sigma_{ij}\, A^{jk}
$$

ortaya çıkar. Lévy 1951'in seri açılımıyla yaklaşık örnekleme veya Wiktorsson, Foster algoritmaları kullanılır; alternatif olarak ortogonal $\sigma$ matrisi (commutative noise) varsayımıyla terim sıfırlanır.

## Ana Bağlamlar
- [[milstein-semasi]] — terimin doğduğu şema
- [[brownian-motion-wiener]] — kaynak süreç
- [[ito-calculus]] — iki katlı integral biçimciliği
- [[mlmc]] — multi-D MLMC verimliliği Lévy alanı yaklaşımına bağlı

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — multi-asset Heston yörüngelerinde teknik engel

## Kaynak
[[levy-1951]], [[giles-2008]]
