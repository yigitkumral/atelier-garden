---
baslik: "Karakteristik Fonksiyon"
slug: "karakteristik-fonksiyon"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fourier, dağılım, fiyatlama]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Karakteristik Fonksiyon

## Özü
Bir rastgele değişkenin $X$ dağılımını, yoğunluk yerine onun Fourier dönüşümü $\varphi_X(t) = \mathbb{E}[e^{itX}]$ üzerinden temsil eden araç; affine SDE modellerinde kapalı form yoğunluk olmasa da $\varphi$ açıkça yazılabildiği için fiyatlama yöntemlerinin omurgası.

## Tanım
$$
\varphi_X(t) = \mathbb{E}[e^{itX}] = \int_{-\infty}^{\infty} e^{itx}\, f_X(x)\, dx.
$$

Özellikleri:
- $|\varphi_X(t)| \le 1$, $\varphi_X(0) = 1$
- Bağımsız değişkenler için $\varphi_{X+Y} = \varphi_X \varphi_Y$
- Tersine çevrim: $f_X(x) = \tfrac{1}{2\pi} \int e^{-itx}\, \varphi_X(t)\, dt$
- Momentler: $\mathbb{E}[X^k] = i^{-k} \varphi_X^{(k)}(0)$

**Affine modeller:** Heston, CIR, çoğu Lévy süreci için $\log S_T$ değişkeninin karakteristik fonksiyonu $\varphi(t) = \exp(A(t) + B(t) v_0)$ formunda Riccati ODE'lerden çözülür. Bu, [[fast-forwardability]] kavramının matematiksel kalbidir — yoğunluk üzerinden değil $\varphi$ üzerinden $T$ ufkuna doğrudan atlama.

**Fiyatlama uygulaması:** Carr-Madan FFT, COS yöntemi, Lewis formülü gibi teknikler $\varphi$'yi alıp Avrupa opsiyon fiyatını tek integralle hesaplar — MC'ye gerek kalmaz ama yalnızca yol-bağımsız payoff'lar için.

## Ana Bağlamlar
- [[heston-stokastik-volatilite]] — affine $\varphi$'nin kanonik örneği
- [[cir-modeli]] — non-central chi-squared $\varphi$
- [[fast-forwardability]] — kuantum bağlamı
- [[non-central-chi-squared]] — CIR'ın geçiş dağılımı

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al.'in fast-forward alt bölümünün altyapısı
- [Seminer](../../projects/ders/2026-bahar-seminer/) — yarı-analitik fiyatlama bağlamı

## Kaynak
[[heston-1993]], [[broadie-kaya-2006]], [[herman-2026]]
