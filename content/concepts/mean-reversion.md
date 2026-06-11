---
baslik: "Ortalamaya Dönüş (Mean Reversion)"
slug: "mean-reversion"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [stokastik-surec, finans, faiz-orani]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Ortalamaya Dönüş (Mean Reversion)

## Özü
Bir stokastik sürecin uzun-vade ortalamasından sapma büyüdükçe, drift teriminin sapmayı azaltacak yönde tepki gösterdiği dinamiktir.

## Tanım
Mean-reverting süreçler, [[drift]] yapısı $\mu(X_t) = \kappa(\theta - X_t)$ biçiminde olan SDE'lerle modellenir; $\kappa$ geri çekilme hızını, $\theta$ uzun-vade ortalamasını verir. Bu yapı, faiz oranı ([[cir-modeli]]), volatilite ([[heston-stokastik-volatilite]]), commodity spot fiyatları ve emisyon kotaları gibi makroekonomik denge gösteren değişkenlerde gözlemlenir. Ornstein-Uhlenbeck süreci, en basit Gaussian mean-reverting örnektir; karekök-difüzyonlu CIR varyantı pozitiflik şartı koşar. Sürecin ergodik dağılımı $\theta$ etrafında yoğunlaşır ve uzun-vade tahmin değeri $\theta$'ya yakınsar.

## Formül
Genel mean-reverting SDE:
$$
dX_t = \kappa(\theta - X_t)\, dt + \sigma_X(X_t)\, dW_t
$$
Yarılanma süresi: $t_{1/2} = \ln 2 / \kappa$.

## Ana Bağlamlar
- [[cir-modeli]] — pozitif kalan kareköklü mean-reversion
- [[heston-stokastik-volatilite]] — varyansın geri çekilme yapısı
- [[drift]] — geri çekme terimini barındıran bileşen
- [[feller-kosulu]] — pozitiflik için ek koşul

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — faiz ve volatilite modellerinin ortak özelliği
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum SDE simülasyonunun tipik test rejimi

## Kaynak
[[cir-1985]], [[hull-2008]]
