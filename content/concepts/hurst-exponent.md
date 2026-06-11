---
baslik: "Hurst Üsteli"
slug: "hurst-exponent"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, zaman-serisi, persistence, multifraktal]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Hurst Üsteli (H)

## Özü
Bir zaman serisinin uzun-vadeli hafızasını ve persistans yapısını tek bir sayıyla özetleyen ölçek üsteli; rastgele yürüyüşten sapmayı ölçer.

## Tanım
$H \in (0,1)$ aralığında bir parametre olup, ölçeklendirilmiş bir istatistiğin (klasik olarak [[rescaled-range-rs]]) zaman penceresi $\tau$ ile nasıl büyüdüğünü kurar. $H = 0.5$ değeri klasik Brownian davranışı (bağımsız artımlar) belirtir; $H > 0.5$ persistent (trendi sürdüren) seriyi, $H < 0.5$ anti-persistent (mean-reverting) seriyi işaret eder. Finansal zaman serileri için $H \neq 0.5$ olması, getirilerin bağımsızlık varsayımının ihlal edildiğine ve uzun-bellekli (long-memory) korelasyonların var olduğuna işarettir. Hurst, multifraktal genelleştirmenin özel bir noktasıdır: ikinci moment için $H = \zeta_2 / 2$ ilişkisi (bkz. [[zeta-q-olcekleme]]) Hurst üstelini multifraktal spektruma bağlar.

## Formül
Klasik R/S tahmini:
$$
\mathbb{E}\left[\frac{R(\tau)}{S(\tau)}\right] \sim \tau^{H}, \quad \tau \to \infty
$$
İkinci momentin ölçeklenmesinden tahmin (multifraktal bağlamda):
$$
\mathbb{E}\left[|X(t+\tau) - X(t)|^{2}\right] \sim \tau^{2H}
$$

## Ana Bağlamlar
- [[rescaled-range-rs]] klasik tahmin yöntemi
- [[multifraktal-spektrum]] çoklu üstel genelleştirme
- [[zeta-q-olcekleme]] $H = \zeta_2/2$ ilişkisi
- [[fraktal-piyasa-hipotezi-fmh]] kavramsal çerçeve
- [[portfoy-hurst-kuadratik-form]] portföy düzeyinde uzantı

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — portföy seviyesinde $H_p$ ölçümü ve kuadratik form analizinin merkez parametresidir
- [Tauron](../../projects/tauron/) — multifraktallık parametrelerinin (λ, ζ_q) klasik öncüsü; Markowitz'in fraktal düzeltmesinde temel girdi
- [Seminer](../../projects/) — fraktal piyasa örneklerinde gözlemsel kanıt parametresi

## Kaynak
[[hurst-1951]], [[mandelbrot-hudson]], [[peters-1991]]
