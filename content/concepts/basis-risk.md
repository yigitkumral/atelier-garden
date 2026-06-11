---
baslik: "Basis Risk (Baz Riski)"
slug: "basis-risk"
olusturuldu: 2026-05-24
guncellendi: 2026-05-24
etiketler: [finans, turev, hedge, risk-yonetimi, emtia, kobi]
aliases: [baz-riski, basis-risiki, basis-risk]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Basis Risk (Baz Riski)

## Özü
Hedge edilen fiziki ürün ile kullanılan futures kontratının lokasyon, kalite, para birimi, vade veya ürün tipi açısından birebir aynı olmaması nedeniyle hedge'in kusurlu çalışması riski.

## Tanım
**Basis** basitçe spot fiyat ile futures fiyatı arasındaki farktır:
$$
\text{Basis}_t = S_t - F_t
$$
İdeal bir hedge'de basis sabit kalmalıdır; ancak gerçekte basis zamanla değişir ve bu değişim hedger için **risk** doğurur. [[futures-hedging-stratejileri]] uygulamada basis stabilitesi varsayımına dayanır; bu varsayım Türkiye gibi sığ piyasalarda ihlal edilir. CME Hedger's Guide, basis'in tarihsel ve mevsimsel desenler izleyebileceğini, alıcı/satıcıların **yerel basis defteri** tutması gerektiğini vurgular. Investopedia basis riskini lokasyon, ürün/kalite ve takvim uyumsuzluğu olarak sınıflandırır.

Türk gıda toptancısı için basis kaynakları: TR fiziki fiyat (TL) − global futures (USD/EUR), navlun, gümrük, TMO regülasyonu, Karadeniz vs ABD kalite farkı. [[optimal-hedge-ratio]] korelasyon bazlı kısmi hedge ile basis riskini *azaltır* ama sıfırlamaz.

## Formül
Hedge sonu net pozisyon (short hedger için):
$$
\text{Net} = S_{T} + (F_{t_0} - F_{T}) = F_{t_0} + (S_T - F_T) = F_{t_0} + \text{Basis}_T
$$
Hedger $t_0$'da $F_{t_0}$ fiyatını kilitler ama nihai sonuç $T$ anındaki **basis**'e bağlıdır. Basis tahmin edilemiyorsa hedge "1:1" değildir.

## Türkiye-Spesifik Basis Kaynakları
| Risk Tipi | Örnek |
|---|---|
| Lokasyon | CBOT Chicago wheat vs Türkiye İç Anadolu fiyatı |
| Kalite | Euronext milling wheat vs Türkiye ekmeklik buğday |
| Kur | Futures USD/EUR; satış TL |
| Vergi/Regülasyon | TMO alımları, ithalat kotası, gümrük vergisi |
| Navlun | Karadeniz, Akdeniz, konteyner/bulk navlun |
| Vade | Fiziki alım/satım tarihi futures vadesiyle uyuşmayabilir |
| Ürün Dönüşümü | Buğday → un, kakao → çikolata, süt → peynir |

## Ana Bağlamlar
- [[futures-hedging-stratejileri]] — basis riskinin gerçekleştiği uygulama
- [[optimal-hedge-ratio]] — basis riskini minimize eden formül
- [[delta-hedging]] — opsiyon tarafında benzer "first-order" hedge mantığı

## Projelerde Kullanım
- [Gıda Toptancı Emtia Hedging](../../projects/gida-toptanci-emtia-hedging/) — TR fiziki vs global futures basis defteri kritik
- [IMF527 Finansal Risk Yönetimi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — VaR ve hedge effectiveness ders konularıyla bağlantılı

## Kaynak
- CME Group, *Grain and Oilseed Hedger's Guide*
- Investopedia, "Basis Risk"
- Hull, J. (2018). *Options, Futures, and Other Derivatives*, Ch. 3
