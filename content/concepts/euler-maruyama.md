---
baslik: "Euler-Maruyama Şeması"
slug: "euler-maruyama"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [sde, ayrıklaştırma, numerik]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Euler-Maruyama Şeması

## Özü
Stokastik diferansiyel denklemleri (SDE) zamanda ayrıklaştırarak yörünge üretmenin en basit yöntemi; **strong order 0.5**, **weak order 1.0** yakınsamayla çalışır.

## Tanım
Genel SDE:

$$
dX_t = \mu(X_t, t)\, dt + \sigma(X_t, t)\, dW_t.
$$

Euler-Maruyama, $\Delta t = T/N$ adımıyla:

$$
X_{t+\Delta t} = X_t + \mu(X_t, t)\, \Delta t + \sigma(X_t, t)\, \Delta W_t,
$$

burada $\Delta W_t \sim \mathcal{N}(0, \Delta t)$ bağımsız Gauss artımları. Yöntem deterministik Euler şemasının doğal stokastik genelidir.

**Yakınsama düzeni:**
- **Strong** (yörünge bazında): $\mathbb{E}[|X_T^{\Delta t} - X_T|] = \mathcal{O}(\Delta t^{0.5})$
- **Weak** (dağılım bazında): $|\mathbb{E}[g(X_T^{\Delta t})] - \mathbb{E}[g(X_T)]| = \mathcal{O}(\Delta t)$

Türev fiyatlama yalnızca beklenen payoff istediğinden weak order önemlidir; ancak [[mlmc]] gibi varyans azaltma yöntemleri strong order'a duyarlıdır — burada [[milstein-semasi]] tercih edilir.

## Ana Bağlamlar
- [[ito-calculus]] — şemanın türetildiği teorik çerçeve
- [[milstein-semasi]] — bir mertebe daha hassas karşıtı
- [[brownian-motion-wiener]] — $\Delta W_t$ kaynağı
- [[heston-stokastik-volatilite]] — pratikte ayrıklaştırılan model

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Heston/SABR yörünge üretiminde başlangıç şeması
- [Tauron](../../projects/tauron/) — multifraktal SDE simülasyonlarında olası ayrıklaştırma adımı

## Kaynak
[[glasserman-2003]], [[herman-2026]]
