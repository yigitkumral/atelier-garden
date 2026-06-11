---
baslik: "Multifraktal Spektrum f(α)"
slug: "multifraktal-spektrum"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, multifraktal, spektrum, legendre]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Multifraktal Spektrum f(α)

## Özü
Tek bir Hurst üsteli yerine, sürecin yerel düzensizlik (singularity) derecelerinin dağılımını tanımlayan iki-boyutlu fraktal kimlik kartı.

## Tanım
Multifraktal bir süreç, farklı zaman/ölçek bölgelerinde farklı yerel ölçek üstellerine $\alpha$ sahiptir. $f(\alpha)$ fonksiyonu, belirli bir $\alpha$ değerine sahip noktaların oluşturduğu altkümesinin Hausdorff fraktal boyutunu verir. Tek-fraktal (monofraktal) süreçlerde spektrum tek bir noktaya çöker; multifraktallık spektrumun genişliği ile ölçülür. Pratikte $f(\alpha)$, [[zeta-q-olcekleme]] yapısı $\zeta_q$'nun [[parabolik-fit-modeli]] gibi bir parametrik fit'i üzerinden Legendre dönüşümü ile elde edilir. Spektrumun maksimum noktası, sürecin baskın ölçek üstelini verir; genişlik ise multifraktallığın gücüdür ve [[multifraktallik-siddeti-lambda]] parametresine bağlanır.

## Formül
Legendre dönüşümü:
$$
\alpha(q) = \frac{d\zeta_q}{dq}, \qquad f(\alpha) = q\,\alpha(q) - \zeta_q
$$
Parabolik durumda $\zeta_q = a q^2 + b q + c$ ise:
$$
f(\alpha) = c - \frac{(\alpha - b)^2}{4a}
$$
Spektrum genişliği $\Delta\alpha = \alpha_{\max} - \alpha_{\min}$ multifraktallığın gücünü ölçer.

## Ana Bağlamlar
- [[zeta-q-olcekleme]] Legendre eşi
- [[parabolik-fit-modeli]] uygulamada parametrik fit
- [[multifraktallik-siddeti-lambda]] genişliği özetleyen tek skaler
- [[hurst-exponent]] spektrumun özel noktası
- [[fraktal-piyasa-hipotezi-fmh]] kavramsal çerçeve

## Projelerde Kullanım
- [Tauron](../../projects/tauron/) — multifraktal düzeltme cezasının (λ, ζ_q parametrelerinin) çıktığı ana yapı
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — hem varlık bazında hem portföy düzeyinde multifraktal kimlik analizi
- [Seminer](../../projects/) — fraktal piyasa hipotezinin görsel/sezgisel anlatımında

## Kaynak
[[sornette-multifractal]], [[mandelbrot-hudson]]
