---
baslik: "ζ_q Ölçek Üsteli"
slug: "zeta-q-olcekleme"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, multifraktal, moment, olcekleme]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# ζ_q — q'uncu Moment Ölçek Üsteli

## Özü
Mutlak getirilerin $q$'uncu momentinin zaman penceresi $\tau$ ile ölçeklenme hızını tanımlayan, multifraktallığın temel niceleyicisi.

## Tanım
Klasik tek-üstel (monofraktal) hipotezde $\zeta_q = qH$ doğrusal davranır. Multifraktal süreçlerde ise $\zeta_q$ doğrusal değildir — eğri (genelde içbükey) bir yapı sergiler ve bu doğrusal-olmayan kısım sürecin multifraktal kimliğini taşır. $\zeta_q$ fonksiyonu [[multifraktal-spektrum]] $f(\alpha)$ ile Legendre dönüşümü üzerinden eştir; pratikte $\zeta_q$ doğrudan ölçülmesi (bkz. [[m-q-tau-momentleri]]) ve sonra [[parabolik-fit-modeli]] ile fit edilmesi en yaygın yoldur. Hurst üsteli özel bir noktaya karşılık gelir: $H = \zeta_2 / 2$.

## Formül
Yapı fonksiyonu (structure function) tanımı:
$$
M_q(\tau) = \mathbb{E}\big[|X(t+\tau) - X(t)|^q\big] \sim \tau^{\zeta_q}, \qquad \tau \to 0
$$
Tahmin: log-log uzayda eğim
$$
\zeta_q = \lim_{\tau \to 0} \frac{\log M_q(\tau)}{\log \tau}
$$

## Ana Bağlamlar
- [[m-q-tau-momentleri]] ham ölçüm yapısı
- [[parabolik-fit-modeli]] yaygın parametrik form
- [[multifraktal-spektrum]] Legendre eşi
- [[hurst-exponent]] $H = \zeta_2/2$
- [[multifraktallik-siddeti-lambda]] eğriliğin tek-sayı özeti

## Projelerde Kullanım
- [Tauron](../../projects/tauron/) — fraktal düzeltme cezası doğrudan $\zeta_q$ üzerinden inşa edilir
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — varlık ve portföy momentlerinin ölçeklenme analizinde merkez parametre
- [Seminer](../../projects/) — multifraktallık argümanının teknik dayanağı

## Kaynak
[[sornette-multifractal]], [[bouchaud-volatility-clustering]]
