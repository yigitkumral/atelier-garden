---
baslik: "Heston Stokastik Volatilite Modeli"
slug: "heston-stokastik-volatilite"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, stokastik-volatilite]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Heston Stokastik Volatilite Modeli

## Özü
Anlık varyansı CIR-tipi bir kareköklü difüzyonla evrilten ve hisse-volatilite arasında negatif korelasyona izin veren ikiz-faktörlü opsiyon fiyatlama modelidir.

## Tanım
Heston modeli, [[black-scholes]]'in sabit-volatilite varsayımını gevşetir ve volatiliteyi kendisi rastgele hareket eden bir süreç olarak ele alır. Hisse fiyatı log-normal bir difüzyon takip ederken anlık varyans bir [[cir-modeli]] yapısında karekök-difüzyon olarak modellenir. İki sürücü Wiener sürecinin korelasyonu $\rho$, ampirik [[leverage-effect]]'i (negatif fiyat-vol kovaryansı) yakalar ve [[volatility-smile]]'in eğikliğini doğal şekilde üretir. Karakteristik fonksiyon kapalı formda olduğu için [[karakteristik-fonksiyon]] tabanlı Fourier yöntemleriyle hızlı opsiyon fiyatlaması mümkündür.

## Formül
$$
dS_t = \mu S_t\, dt + \sqrt{v_t}\, S_t\, dW_t^{(1)}
$$
$$
dv_t = \kappa(\theta - v_t)\, dt + \sigma_v \sqrt{v_t}\, dW_t^{(2)}, \quad d\langle W^{(1)}, W^{(2)}\rangle_t = \rho\, dt
$$
Parametreler: $\kappa$ mean-reversion hızı, $\theta$ uzun-vade varyansı, $\sigma_v$ [[vol-of-vol]], $\rho$ kaldıraç korelasyonu.

## Ana Bağlamlar
- [[cir-modeli]] — varyans sürecinin yapısal kalıbı
- [[leverage-effect]] — $\rho < 0$ üzerinden ampirik gerçek
- [[vol-of-vol]] — $\sigma_v$ parametresinin rolü
- [[volatility-smile]] — modelin doğal ürettiği gözlem
- [[moment-patlama]] — yüksek momentlerin sonlu olmadığı rejim

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — Black-Scholes ötesi pedagojik geçiş
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum hızlanma vaadinin temel test modeli

## Kaynak
[[heston-1993]], [[andersen-piterbarg-2007]]
