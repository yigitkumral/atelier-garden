---
baslik: "Bipartite Korelasyon Yapısı"
slug: "bipartite-korelasyon"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [stokastik-volatilite, multi-asset, kovaryans]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Bipartite Korelasyon Yapısı

## Özü
Çoklu varlıklı Heston modellerinde fiyat ve varyans Wiener süreçlerinin iki blok halinde — varlıklar-arası ve fiyat-varyans — kümeleşmiş korelasyon matrisi düzenidir.

## Tanım
$d$ varlık için multi-asset [[heston-stokastik-volatilite]] modelinde her varlığın bir fiyat ve bir varyans süreci vardır; toplam $2d$ Wiener faktörünün korelasyon matrisi bipartite bir bloklu yapıda kurulur. Diagonal $d \times d$ alt-blok varlıkların fiyat-varyans [[leverage-effect]]'lerini ($\rho_i$) içerir; off-diagonal bloklar ise fiyat-fiyat ve varyans-varyans çapraz korelasyonlarını taşır. Pozitif yarı-tanımlılık (PSD) kısıtı, ham parametre seçiminin bir projeksiyon adımı gerektirebilmesi anlamına gelir. Yapı, kuantum amplitüd tahmininde rejister kodlamasının doğal şekilde paralelleştirilmesine de imkan tanır.

## Formül
Genel blok yapı:
$$
\Sigma = \begin{pmatrix} \Sigma_{SS} & \Sigma_{Sv} \\ \Sigma_{Sv}^\top & \Sigma_{vv} \end{pmatrix}, \quad (\Sigma_{Sv})_{ii} = \rho_i \quad (\text{leverage})
$$
PSD koşulu: tüm öz değerler $\ge 0$.

## Ana Bağlamlar
- [[heston-stokastik-volatilite]] — tek-varlık temelinin genişlemesi
- [[leverage-effect]] — diagonal $\rho_i$ değerlerinin ekonomik anlamı
- [[kovaryans-matrisi]] — bloklu PSD yapı
- [[kuantum-turev-fiyatlama]] — yapının kuantum kodlamada paralelleşmesi

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — multi-asset stokastik vol matematiği
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — sepet/spread opsiyonlarının kuantum simülasyonu

## Kaynak
[[heston-1993]], [[glasserman-2003]]
