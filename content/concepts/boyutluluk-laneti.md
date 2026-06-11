---
baslik: "Boyutluluk Laneti"
slug: "boyutluluk-laneti"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [numerik, entegrasyon, kompleksite]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Boyutluluk Laneti

## Özü
Grid (kafes) tabanlı numerik integrasyon yöntemlerinin maliyetinin boyut $d$ ile üstel olarak büyümesi olgusu; finansal yörünge integrallerinde MC'nin niçin tek pratik seçenek olduğunu açıklar.

## Tanım
Tek boyutta $n$ kafes noktasıyla $\mathcal{O}(n^{-k})$ doğruluk veren bir kuadratür kuralı, $d$ boyutta $n^d$ noktaya ihtiyaç duyar — toplam maliyet:

$$
N_{\text{grid}} = n^d, \quad \text{hata} \sim N_{\text{grid}}^{-k/d}.
$$

Yani boyut arttıkça hatanın yakınsama hızı $1/d$ ile yavaşlar. Buna karşılık [[monte-carlo-entegrasyonu]] hatası $\mathcal{O}(N^{-1/2})$ ile **boyuttan bağımsızdır**. Türev fiyatlamada zaman ızgarası $T/\Delta t$ adımlı her yörünge $d \sim 100$–$1000$ boyutlu bir integrale denk düşer; grid burada imkansız hale gelir.

Bellman'ın 1957'de "curse of dimensionality" diye adlandırdığı bu olgu, optimizasyon, makine öğrenmesi ve PDE çözümünde de aynı şekilde ortaya çıkar.

## Ana Bağlamlar
- [[monte-carlo-entegrasyonu]] — laneti aşmanın klasik yolu
- [[mlmc]] — MC'nin kendi lanetini (zaman boyutu) kıran varyant
- [[qmci]] — kuantum hızlanma yine boyut-bağımsız
- [[karakteristik-fonksiyon]] — Fourier yöntemleri tek boyutta lanete takılmaz

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al.'in klasik MC seçimini gerekçelendiren temel argüman
- [Seminer](../../projects/ders/2026-bahar-seminer/) — yüksek boyutlu finans problemlerinin niçin kuantum-uygun olduğu

## Kaynak
[[glasserman-2003]]
