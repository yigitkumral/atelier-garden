---
baslik: "Avrupa Opsiyonu"
slug: "avrupa-opsiyonu"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, opsiyon]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Avrupa Opsiyonu

## Özü
Yalnızca vade gününde kullanılabilen, payoff'u sadece vade fiyatına bağlı path-independent klasik opsiyon sözleşmesidir.

## Tanım
Avrupa tipi call/put opsiyonları, sahibine yalnızca vade tarihi $T$'de dayanak varlığı önceden belirlenmiş kullanım fiyatı $K$'den alma (call) veya satma (put) hakkı verir. [[payoff-fonksiyonu]] $S_T$'ye bağlı olduğundan değerleme, risk-nötr ölçü altında log-normal beklenen değerin iskonto edilmesine indirgenir; bu da [[black-scholes]] kapalı formunu doğurur. Path-independent yapısı, hem analitik tractability hem de [[greeks]] hesaplamasının kolaylığını sağlar. Erken kullanım hakkı yoktur, bu yönüyle Amerikan ve Bermudan opsiyonlardan ayrılır.

## Formül
Call payoff (vade $T$):
$$
h_{\text{call}}(S_T) = \max(S_T - K, 0)
$$
Black-Scholes kapalı form:
$$
C = S_0 \Phi(d_1) - K e^{-rT}\Phi(d_2)
$$

## Ana Bağlamlar
- [[payoff-fonksiyonu]] — vade fiyatına bağlı tek-noktalı payoff
- [[black-scholes]] — Avrupa opsiyonun kapalı-form değerlemesi
- [[greeks]] — Avrupa opsiyondan türetilen duyarlılıklar
- [[asyali-opsiyonu]] — path-dependent karşıtı

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — pedagojik başlangıç ürünü
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum vs klasik karşılaştırmasında baseline

## Kaynak
[[black-scholes-1973]], [[hull-2008]]
