---
baslik: "Kaldıraç Etkisi (Leverage Effect)"
slug: "leverage-effect"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, ampirik, stokastik-volatilite]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Kaldıraç Etkisi (Leverage Effect)

## Özü
Hisse fiyatı düştüğünde volatilitenin sistematik olarak yükselmesi, yani fiyat ve volatilite arasındaki negatif korelasyonu ifade eden ampirik gözlemdir.

## Tanım
Black (1976) tarafından ilk kez raporlanan kaldıraç etkisi, hisse fiyatındaki düşüşlerin firmanın borç/öz-kaynak oranını yükselttiği ve dolayısıyla pay başına volatiliteyi artırdığı argümanıyla açıklanır; ancak modern literatür bunun davranışsal ve risk-prim kanallarıyla da güçlendirildiğini savunur. [[heston-stokastik-volatilite]] modelinde bu etki, hisse-volatilite Wiener süreçlerinin korelasyon parametresi $\rho < 0$ ile yakalanır ve [[volatility-smile]]'in solak eğikliğini doğal olarak üretir. Finansal modellerin ampirik geçerliliği için $\rho$'nun negatif kalibre edilmesi neredeyse zorunludur.

## Formül
Heston'da:
$$
d\langle W^{(S)}, W^{(v)}\rangle_t = \rho\, dt, \quad \rho < 0
$$
İmplied vol eğimi: $\partial \sigma_{\text{imp}}/\partial K < 0$ (hisse opsiyonları için).

## Ana Bağlamlar
- [[heston-stokastik-volatilite]] — etkiyi $\rho$ ile yakalayan model
- [[volatility-smile]] — eğikliğin gözlemsel sonucu
- [[bipartite-korelasyon]] — çoklu varlıkta genelleştirilmiş hali
- [[fat-tailed-dagilim]] — sol kuyruk ağırlığını besler

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — Black-Scholes ötesi ampirik motivasyon
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kalibrasyon hedefi olarak kritik

## Kaynak
[[heston-1993]], [[hull-2008]]
