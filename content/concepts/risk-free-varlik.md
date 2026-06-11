---
baslik: "Risk-Free Varlık"
slug: "risk-free-varlik"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [finans, portfoy, varsayim]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Risk-Free Varlık

## Özü
Sıfır varyansa ve diğer varlıklarla sıfır kovaryansa sahip varsayılan, sabit getiri $r_f$ veren teorik varlık türüdür.

## Tanım
Risk-free varlık (risksiz varlık), Markowitz çerçevesinin standart genişletmesinde varlık evrenine eklenir; genellikle kısa vadeli devlet tahvilleriyle (örn. T-Bill) yaklaşık olarak temsil edilir. Modelin matematiksel sonucu: [[etkin-sinir]] eğri yerine [[sermaye-tahsis-dogrusu-cal]]'a dönüşür ve riskli kısmın kompozisyonu tek bir noktaya, [[tangent-portfoy]]'a indirgenir. Pratikte gerçek bir varlık tam olarak risksiz değildir; nominal getiri dahi enflasyon, kur ve temerrüt riskleriyle yüklüdür. Klasik tahvil literatüründe "risksiz oran" ile "kısa-vadeli para piyasası oranı" arasında ayrım yapılır; [[markowitz-1952]]'nin orijinal kurgusu bu varlığı içermez, eklemesi sonraki çalışmalarındadır (ör. Tobin 1958).

## Formül
Tanımlayıcı varsayımlar:
$$
\mathrm{Var}(r_f) = 0, \quad \mathrm{Cov}(r_f, r_i) = 0 \;\; \forall i
$$
Risk-free dahil portföy getirisi:
$$
\mu_p = (1 - w^T \mathbf{1}) r_f + w^T \mu, \quad \sigma_p^2 = w^T \Sigma w
$$
burada $w$ riskli varlık ağırlık vektörüdür, $1 - w^T \mathbf{1}$ risk-free payı.

## Ana Bağlamlar
- [[sermaye-tahsis-dogrusu-cal]] başlangıç noktası ($\sigma=0, \mu=r_f$)
- [[tangent-portfoy]] varlığı bu varsayıma dayanır
- [[sharpe-orani]] tanımındaki referans
- [[markowitz-portfoy-teorisi]] genişletilmiş hâlinin tetikleyicisi

## Projelerde Kullanım
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — risk-free dahil portföyler için $r_f$ girdisi (T-Bill vb.)
- [Tauron](../../projects/tauron/) — risk-free oranın multifraktal modeldeki konumlanması (klasik referans olarak korunur)
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — Sharpe karşılaştırmasında baz oran

## Kaynak
[[markowitz-1952]]
