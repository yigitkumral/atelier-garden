---
baslik: "Cox-Ingersoll-Ross (CIR) Modeli"
slug: "cir-modeli"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, faiz-orani, stokastik-surec]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Cox-Ingersoll-Ross (CIR) Modeli

## Özü
Pozitiflik koşulunu doğal olarak sağlayan, [[mean-reversion]] özellikli karekök-difüzyon faiz oranı modelidir.

## Tanım
CIR modeli, kısa vadeli faiz oranlarını uzun-vade ortalamasına geri çekilen ama negatif değer alamayan bir SDE ile tanımlar. Difüzyon katsayısı oranın kareköküyle orantılıdır; bu, oran sıfıra yaklaştığında varyansın söndüğü ve dolayısıyla [[feller-kosulu]] sağlandığında sürecin kesinlikle pozitif kaldığı anlamına gelir. Geçiş yoğunluğu [[non-central-chi-squared]] dağılımdır; bu sayede tahvil fiyatları ve ileriye dönük oranlar için kapalı-form ifadeler türetilebilir. Aynı SDE biçimi [[heston-stokastik-volatilite]] modelinde varyans süreci olarak yeniden ortaya çıkar.

## Formül
$$
dr_t = \kappa(\theta - r_t)\, dt + \sigma \sqrt{r_t}\, dW_t
$$
$\kappa$ geri çekiliş hızı, $\theta$ uzun-vade ortalaması, $\sigma$ volatilite katsayısıdır. Pozitiflik koşulu:
$$
2\kappa\theta \ge \sigma^2 \quad \text{(Feller)}
$$

## Ana Bağlamlar
- [[mean-reversion]] — modelin temel davranışı
- [[feller-kosulu]] — sıfıra ulaşmayı engelleyen koşul
- [[non-central-chi-squared]] — geçiş yoğunluğu
- [[heston-stokastik-volatilite]] — varyans sürecinde aynı yapı

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — faiz oranı modellemesi pedagojisi
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum simülasyon makalesinde örnek SDE

## Kaynak
[[cir-1985]], [[hull-2008]]
