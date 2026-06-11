---
baslik: "Volatilitenin Volatilitesi (Vol-of-Vol)"
slug: "vol-of-vol"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, stokastik-volatilite, parametre]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Volatilitenin Volatilitesi (Vol-of-Vol)

## Özü
Stokastik volatilite modellerinde varyans sürecinin difüzyon katsayısı; varyansın kendisinin ne kadar çalkantılı evrildiğini ölçer.

## Tanım
[[heston-stokastik-volatilite]] modelinde varyans süreci $dv_t = \kappa(\theta - v_t)dt + \sigma_v \sqrt{v_t}\,dW_t^{(2)}$ biçimindedir; buradaki $\sigma_v$ "vol-of-vol" parametresidir. Yüksek $\sigma_v$, varyansın hızlı ve şiddetli sıçramalarına neden olur ve bu durum [[volatility-smile]]'in derinliğini, kuyruk olasılıklarını ve [[moment-patlama]] eşiğini doğrudan etkiler. Kalibrasyonda piyasa-implied gülümseme eğriliğinden çıkarılır; geri kazanım için [[karakteristik-fonksiyon]] tabanlı yöntemler kullanılır.

## Formül
Heston modelinde:
$$
dv_t = \kappa(\theta - v_t)\, dt + \underbrace{\sigma_v}_{\text{vol-of-vol}} \sqrt{v_t}\, dW_t^{(2)}
$$
[[feller-kosulu]] $2\kappa\theta \ge \sigma_v^2$ ile ilişkilidir: yüksek vol-of-vol Feller'ı kırma riskini artırır.

## Ana Bağlamlar
- [[heston-stokastik-volatilite]] — parametrenin tanımlandığı model
- [[volatility-smile]] — eğriliği belirler
- [[feller-kosulu]] — pozitiflik için üst sınır koyar
- [[moment-patlama]] — büyük $\sigma_v$ moment patlamalarını tetikler

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — stokastik volatilite kalibrasyonu
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum simülasyon doğruluğunu sınayan parametre

## Kaynak
[[heston-1993]], [[andersen-piterbarg-2007]]
