---
baslik: "M_q(τ) Yapı Fonksiyonu"
slug: "m-q-tau-momentleri"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, multifraktal, moment, yapi-fonksiyonu]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# M_q(τ) — Yapı Fonksiyonu (Structure Function)

## Özü
Bir fiyat/getiri serisinin $q$'uncu mutlak momentinin zaman penceresi $\tau$ ile nasıl ölçeklendiğini ölçen ham yapı; multifraktal analizin gözlemsel girdisi.

## Tanım
$X(t)$ log-fiyat süreci olmak üzere, $\tau$ pencereli mutlak getiri $|X(t+\tau) - X(t)|$ tanımlanır. Bunun $q$'uncu mutlak momentinin zaman ortalaması $M_q(\tau)$, multifraktallığın temel ölçüm aracıdır. Pratikte $q \in \{1, 2, 3, 4, 5\}$ ve $\tau$ logaritmik bir ızgarada (örn. 5 dakika, 1 saat, 1 gün, 1 hafta) hesaplanır. $\log M_q(\tau)$ vs $\log \tau$ grafiğinin eğimi $\zeta_q$'yu verir (bkz. [[zeta-q-olcekleme]]). Bu işlem her $q$ için tekrarlandığında $\zeta_q$ eğrisi elde edilir; oradan da [[parabolik-fit-modeli]] ile parametrelendirilir. Ölçüm pratikte gürültülü olduğu için bootstrap güven aralıkları ve [[block-bootstrap]] kullanılır (bkz. [[estimator-gurultusu-bias-variance]]).

## Formül
$$
M_q(\tau) = \frac{1}{N_\tau} \sum_{t=1}^{N_\tau} |X(t+\tau) - X(t)|^q
$$
Ölçeklenme:
$$
M_q(\tau) \sim \tau^{\zeta_q}
$$
Tahmin: log-log lineer regresyon ile $\zeta_q$ eğimden okunur.

## Ana Bağlamlar
- [[zeta-q-olcekleme]] log-log eğim
- [[parabolik-fit-modeli]] $\zeta_q$'nun parametrik fit'i
- [[block-bootstrap]] güven aralığı için
- [[estimator-gurultusu-bias-variance]] tahmin gürültüsü

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — hem varlık hem portföy yapı fonksiyonu hesabı, log-log fit pipeline'ı
- [Tauron](../../projects/tauron/) — $\zeta_q$ ölçümünün ham girdisi; simülatörün veri katmanı
- [Seminer](../../projects/) — multifraktallığın gözlemsel kanıt görselleri buradan üretilir

## Kaynak
[[sornette-multifractal]]
