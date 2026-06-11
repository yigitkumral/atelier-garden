---
baslik: "Multi-Level Monte Carlo (MLMC)"
slug: "mlmc"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [montecarlo, varyans-azaltma, numerik]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Multi-Level Monte Carlo (MLMC)

## Özü
Farklı çözünürlükteki yörünge ayrıklaştırmalarını teleskopik biçimde birleştirerek standart MC'nin maliyetini $\mathcal{O}(\varepsilon^{-2}\log^2\varepsilon)$ veya $\mathcal{O}(\varepsilon^{-2})$'ye indiren Giles 2008 yöntemi.

## Tanım
$P_\ell$ ile $\ell$ seviyesinde (adım $h_\ell = h_0 \cdot 2^{-\ell}$) ayrıklaştırılmış payoff'u gösterelim. Teleskop:

$$
\mathbb{E}[P_L] = \mathbb{E}[P_0] + \sum_{\ell=1}^{L} \mathbb{E}[P_\ell - P_{\ell-1}].
$$

Her seviye terimi $Y_\ell = P_\ell - P_{\ell-1}$ **aynı Brown yörüngesi** kullanılarak hesaplanır (coupling); böylece $V_\ell = \mathrm{Var}(Y_\ell) \to 0$ ($\ell \to \infty$). Toplam tahminci:

$$
\hat{P} = \sum_{\ell=0}^{L} \frac{1}{N_\ell} \sum_{i=1}^{N_\ell} Y_\ell^{(i)}, \quad N_\ell \propto \sqrt{V_\ell / C_\ell}.
$$

**Maliyet teoremi:** $V_\ell = \mathcal{O}(h_\ell^\beta)$, $C_\ell = \mathcal{O}(h_\ell^{-\gamma})$, bias $= \mathcal{O}(h_L^\alpha)$ olduğunda:
- $\beta > \gamma$: toplam maliyet $\mathcal{O}(\varepsilon^{-2})$
- $\beta = \gamma$: $\mathcal{O}(\varepsilon^{-2}\log^2\varepsilon)$

Avrupa opsiyonu + Euler ($\beta=1$) için ikinci, Milstein ($\beta=2$) için ilk durum geçerli; varyans-strong order kritik.

## Ana Bağlamlar
- [[monte-carlo-entegrasyonu]] — temel yöntem
- [[milstein-semasi]] — $\beta=2$ rejimi için gerekli
- [[euler-maruyama]] — $\beta=1$ rejimi
- [[qmci]] — kuantum-MLMC füzyonu (An 2021)

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — klasik baseline ve QMCI ile birleştirilmiş hibrit (An 2021)
- [Seminer](../../projects/ders/2026-bahar-seminer/) — varyans azaltmanın kanonik örneği

## Kaynak
[[giles-2008]], [[an-2021]]
