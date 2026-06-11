---
baslik: "Payoff Fonksiyonu"
slug: "payoff-fonksiyonu"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, opsiyon]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Payoff Fonksiyonu

## Özü
Bir türev sözleşmenin vade veya kullanım anındaki nakit ödemesini, dayanak varlık yörüngesine bağlı olarak belirleyen kuraldır.

## Tanım
Türev fiyatlama, payoff'un risk-nötr beklenen değerinin iskonto edilmesi olarak özetlenir. Path-independent ürünlerde (klasik [[avrupa-opsiyonu]]) payoff yalnızca vade fiyatı $S_T$'ye bağlıdır; örneğin call opsiyonu $\max(S_T - K, 0)$ verir. Path-dependent ürünlerde ([[asyali-opsiyonu]], bariyer, lookback) payoff yörüngenin tamamına bağımlıdır ve genellikle kapalı-form çözüm yoktur — [[monte-carlo-entegrasyonu]] veya kuantum genişlemeleri gerekir. Payoff fonksiyonunun doğrusal olmaması, opsiyonların asimetrik risk profilinin matematiksel kaynağıdır.

## Formül
Avrupa call: $h(S_T) = \max(S_T - K, 0) = (S_T - K)^+$. Asyalı (geometrik ortalama): $h = \max\!\left(\big(\prod_{i=1}^n S_{t_i}\big)^{1/n} - K, 0\right)$. Genel fiyat:
$$
V_0 = e^{-rT} \mathbb{E}^{\mathbb{Q}}\!\left[h(S_{[0,T]})\right]
$$

## Ana Bağlamlar
- [[avrupa-opsiyonu]] — path-independent payoff örneği
- [[asyali-opsiyonu]] — path-dependent payoff örneği
- [[black-scholes]] — payoff'a uygulanan iskonto-beklenti formülü
- [[monte-carlo-entegrasyonu]] — kapalı formu olmayan payoff'ların değerlemesi

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — opsiyon türleri sınıflaması
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum amplitüd kodlamada hedef fonksiyon

## Kaynak
[[hull-2008]]
