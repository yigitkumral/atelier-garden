---
baslik: "Milstein Şeması"
slug: "milstein-semasi"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [sde, ayrıklaştırma, numerik]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Milstein Şeması

## Özü
[[euler-maruyama]] şemasına Itô-Taylor genişlemesinden gelen ek bir düzeltme terimi ekleyerek **strong order 1.0**'a çıkan SDE ayrıklaştırma yöntemi.

## Tanım
SDE $dX_t = \mu(X_t)\, dt + \sigma(X_t)\, dW_t$ için Milstein güncellemesi:

$$
X_{t+\Delta t} = X_t + \mu \Delta t + \sigma \Delta W_t + \tfrac{1}{2} \sigma\, \sigma'\, \big[(\Delta W_t)^2 - \Delta t\big],
$$

burada $\sigma' = \partial\sigma/\partial X$. Ek terim $\sigma\sigma' \cdot \tfrac{1}{2}[(\Delta W_t)^2 - \Delta t]$ tam olarak [[ito-calculus]]'un ikinci türev düzeltmesinden gelir; klasik Taylor'da ortaya çıkmayan bu terim Itô integralinin tekrarlı uygulanmasıyla doğar.

**Yakınsama:** Strong order $\mathcal{O}(\Delta t)$ — yörünge başına Euler-Maruyama'nın iki katı hassas. Weak order yine $\mathcal{O}(\Delta t)$ olduğundan tek seviyeli MC'de kazanç sınırlı; ancak [[mlmc]] çerçevesinde strong order kritiktir ve toplam maliyeti $\mathcal{O}(\varepsilon^{-2})$'ye indirir.

**Çok-boyutlu kısıtı:** $d > 1$ durumda $W$ bileşenlerinin çapraz [[levy-area]] terimleri ortaya çıkar; bunlar genelde kapalı formda örneklenemez.

## Ana Bağlamlar
- [[euler-maruyama]] — bir mertebe düşük ata şema
- [[levy-area]] — çok-boyutlu Milstein'ın engeli
- [[ito-calculus]] — düzeltme teriminin teorik kaynağı
- [[mlmc]] — Milstein'ın asıl gücünü gösterdiği bağlam

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Heston modelinde yörünge ayrıklaştırması
- [Tauron](../../projects/tauron/) — yüksek doğruluklu yörünge gerektiren simülasyonlar

## Kaynak
[[glasserman-2003]], [[giles-2008]]
