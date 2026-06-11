---
baslik: "Black-Scholes Modeli"
slug: "black-scholes"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, turev, opsiyon-fiyatlama]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Black-Scholes Modeli

## Özü
Avrupa tipi bir hisse opsiyonunun arbitrajsız fiyatını kapalı-form çözen klasik PDE-tabanlı türev fiyatlama modelidir.

## Tanım
Black-Scholes modeli, dayanak varlığın [[geometric-brownian-motion]] sürecini izlediği, sabit faiz ve sabit volatilite varsayımları altında bir Avrupa opsiyonunun değerini analitik olarak veren bir çerçevedir. Risk-nötr ölçü altında [[ito-calculus]] ile delta-hedge edilmiş bir portföy kurularak ikinci dereceden parabolik bir kısmi diferansiyel denklem türetilir; sınır koşulu vade günündeki [[payoff-fonksiyonu]]'dur. Çözüm, log-normal fiyat dağılımının kümülatif fonksiyonu cinsinden ifade edilir ve modern türev finansının kuramsal omurgasını oluşturur.

## Formül
$$
C(S_0, t) = S_0 \, \Phi(d_1) - K e^{-r(T-t)} \Phi(d_2)
$$
$$
d_1 = \frac{\ln(S_0/K) + (r + \sigma^2/2)(T-t)}{\sigma\sqrt{T-t}}, \quad d_2 = d_1 - \sigma\sqrt{T-t}
$$
Burada $S_0$ spot fiyat, $K$ kullanım fiyatı, $r$ risksiz faiz, $\sigma$ volatilite, $T-t$ vadeye kalan süre ve $\Phi$ standart normal CDF'dir.

## Ana Bağlamlar
- [[geometric-brownian-motion]] — fiyat sürecinin altyapısı
- [[ito-calculus]] — PDE türetimi için kullanılan araç
- [[greeks]] — modelden türetilen duyarlılıklar
- [[avrupa-opsiyonu]] — fiyatlanan sözleşme tipi

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — pedagojik tarihçe (klasik faz)
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum hızlanma karşılaştırmasında klasik baseline

## Kaynak
[[black-scholes-1973]], [[hull-2008]]
