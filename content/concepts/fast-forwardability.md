---
baslik: "Fast-Forwardability"
slug: "fast-forwardability"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, simulasyon, montecarlo]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Fast-Forwardability

## Özü
Bir stokastik sürecin gelecek dağılımını $T$ ufkuna kadar **ara zaman adımlarını işlemeden** doğrudan örnekleyebilme özelliği; kuantum türev fiyatlamada kuantum hızlanmasının korunması için kritik koşul.

## Tanım
Klasik Hamilton simülasyonu için "fast-forward" terimi: $e^{-iHt}$ unitarisini $\mathcal{O}(\text{poly}\log t)$ kuantum maliyetiyle uygulayabilmek (lineer $t$ yerine). Atia-Aharonov 2017 ve sonrası, sadece commuting/dejenere Hamiltonyenler veya özel yapı (örn. düzgün Hamilton spektrumu) için fast-forward'ın mümkün olduğunu gösterir.

**Stokastik finans bağlamı (Herman et al. 2026):**
Bir SDE'nin $X_T$ marjinal dağılımı, ara $\Delta t$ adımlarını işlemeden tek bir kuantum devresiyle yüklenebiliyorsa süreç **fast-forwardable** denir. Bu, ya:
- Kapalı form geçiş yoğunluğu (Black-Scholes log-normal, [[cir-modeli]] non-central chi-squared, [[broadie-kaya-2006]] Heston exact)
- Yarı-analitik [[karakteristik-fonksiyon]] $\varphi(t, T)$ üzerinden ters Fourier
- [[qet]] tabanlı düzgün polinom yaklaşımı

ile sağlanır. Aksi hâlde Euler/Milstein zincirinin $T/\Delta t$ adımı kuantum devresine girer ve [[qae]] hızlanması toplam maliyette yutulur.

**Kritik sonuç:** Yol-bağımsız (Avrupa) opsiyonlar fast-forwardable modellerde tam quadratic hızlanma sağlar; yol-bağımlı (Asya, Bermuda) opsiyonlar ekstra trick gerektirir ([[chakrabarti-2021]] reparameterization).

## Ana Bağlamlar
- [[karakteristik-fonksiyon]] — Fourier yolu
- [[broadie-kaya-2006]] — Heston exact örneği
- [[qet]] — polinom yaklaşım çerçevesi
- [[kuantum-turev-fiyatlama]] — ana kullanım alanı
- [[chakrabarti-2021]] — yol-bağımlı genişletme

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al.'in ana kavramsal katkısı

## Kaynak
[[herman-2026]], [[broadie-kaya-2006]]
